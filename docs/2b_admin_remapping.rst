=============================================
Mapping data to new administrative boundaries
=============================================

The survey was conducted at a time when the Survey Department was restructuring the administrative boundaries of Nepal, as per GoN’s directive of adapting a federal structure of government. As a result, geographical information (Municipalities, VDCs, etc) in the data is based on the older administrative boundaries.

Given the present geopolitical context, it was identified (during the feedback collection exercise in Phase I) that features of the currently existing portal would be more relevant, and useful to government organizations, researchers and general users if they were mapped to the newer, currently existing administrative boundaries.

Challenges
----------

Remapping existing portal data into new admin boundaries requires geographic shapefiles and transformation tables - none of which are publicly available or in possession of the project partners. Therefore, upon the request of NPC, KLL has coordinated directly with the Central Bureau of Statistics (CBS) for necessary shape files and transformation tables.

Current Progress
----------------

**Summary: The administrative remapping exercise has been completed and is now publicly available at https://v1-opendata.klldev.org**

As of June 2018, CBS has already provided KLL with the shape files of new administrative boundaries and the tables for transforming old admin boundaries into new admin boundaries. After veryfing both of these outputs, KLL has successfully completed work around re-generating base analytical tables and statistics for new administrative units. In addition, the citizen facing web portal has also been re-coded to show data segregated by new admin boundaries.

**Methodology**:

At a broad level, the administrative remapping activity requires the following four activities to be carried out:

- **Generating maps for the newer administrative units**: This activity was carried out in close collaboration with CBS, and the final outcome of this exercise are shapefiles that contain:

    - Boundaries for VDCs/Municipalities according to the old structure along with their respective geographical IDs.

    - Boundaries for Gaunpalikas/Nagarpalikas according to the new federal structure along with their respective geographical IDs.

    - Mapping files (in the form of a table) that describe the relation between the IDs as described in 1(a) and 1(b).

- **Remapping data in ODP to new boundaries**: This step involves using the output generated in 1 to regenerate corresponding Ward/Municipality/Gaunpalika IDs in the base dataset.

- **Regenerating statistics displayed in ODP**: This steps involves recalculating all of the statistics present in ODP based on new IDs generated in step 2.

- **Updating the client side application**: This step involves updating the client side application to display statistics calculated in step 3.

  - Update the map based view in “Explore Section” based on new boundaries.

  - Update filters throughout the website based on new administrative structure.


Notes:
__This portal currently serves data for the 11 most earthquake affected districts namely Dolakha, Dhading, Makwanpur, Nuwakot, Gorkha, Okhaldhunga, Sindhupalchowk, Ramechhap, Rasuwa, Sindhuli, and Kavre. Under the federal system, Gorkha is in Province 4, Okhaldhunga is in Province 1 and the rest lie in Province 3.__
