Exercise 3
==========

**Due date:** Please complete this exercise by **the end of day on Friday the 5th of February 2021** (day **after** the next practical session).

.. admonition:: Exercise 3 - Start your assignment

    You can start working on your personal (private) copy of Exercise by `accepting the GitHub Classroom assignment <https://classroom.github.com/a/Vzsx_8Gp>`__. Notice that if you are using
    GitHub Classroom for the first time, it might ask from you a permission to verify your GitHub identity. In such case, choose "Authorize GitHub Classroom".

    After you have your personal exercise in GitHub, start doing the programming using CSC Notebooks:

    .. image:: https://img.shields.io/badge/launch-CSC%20notebook-blue.svg
        :target: https://notebooks.csc.fi/#/blueprint/c54303e865294208ba1ef381332fd69b

You can also take a look at the open course copy of `Exercise 3 in the course GitHub repository <https://github.com/Sustainability-GIS-2021/Exercise-3>`__ (does not require logging in).
Note that you should not try to make changes to this copy of the exercise, but rather only to the copy available via GitHub Classroom.

.. note::

    We will use git and GitHub when working with the exercises.
    You can find instructions for using git and the Jupyter Lab git plugin :doc:`in here <../L1/git-basics>`.

Hints
-----

More detailed instructions for parsing trajectory statistics
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**When looping over the groups in Problem 3:**

- Check if the maximum value of the column `speed` is zero. If it is, do not proceed further and continue to the next iteration. In case it is not:
- Create a TrajectoryCollection from the group using `vehicle_id` as the identifier.
- Add speed to the TrajectoryCollection (overwrite existing one).
- If there are any trajectories in our TrajectoryCollection, select the first trajectory from the TrajectoryCollection (*each collection should only have a single Trajectory because we have grouped the data ourselves based on "vehicle_id"*)
- Split the trajectory based on criteria that if there is a 5-minute time gap between observations, the trajectory should be splitted into multiple ones. This step is used to detect if there were multiple trips between same route and direction (which is likely because the same vehicle travels the same route many times during the day). You can use the [mpd.ObservationGapSplitter()](https://movingpandas.readthedocs.io/en/latest/trajectorysplitter.html#movingpandas.ObservationGapSplitter) to split the observations.
- Iterate over the splitted trajectories and:
- Calculate the speed in kilometers per hour (into column `speed_kmph`) based on the `speed` information which is reported as `meters per second`.
- Based on the `speed_kmph` select only rows that have speed over 1 kilomters per hour.
- If there weren't any observations left after you do the selection in the previous step, do not proceed but continue to the next iteration. Otherwise:
- Create a LineString geometry from the trajectory (you can take advantage of the `.to_linestring()` method that is part of the `Trajectory` class.
- Calculate the average speed of the trajectory based on the `speed_kmph`
- Calculate the standard deviation of the speed of the trajectory (again based on the `speed_kmph`)
- Parse other useful information from the trajectory (should be a single value): vehicle_id, route_id, direction_id, start_time (i.e. what was the first timestamp of the trajectory)
- After you have parsed all the previous information, make a GeoDataFrame out of them and store them into `results` list.