Exercise 2
==========

**Due date:** Please complete this exercise by **the end of day on Friday the 29th of January 2021** (day after the next practical session).

.. admonition:: Exercise 2 - Start your assignment

    You can start working on your personal (private) copy of Exercise by `accepting the GitHub Classroom assignment <https://classroom.github.com/a/kIBYhgbe>`__. Notice that if you are using
    GitHub Classroom for the first time, it might ask from you a permission to verify your GitHub identity. In such case, choose "Authorize GitHub Classroom".

    After you have your personal exercise in GitHub, start doing the programming using CSC Notebooks:

    .. image:: https://img.shields.io/badge/launch-CSC%20notebook-blue.svg
        :target: https://notebooks.csc.fi/#/blueprint/c54303e865294208ba1ef381332fd69b

You can also take a look at the open course copy of `Exercise 2 in the course GitHub repository <https://github.com/Sustainability-GIS-2021/Exercise-2>`__ (does not require logging in).
Note that you should not try to make changes to this copy of the exercise, but rather only to the copy available via GitHub Classroom.

.. note::

    We will use git and GitHub when working with the exercises.
    You can find instructions for using git and the Jupyter Lab git plugin :doc:`in here <../L1/git-basics>`.

Hints
-----

Hint 1: Running out of memory at CSC Notebooks?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In tutorial 2 and exercise 2, we create fairly large networks (covering whole Helsinki metropolitan area) which consumes
quite a bit of memory. Unfortunately, the CSC Notebook instances have only 8 GB of memory which might cause a situation
in which your instance runs out of memory Jupyter Lab Python kernel just stops (without producing any clear error message).
If that situation happens, then it is recommended to try to reduce the memory footprint in your data. This can be done
easily by dropping all unnecessary columns from your data.

**Detected problem:** You might end up running out of memory when trying to create a NetworkX graph from your edges.
**Solution:** After you have modified the edges of your road network, select only following columns from your edges that
are required for creating the routable graph: ``"oneway", "travel_time_seconds", "length", "u", "v", "geometry"``.

After the above trick, you should be able to create a graph and finish all problems in Exercise 2.

Hint 2: Do your programming in small steps and only for one object at a time
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the Exercise 2, you should calculate catchment areas for many hospitals and calculate different things based
on the data. Whenever repeating the same analytical steps for many objects (here hospitals and postal code area),
it is highly recommended that before starting to loop over your data, you try to first finish all the required steps for
one hospital or postal code area. Repeat the analytical processes for all hospitals/postal code areas only after
you are certain that the code does what you think it should do.

Hint 3: How to convert a NetworkX graph to GeoDataFrame?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you have created a routable Networkx graph from nodes and edges, it is naturally also possible to convert
the graph back to GeoDataFrames. `OSMnx <https://github.com/gboeing/osmnx>`__ package provides a handy function
to do this called ``ox.graph_to_gdfs()`` which takes the NetworkX graph as an input and returns the nodes and edges
associated with the graph (including the edge attributes).