Final assignment
================

.. admonition:: Start your assignment

    Start your final assignment by accepting the `GitHub Classroom <>`_ for the final work.

    After you have your personal exercise in GitHub, start doing the programming using CSC Notebooks:

    .. image:: https://img.shields.io/badge/launch-CSC%20notebook-blue.svg
        :target: https://notebooks.csc.fi/#/blueprint/c54303e865294208ba1ef381332fd69b

Aim of the work
---------------

The final project is an individual task where the aim is to apply spatial data science methods to study a selected
sustainability challenge and write a short report documenting your work.

You can select a pre-defined topic, or develop your own question. You should take advantage of your programming and spatial data science skills,
version control skills (git + GitHub) and good coding practices (writing readable code) when doing the final assignment.

Think about the final project as a challenge for yourself to show and implement the programming skills that you have learned this far.
You have learned a lot already!

Final work structure
--------------------

Here is the suggested structure of the work, that also serves as the basis for grading:

1. **Introduction - Research questions** (Overview: What are you studying/research questions? What data do you use? What methods?)
2. **Data acquisition** (Fetching data, subsetting data, storing intermediate outputs etc.)
3. **Data analysis** (Analytical steps required to produce the results)
4. **Visualization** (Visualizing main results and other relevant information as maps and graphs)
5. **Results / conclusions** (What did your analysis reveal?)

**The workflow should be repeatable and well documented.** In other words, anyone who gets a copy of your repository should be able to run your code, and read your code.

You can design the structure of your assignment freely as long as it contains the main components listed above.
If you have longer pieces of code, we suggest that you create functions in separate script files, and demonstrate the use of those functions in one or several notebooks.
All in all, the work should include these components:

- A short introduction to the topic
- Short description of the datasets you used
- Short generic description of the methods you used
- Actual codes and visualizations to produce the **results**
- Discussion related to the results (what should we understand and see from them?)
- Reflection about the analysis, for example:
  - What can we see/learn from your analysis?
  - What kind of assumptions, biases or uncertainties are related to the data and/or the analyses that you did?
  - Any other notes that the reader should know about the analysis

What should be returned?
------------------------

Organize all your material into your personal Final-Assignment repository and store your work into the ``final_assignment.ipynb`` file.
If you wish, you can write parts of your analysis workflow into separate Python script files (``.py``) and then apply them inside the Notebook.
Anyone who downloads the repository should be able to **read your code** and documentation and understand what is going on, and **run your code** in order to reproduce the same results.
Please return a clean and coherent notebook (think it as a report) that only contains necessary code cells to reproduce and report the findings of your analyses
(i.e. remove all unnecessary code blocks for printing the first rows of the GeoDataFrame etc.).
**Please ensure that everything works before returning your work**: Run the whole notebook (`like this <https://stackoverflow.com/a/53214668>`__)
and return the work once you do not have any surprising errors and your results look as they should (this is what reproducibility is all about!).

*Note: If your code requires some python packages not found in the csc notebooks environment, please mention them also in the report and provide installation instrutions.*

When is the deadline?
---------------------

The deadline for returning the final assignment is **March 14th, 2021**. Naturally, you can return the assignment earlier.
We apologise that the course is slightly prolonged over a single study period this year. If you have tight schedule in the following weeks
(e.g. many new courses starting in the following study period), please contact the teacher so we can agree on a schedule for your final assignment.

Label your submissions as "submitted" in the exercise repository's `README.md` under "status" once you are finished with the Final assignment.

Submissions are checked after the deadline and the final grade is given within 4 weeks after the deadline.
If you need the course grade earlier, please contact the course instructor.

Grading
-------

The grading is based on a typical 0-5 scale. See detailed grading criteria :doc:`here <final-assignment-grading>`.
The final assignment is graded based on:

- Main analysis steps (data fetching, data analysis, visualization)
- Repeatability (it should be possible to repeat the main analysis steps)
- Quality of visualizations (maps and graphs)
- Report and overall documentation of the work (written parts, and how well the used methods have been described)

Take a look of these hints for using markdown:

- `using markdown in Jupyter Notebooks  <http://www.firstpythonnotebook.org/markdown/>`_
- `General Markdown syntax guide <https://guides.github.com/features/mastering-markdown/>`__.

Option 1: Sustainable cities and communities
--------------------------------------------

In this assignment, the aim is to focus on Sustainable Development Goal 11 (Sustainable cities and communities) and create
an analysis workflow in which you:

- fetch the data for given area of interest (choose two areas so that you can compare them),
- conduct the data analysis that aims to provide information related to the given target/indicator (i.e. what is the current state in the area based on the given indicator)
- repeat the analysis workflow for another area of interest (e.g. in another city or neighborhood)
- report your findings with informative maps and graphics as well as written text (think it as a "mini-report")
    - E.g. what does the indicators reveal?
    - How do the areas compare? Are there differences or similarities?

The main idea of the assignment is to calculate a set of metrics / indicators based on openly available data, and to compare the cities/regions based on these measures.
This assignment is not accurately defined, as the idea is to allow you to use your own imagination and interest to explore different datasets and conduct analyses that interest to you,
still providing useful insights about the given indicator in the areas that you picked.

**Suggested topic:**

