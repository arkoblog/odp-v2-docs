================================
Portal re-design and development
================================

The following sections provides an outline of key activities with regards to portal re-design and development.

PDF Report Generator
^^^^^^^^^^^^^^^^^^^^

Local government representatives, who took part in the Focus Group Discussions, mentioned that the usefulness of printed documents are still very high, i.e. people prefer to have hard copies of the data. Thus, they have recommended an on-site ability to generate pdf version of
the visualizations on the GENERATE section.

**Progress**

- A basic outline for the proposed PDF report has been developed. This can be found `here.  <https://drive.google.com/file/d/1ZvcWvISEYpv2KDNIVVG42Vs5mCisRCXD/view?usp=sharing>`_
- Work on generating this PDF on-the-fly from the NHRP front-end is currently ongoing.

**To-dos**

- The generated PDF will be reviewed and reformatted to make it more user friendly. (ongoing)
- The PDF generation feature will be migrated to the live website. (ongoing)

**Notes**

- The team has opted to use a table-based representation (with some bar chart components, for distribution charts) in the generated PDF. This was done in order to:
  - Minimize information loss, arising from representation of data through charts
  - Make sure users are interacting with data in a format that is familiar to them (table are ubiquitous).
  - Avoid any possible misinterpretation that may arise from reading charts.
- A single Sankey chart has been translated to three tables:
  - A table showing the distribution of resource use before the earthquake,
  - A table showing the distribution of resource use after the earthquake,
  - A table showing the distribution of shifts among resources.

Dual Language Feature
^^^^^^^^^^^^^^^^^^^^^

Since one of the primary purposes of this portal is to increase the usability of its data, making this portal available in English as well as Nepali will make it more suitable to a wider range of audience. This dual language requirement was raised, especially by the central and local governments’ officials.

**Progress**

- Creation of locale variables for storing English and Nepali text is complete.
- Draft translation of all textual content (into Nepali), and linking them to their corresponding locale variables is also complete.
- Incorporation of a language switch button on the ODP front-end is also complete.

**To-dos**

- Review translations for correctness and accuracy. (ongoing)
- Review UI elements based on UI changes identified as part of the wire-framing exercise.

API Development
^^^^^^^^^^^^^^^
With an API in place, third-party applications (such as other websites, portals, visualizations, etc.) will be able to fetch the portal data directly via using web URLs (Universal Resource Locators). In other words, APIs will allow other applications to ‘talk’ to our portal directly.

**Progress**

- Two independent APIs: api/crosstabs and api/distributions have been developed for facilitating comparison across geographies and deep-diving within a geography respectively.
  - This involved the generation of base data-sets that will be used by this API
- Documentation for making use of these APIs, such as the parameters they take, sample queries and responses, is ongoing, and can be found here: eq2015.npc.gov.np/docs


**To-dos**

- Test these APIs using standard JavaScript libraries, and make appropriate changes to the API and/or base data-sets. (ongoing)


Improvement of user experience (UX) and user interface (UI) elements
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Part of Phase II involved a thorough  evaluation of the existing user interface, with a goal of identifying and assessing user experience problems that currently exist in the portal. A thorough heuristic evaluation of the current existing portal was carried out across the following three dimensions:

  1. Learn-ability: This refers to an assessment of how easy or difficult it is for identified user groups to learn how to use the system.
  2. Efficiency: This refers to an assessment of how quickly a user can arrive at what he wants from the system
  3. Safety: This refers to an assessment of error prone areas of the interface.


**Progress**

- New project wire-frames with changes based on learnings from the heuristic evaluation exercise have been designed.
- Based on this, changes to the application front-end is currently underway.


Incorporation of Original Survey Questionnaire
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

During interviews with potential stakeholders, it was found that experts are often skeptical about data received from external sources. It was suggested that having the original survey questionnaire available on the portal would help them understand the overall context and hence build confidence the data.

**Progress**

- Wire-frame has been updated to include survey questionnaire. Changes to the UI is ongoing


Integration (if possible) of location codes used by other data sources
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The KLL team sought the advice of experts from the Central Bureau of Statistics and Survey department regarding commonly adopted administrative codes:

 - CBS and Survey Department came to the conclusion that the usage of HLCIT codes and OCHA codes will decrease with as both HLCIT  (High Level Commission for Information Technology) OCHA has stopped their operations in Nepal, and it isn’t likely that codes will be available for the newer administrative units.
 - Upon meeting employees from the Geographic Information and Infrastructure Division of the Survey Department, KLL learnt that survey department does not have a standardized geographic coding system. Even when sharing/selling data, the department usually provides shapefiles without an ID column, and areas are identified by their names.
 - The survey department mentioned that “they need to adapt” the coding system adopted by CBS, which is the same as what has been used in our website.

Based on these learnings, we have decided not to go ahead with integrating any other location codes in the system.