If you have hard time choosing a target/indicator, we suggest that you focus on target 11.2, which is:

  "By 2030, provide access to safe, affordable, accessible and sustainable transport systems for all, improving road safety, notably by expanding public transport, with special attention to the needs of those in vulnerable situations, women, children, persons with disabilities and older persons."

As a starting point check the more detailed description for the indicator of this target `provided by SDSN <https://indicators.report/targets/11-2/>`__
as well as the `indicator metadata <https://unstats.un.org/sdgs/metadata/files/Metadata-11-02-01.pdf>`__ provided by UN.
From the descriptions you can see that there are three proposed sub-indicators that constitute the indicator 11.2:

1. `Road traffic deaths per 100,000 population <https://indicators.report/indicators/i-25/>`__
2. `Access to all-weather road (% access within [x] km distance to road) <https://indicators.report/indicators/i-58/>`__
3. `Percentage of people within 0.5km of public transit running at least every 20 minutes. <https://indicators.report/indicators/i-67/>`__

Your task is to find relevant information from open data sources (see Data section below, OpenStreetMap is a good place to start!)
and construct metrics for these three sub-indicators **for at least two different regions (cities)** as described in the indicator documentation (above).
In your report, also reflect your thoughts about the suitability of the indicator to understand and measure the progress toward the target
(do you see any issues, or have other comments?). Also reflect how well you were able to construct the indicators based on openly available data
(are there any issues e.g. in terms of data quality?).

Notes
~~~~~

Notice that there are no specific criteria how you should conduct and do the analyses, as they are up to you to decide and figure out.
As said earlier, the main purpose of the final assignment is to demonstrate your analysis skills (as well as writing skills),
so aim to do the work in a way that you feel comfortable with. Remember that getting things done is better than perfect!
Also remember that half of the points come from the report and documentation, hence, we advice you to get the written
parts done as early as possible (at the same time as you proceed). As you might have experienced during this course, the programming parts can take a lot of time,
so putting all your effort and strength to solving the programming parts is not a good strategy.

Option 2: Your own project work
-------------------------------

Another option for the final assignment is to develop your own topic.
Requirement for the work is that it needs to relate to sustainability and you need to apply spatial data science methods in your work.
You can for example choose another SDG target that you analyze if it interests you more than the one described in Option 1 above. In general, your own topic should also contain the same five sections as described in the `final work structure <#final-work-structure>`__.

Feel free to be creative! Your own project might be, for example, related to your thesis or work project.
Remember to describe clearly what you are doing in the final assignment Notebook.
Preferably, present your idea to the course instructors before starting it.

Useful documentation
--------------------

Check these resources that are most likely very useful when doing the final assignment:

- `UN SDG indicators document <https://unstats.un.org/sdgs/indicators/Global%20Indicator%20Framework%20after%202020%20review_Eng.pdf>`__ provides an overview of all SDG goals and indicators to measure the progress.
- `Indicators and Monitoring Framework <https://indicators.report/>`__ website provides more detailed explanation about the methodology, such as providing details how specific indicator should be calculated.
- `Metadata / methods description for all SDG indicators <https://unstats.un.org/sdgs/metadata/files/SDG-indicator-metadata.zip>`__ (downloads a Zip package with the descriptions ~154MB)


Data sources
------------

You can use any (spatial) data that you can find, and generate your own report describing how the cities differ from each other based on different perspectives (see below hints about possible analyses).
You can use any data that is available, for example, from the following sources:

- `OpenSreetMap <www.openstreetmap.org>`__ (streets, buildings, points of interest, public transport stops, etc.) following the approaches learned during this course.
- `PaiTuli <https://paituli.csc.fi/download.html>`__
- `Avoindata.fi service <https://www.avoindata.fi/en>`__
- `Helsinki Region Infoshare <https://hri.fi/en_gb/>`__
- `Open data service of Tampere <https://data.tampere.fi/en_gb/>`__
- `The DataBank of the World Bank <https://databank.worldbank.org/home.aspx>`__
- `European Data portal <https://www.europeandataportal.eu/en>`__
- `Eurostat <https://ec.europa.eu/eurostat/data/database>`__

Data sources are not limited to these, hence you can also use other data from any source that you can find (remember to document where the data is coming from!).

Technical considerations
------------------------

Take care that you:

- Document your analyses well using the Markdown cells and describe 1) what you are doing and 2) what you can see from the data and your results.
- Use informative visualizations:

  - Create maps (static or interactive)
  - Create other kind of graphs (e.g. bar graphs, line graphs, scatter plots etc.)
  - Use subplots that allows to easily compare results side-by-side

- When writing the codes, we highly recommend that you use and write functions for repetitive parts of the code. As a motivation: think that you should repeat your analyses for all cities in Finland, write your codes in a way that this would be possible. Furthermore, we recommend that you save those functions into a separate .py -script file that you import into the Notebook (`see example from Geo-Python Lesson 4 <https://geo-python-site.readthedocs.io/en/latest/notebooks/L4/functions.html#calling-functions-from-a-script-file>`__)

Literature + inspiration
------------------------

You can use the literature provided during the course as inspiration and as a source for information, but please remember
to cite your sources appropriately in your final assignment. Add a reference list to the end of your notebook.