
============================
 Global Coffee Data Standard
============================
This project displays the initial basic common indicators for farm-level coffee sustainability. The common indicators are a result of a collective multi-stakeholder approach on defining key metrics for sustainability performance, based on the Sustainability Progress Framework elaborated under the joint facilitation of the Sustainable Coffee Challenge (SCC) and the Global Coffee Platform (GCP).  COSA – with feedback from the members of a carefully selected global expert committee – have developed and synthesized practical metrics to operationalize the indicators so they can be functional across origins and comparable over time. The approach builds on extensive global experience with sustainability metrics and the expertise of the committee members.

.. contents::
    :depth: 4

**********
1 Metadata
**********
.. topic:: Details:

   **Property name**: metadata

   **Type**: *object*


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-metadata').toggle(300)">Metadata Example Data</button>
    <div id="example-data-metadata" style="display: none;">

.. literalinclude:: _static/example-data/metadata.json
   :linenos:

.. raw:: html

    </div>

1.1 Coffee Dataset Id
^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: globalCoffeeDatasetId

   **Reference**: *global-unique-id.json*


The unique identifier for this dataset. The organisation is responsible for the best-practice values.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/global-unique-id.json"></script>


1.2 Schema version
^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: schemaVersion

   **Type**: *string*

   **Allowed values**: '0.0.5'


**Optional**

The version number of the schema. When not provided the latest version of the schema will be used to validate the dataset.


1.3 Production year
^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: productionYear

   **Type**: *object*


The production year is defined as the end of the last harvest to the end of the corresponding harvest before that (12 month period).


1.3.1 The start of the projection year in YYYYMM
------------------------------------------------
.. topic:: Details:

   **Property name**: start

   **Type**: *integer*

   **Minimum**: *199000*

   **Maximum**: *210000*


1.3.2 The end of the projection year in YYYYMM
----------------------------------------------
.. topic:: Details:

   **Property name**: end

   **Type**: *integer*

   **Minimum**: *199000*

   **Maximum**: *210000*


********
2 Farmer
********
.. topic:: Details:

   **Property name**: farmer

   **Type**: *object*


The farmer characteristics


2.1 General farmer characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: general

   **Type**: *object*


The general farmer characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-farmer-general').toggle(300)">Farmer General Example Data</button>
    <div id="example-data-farmer-general" style="display: none;">

.. literalinclude:: _static/example-data/farmer-general.json
   :linenos:

.. raw:: html

    </div>

2.1.1 Unique ID of the farmer
-----------------------------
.. topic:: Details:

   **Property name**: farmerId

   **Reference**: *global-unique-id.json*


Globally Unique ID of the recording of the farmer at a specific time and by a specific organisation.


Each producer should have a unique ID. Optimally this can be a national ID, but in its absence a buyer ID, project ID or other unique number can serve. It is important to keep in mind that various entities may have access to reported data, so confidential information should not be included in the shared record (e.g. Social Security number).


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/global-unique-id.json"></script>


2.1.2 Name of the farmer
------------------------
.. topic:: Details:

   **Property name**: name

   **Reference**: *name.json*


First and last name(s) of the farmer surveyed should be collected in separate fields/columns to ensure consistency (avoiding confusion between Carlos de la Huerta and De la Huerta, Carlos). Initials should be avoided when possible. In places where farmers use only one name (a family name), that name should be entered as the Last Name and an appropriate prefix or "Farmer" could be entered as the First Name.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/name.json"></script>


2.1.3 The address of the farm
-----------------------------
.. topic:: Details:

   **Property name**: address

   **Reference**: *address.json*


Generally, data should include Country and then State/Department and Municipality/District, unless the address is collected for the sake of auditing. This should be the location of the farm itself (main plot), not the home of the farmer, if different.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/address.json"></script>


2.1.4 Date of birth
-------------------
.. topic:: Details:

   **Property name**: dateOfBirth

   **Type**: *string*

   **Examples**: '2000-08-17', '1973-05-30'

   **Pattern**: *^[12][0-9]{3}-[01][0-9]-[0-3][0-9]$*

.. raw:: html 

   <a href="https://regex101.com/r/SIq25G/1" target="_blank">Pattern validator</a>


Best practice is to use 'Year of Birth' as opposed to age. Age has to be updated annually, but year of birth is the same indefinitely, and can be used to calculate age at any point.


Data point used to understand the relative presence of youth and calculate youth engagement: % of producers in the sustainability program or supply chain 35 years old and under.


2.1.5 Gender
------------
.. topic:: Details:

   **Property name**: gender

   **Type**: *string*

   **Allowed values**: 'M', 'F', 'O', 'NA'


Data point used to understand the relative presence of women and to calculate women's engagement and the outcomes they experience as diverse from men: % of women in the sustainability program or supply chain.


2.1.6 Farm Ids
--------------
.. topic:: Details:

   **Property name**: farmIds

   **Type**: *array*

   **Unique items**: *True*

   **Minimum items**: *1*

   **Array items**: *global-unique-id.json*


Which farms belong to this farmer. At least one is required.


2.1.7 Third-party identifier
----------------------------
.. topic:: Details:

   **Property name**: thirdPartyIds

   **Type**: *array*

   **Unique items**: *True*

   **Array items**: *global-unique-id.json*


When this dataset is reused by another organisation who needs to use their own Global Unique Identifier, the original identifier can be saved here, to track history and origin.


2.2 Social farmer characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: social

   **Type**: *object*


The social farmer characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-farmer-social').toggle(300)">Farmer Social Example Data</button>
    <div id="example-data-farmer-social" style="display: none;">

.. literalinclude:: _static/example-data/farmer-social.json
   :linenos:

.. raw:: html

    </div>

2.2.1 Poverty level
-------------------
.. topic:: Details:

   **Property name**: povertyLevel

   **Reference**: *poverty-level.json*


Comparison of total household revenue to World Bank International Extreme Poverty Line (total divided by # adult individuals in household).


The Monitoring approach is to ask producers the proportion of total household income coming from the sale of coffee (since the coffee revenue amount from the Net Income indicator (Profit) is already known, an estimate of the full household income amount can be derived with that proportion). This allows a good sense of the economic picture on the farm without adding substantial detail to the approach in terms of all household income streams (e.g., sales of other crops or services, income from other businesses, gifts and remittances, etc.) and any associated costs.

The World Bank International Extreme Poverty Line is $1.90 USD per day as of 2015 (https://datahelpdesk.worldbank.org/knowledgebase/articles/906519). Comparison to national poverty lines may be useful for discussion related to one country or domestic policy but that can be calculated separately as needed.

An organisation may choose to use the PPI score evaluation of the propensity of a farmer or community to be poor as another option that can be more relevant in some rural areas and can be calculated separately as needed. Organisations may also choose to participate on this topic in the Living Income Community of Practice.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/poverty-level.json"></script>


2.2.2 Child labor
-----------------
.. topic:: Details:

   **Property name**: childLabor

   **Reference**: *child-labor.json*


The issue of Child Labor is often addressed as a compliance audit question, but it is rarely answered because of the moral hazard (nobody wants to answer that they have child labor). Instead, "children in school at the appropriate grade level" serves to provide a valuable proxy that directly reflects an outcome of child labor and results in a better understanding of the plight of children in a community. Note that in many countries the compulsory school age may be lower than 18, and organisations are welcome to include other age limits in their own analysis of the data, but children in the appropriate grade for their age through 18 serves as an aspirational target. This data can be segmented by gender to get additional insights into the differences in education levels for both boys and girls in a community.


As an additional option, it may be desirable to ask whether young workers (those under age 18) are working in hazardous conditions (applying chemical pesticides, using hazardous machinery, moving excessive weights/loads, etc.)

These concepts are common to many sustainability standards and the approach is built on the ILO standards and the SDGs.

We recognize that child labor can also occur outside the family setting. At this initial stage of common metrics, it is necessary to note that capturing that requires either a labor assessment targeting workers (risky for them, often requires an independent surveyor, and timing is critical) or a risk assessment or data from the wider community (consider costs and comparability). This is an important topic and it is necessary to adequately understand which communities are more prone to this situation, therefore, we propose that it be addressed with different tools than these basic performance indicators developed with the GCP.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/child-labor.json"></script>


2.2.3 Hunger days
-----------------
.. topic:: Details:

   **Property name**: hunger

   **Type**: *integer*

   **Minimum**: *0*


Whether the household was food secure during the last production year (report 0 days of food insecurity--i.e., not skipping meals or significantly reducing food intake because food was not available).


The simple approach depends on asking the producer the number of days during the last production year that any member of household cut food consumption due to lack of food. It is good practice to ask this question in ranges of days to help with farmer recall: 0 days; 1-9 days, 10-19 days; 20-29 days; 30 or more days in the past year. Producers that answer '0 days' are considered to be food secure. Optimally, the approach would also include the months when food insecurity occurred in order to understand the times of year when producers experience more or less food security.

More comprehensive nutritional indicators can be expensive and require significant technical ability, time and resources to carry out effectively, so instead the focus is on days of food insecurity as a proxy. Note that while this survey question is often asked to the head of household, this indicator is best expressed when it includes multiple perspectives in the household. This indicator is an important human development issue and a core indicator for social justice.


******
3 Farm
******
.. topic:: Details:

   **Property name**: farm

   **Type**: *object*


The farm characteristics


3.1 General farm characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: general

   **Type**: *object*


The general farm characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-farm-general').toggle(300)">Farm General Example Data</button>
    <div id="example-data-farm-general" style="display: none;">

.. literalinclude:: _static/example-data/farm-general.json
   :linenos:

.. raw:: html

    </div>

3.1.1 Farm Id
-------------
.. topic:: Details:

   **Property name**: farmId

   **Reference**: *global-unique-id.json*


Globally Unique ID of the recording of the farm at a specific time and by a specific organisation.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/global-unique-id.json"></script>


3.1.2 Farmer Id
---------------
.. topic:: Details:

   **Property name**: farmerId

   **Reference**: *global-unique-id.json*


Globally Unique ID of the farmer of this farm


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/global-unique-id.json"></script>


3.1.3 Location of the farm
--------------------------
.. topic:: Details:

   **Property name**: location

   **Reference**: *farm-location.json*


GPS should be captured for each farm plot if possible. GPS readings should be taken outside of buildings and away from significant tree coverage to avoid interference in the signal. GPS should be captured in the middle of the plot, and/or near the entrance to any main building (if there is one). Where the main residence or other buildings are not located on the farm plot, GPS should be taken in the middle of the plot.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/farm-location.json"></script>


3.1.4 Farm address
------------------
.. topic:: Details:

   **Property name**: address

   **Reference**: *address.json*


This should be the location of the farm itself (main plot), not the home of the farmer, if different.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/address.json"></script>


3.1.5 Total farm size (ha)
--------------------------
.. topic:: Details:

   **Property name**: totalFarmSize

   **Type**: *number*

   **Exclusive minimum**: *0*


Total Farm size refers to total property size, including land used to grow crops, pasture, wooded areas, land covered by buildings, and any other area included in the property.


Best practice is to collect response in any given unit, and then perform conversion to a standard international unit (ha). Data validation should ensure that the total area planted in coffee should be less than the total farm size. It is ok to rely on farmer recall although more rigorous estimates will include GPS or polygonal mapping data. Consider that farms may contain multiple plots (plots are farm land areas that are not connected, or farm areas that are managed differently, or both). Make sure to add all relevant plots managed by members of a household together (that is, the farm area should coincide with the land used to account for the farm cost and revenue data being reported).


3.1.6 Total Area planted in Coffee (ha)
---------------------------------------
.. topic:: Details:

   **Property name**: totalAreaCoffee

   **Type**: *number*

   **Exclusive minimum**: *0*


Sum of coffee farm areas from producers in the sustainability program or supply chain (ha)


Area under coffee production can also be triangulated with other pieces of data collected (e.g., trees planted per unit land (density rate) and/or total number of trees planted).


3.1.7 Third-party identifier
----------------------------
.. topic:: Details:

   **Property name**: thirdPartyIds

   **Type**: *array*

   **Unique items**: *True*

   **Array items**: *global-unique-id.json*


When this dataset is reused by another organisation that needs to use their own Global Unique Identifier, the original identifier can be saved here, to track history and origin.


3.2 Social farm characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: social

   **Type**: *object*


The social farm characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-farm-social').toggle(300)">Farm Social Example Data</button>
    <div id="example-data-farm-social" style="display: none;">

.. literalinclude:: _static/example-data/farm-social.json
   :linenos:

.. raw:: html

    </div>

3.2.1 Labor Practices
---------------------
.. topic:: Details:

   **Property name**: laborPractices

   **Reference**: *labor-practices.json*


% of good labor practices adopted (of those listed). This indicator is applicable where farms rely on hired labor (not labor of household members).


The percent refers to the number of good labor practices from the list that are adopted (meaning that each practice should have a binary response) and change over time is noted by the type and number of practices.

These concepts are common to many sustainability standards and the approach is built on the ILO standards and the SDGs. While there may be moral hazard in asking these questions outright, asking the questions themselves serves to educate the respondent about the norms and aspirations that are part of general good labor practices.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/labor-practices.json"></script>


3.2.2 Wages
-----------
.. topic:: Details:

   **Property name**: wages

   **Reference**: *wages.json*


Daily average earnings for farm labor compared to (rural) minimum wage. Wage is listed and also expressed as a percentage of the rural minimum wage (where that exists), alternately to the national minimum wage.


The approach involves asking for the average daily wage rate paid. If applicable, include wages for coffee production, harvesting, and processing and take an average across all three categories.

Wage is listed and also expressed as a percentage of the rural minimum wage (where that exists), alternately to the national minimum wage.

This approach gives a good sense of worker earnings coming from the most prominent types of labor without needing to detail individual jobs, rates, benefits, etc.

Organisations may wish to participate in working groups to define and measure living wage. There is still no widely used methodology, but the ability to understand whether a worker could survive on the wage earned would be useful for any industry. 


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/wages.json"></script>


3.3 Economic farm characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: economic

   **Type**: *object*


The economic farm characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-farm-economic').toggle(300)">Farm Economic Example Data</button>
    <div id="example-data-farm-economic" style="display: none;">

.. literalinclude:: _static/example-data/farm-economic.json
   :linenos:

.. raw:: html

    </div>

3.3.1 Coffee Profit
-------------------
.. topic:: Details:

   **Property name**: coffeeProfit

   **Type**: *number*

   **Exclusive minimum**: *0*


Total revenue from coffee sales minus total costs for coffee production (Reported in USD/ha of coffee productive area.)


The simple approach (which avoids the additional time and resources necessary for detailed accounting while still providing good results) is to ask for the **total** revenue from sales of coffee as a whole, and subtract main costs. This indicator is reported on a per hectare basis to allow comparability across projects and regions.

This simplified approach does not cover asking the producer about revenue and prices for each transaction or amount sold, nor any premiums or deductions. It also factors in only the main costs in the coffee production system (see Cost of Production indicator below).


3.3.2 Yield / Productivity
--------------------------
.. topic:: Details:

   **Property name**: productivity

   **Reference**: *productivity.json*


kgs of GBE (harvested)/ha of coffee productive area


For general GBE conversion guidance, please see: http://www.thecoffeeguide.org/coffee-guide/world-coffee-trade/conversions-and-statistics/


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/productivity.json"></script>


3.3.3 Cost of Production
------------------------
.. topic:: Details:

   **Property name**: productionCosts

   **Reference**: *production-costs.json*


Costs incurred to produce the coffee during the last production year (calculated per kg of GBE)


The simple approach asks only about the main costs in the production system that typically account for the vast majority of total costs (and the total amount spent on each during the last production year). By focusing on the main costs in a system, this provides a good sense of the economic picture on the farm without adding substantial detail to the approach.

Main costs typically include (at a minimum):

* Fertilizers

* Pesticides

* Hired Labor

* Planting material/ Renovation costs

For those using the Full cost accounting approach the categories are comparable though fewer. The full approach would include: deductions by buyers, rent of land, energy, irrigation, capital assets, cultivation practices, traceability and record keeping, costs of standards or certifications, planting and reforestation costs, training costs, interest on credit, crop insurance, cooperative fees, or the value of unpaid family labor (although any important costs in a system should be captured).

Costs should be associated with the coffee production only (i.e., if labor is hired for multiple crops, only the portion used for coffee production should be included). One way to make sure that costs are correctly associated with the production of the coffee is to ask for the percent of inputs that were used for the coffee.

When calculating costs, include only expenditures coming from the household’s own revenue. If inputs are provided as technical assistance for free or at a subsidized cost on a **persistent**, **substantial**, and **systemic** basis it is recommended to account for the value of the input as a cost in the calculation (at an appropriately determined rate).


This indicator is a Sub-metric for Net Income (or Profit).


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/production-costs.json"></script>


3.3.4 Average Price
-------------------
.. topic:: Details:

   **Property name**: price

   **Reference**: *average-price.json*


Average Price received per kg of coffee (GBE). The simple approach involves asking for the total revenue received from coffee during the last production year as well as the amount sold (and the form). The average price per unit can then be calculated. For multiple sales, calculate the price average of sales


The average price can then be compared to the global reference price (e.g., ICO).

This approach avoids the additional time and resources necessary for detailed accounting and asking about each sale (and the associated premiums, deductions or bonuses) while still providing good results.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/average-price.json"></script>


3.3.5 Sustainable purchases
---------------------------
.. topic:: Details:

   **Property name**: sustainablePurchases

   **Reference**: *sustainable-purchases.json*


The volume of sustainable purchases by the buyer and as a proportion of the total, and change year to year.


Detailed methodology developed by the SPF Working Group (not a farmer level metric).


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/sustainable-purchases.json"></script>


3.4 Environmental farm characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: environmental

   **Type**: *object*


The environmental farm characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-farm-environmental').toggle(300)">Farm Environmental Example Data</button>
    <div id="example-data-farm-environmental" style="display: none;">

.. literalinclude:: _static/example-data/farm-environmental.json
   :linenos:

.. raw:: html

    </div>

3.4.1 Forest and Ecosystem Protection
-------------------------------------
.. topic:: Details:

   **Property name**: forestEcosystemProtection

   **Reference**: *forest-ecosystem-protection.json*


The approach involves asking producers if they converted any natural land (e.g., forest, savanna) to land used for coffee production and how much [both in absolute terms (ha) and relative terms (proportion of the farm)] during the last 5 years.


In addition, overlaying gps coordinates of farms (See GPS Coordinate instructions above) with regional deforestation maps provides more interesting data at a landscape level to understand areas of risk. Note though that usually only a single gps point will exist for many smallholder farms, meaning that there often isn't sufficient information to track the contribution of individual farms to deforestation in most cases. However, even with single gps points, general farming areas prone to deforestation will still be visible.

**Forest and ecosystem protection practices** include: 

1. Reforestation with non-productive trees (i.e., those trees that will not be regularly pruned or removed)

2. Laying land aside (fallow) and/or blocking active use (including hunting).


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/forest-ecosystem-protection.json"></script>


3.4.2 Fertilizer use
--------------------
.. topic:: Details:

   **Property name**: fertilizerUse

   **Type**: *string*

   **Allowed values**: 'Yes', 'No'


Whether a professional assessment or advice was used to determine fertilizer needs on the farm. It does not require in-depth fertilizer information: nutrient amounts, local commercial names, dosage amounts, application rates, etc. 


The simple approach depends on asking the producer about fertilizer use best practices instead of all the individual fertilizer types and amounts they use. Asking if the producer based their fertilizer use on professional advice or assessments is easy to ask in a standardized way globally and can be a proxy for proper fertilization on the farm (there is ample evidence that the correlation between fertilizer use and yields is not as good as prescribed fertilization and yields).

Professional assessments include advice from an extension agent or other sustainability program implementer and NOT input sellers.

This approach does not require in-depth fertilizer information: nutrient amounts, local commercial names, dosage amounts, application rates, etc.


3.4.3 Water Conservation & Contamination Prevention
---------------------------------------------------
.. topic:: Details:

   **Property name**: water

   **Reference**: *water.json*


Water conservation practices include (relevance of individual practices will need to be determined by region):


1. Drip irrigation

2. Water catchments

3. Water-efficient processing

For practices that conserve soil moisture balance and control runoff, please reference the "Soil Conservation" indicator below.

Water contamination prevention measures include the following:

1. Pesticide equipment is cleaned away from natural water bodies

2. Ensuring untreated water from processing does not enter natural water bodies

3. Grazing livestock away from natural water bodies

4. Domestic discharge prevented from entering natural water bodies

These concepts are common to many sustainability standards and the approach is built on FAO Good Agricultural Practices.

Asking about best practice adoption is a standardized way to address this indicator globally without the expensive and technical expertise required to measure water use amounts (and evaluating that in the local context) or taking water samples to evaluate contamination levels and the required protocols for that (taking samples at the appropriate locations and time, factoring in elements that may be beyond an individual producers control, etc.).


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/water.json"></script>


3.4.4 Pest control - hazards
----------------------------
.. topic:: Details:

   **Property name**: pestControl

   **Reference**: *pest-control.json*


**Standard IPM techniques include**:

* Conduct regular visual examinations of the coffee to detect pests and/or diseases

* Use traps, repellants, and natural pesticides

* Create or preserve places (including plant species) for beneficial predators of pests to live

* Maintain written record of pest infestation, treatments, and results

* Plant or preserve species that repel pests of the coffee

* Apply pesticide or kill pests only after identifying the pest and only at the best time in the pest’s life cycle to permanently reduce its population

Banned or hazardous pesticides will be based of the WHO Ia and Ib lists. COSA suggests that over time it will be useful to understand the types and/ or individual banned pesticides being used so that research bodies can develop varietals or take other actions that help prevent the need for their use in the field. This approach does not address proper disposal of pesticide containers.

Pesticides include insecticides, fungicides, rodenticides, nematicides and herbicides.

Focusing on IPM techniques is a globally standardized way to understand pest management best practices without the more costly and time-consuming process of detailing individual pesticides, active ingredients, amount used in local units, etc.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/pest-control.json"></script>


3.4.5 Soil Conservation
-----------------------
.. topic:: Details:

   **Property name**: soilConservation

   **Reference**: *soil-conservation.json*


% of applicable soil conservation practices used on the farm (of those listed)


**Soil conservation measures include**:

1. contour planting, terracing, or soil ridges around trees

2. live fences, hedgerows or buffer zones

3. recycling organic matter and crop waste

4. interplanting, nitrogen fixing plants, cover crops, or mulching

5. check dams, drainage channels or diversion ditches

These concepts are common to many sustainability standards and the approach is built on FAO Good Agricultural Practices.

Asking about best practice adoption is a standardized way to address this indicator globally without the expensive and technical expertise required to measure the actual amount of soil conserved or to do individual soil testing on farms.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/soil-conservation.json"></script>


******
4 Plot
******
.. topic:: Details:

   **Property name**: plot

   **Type**: *object*


The plot characteristics. This is an example of what is possible. The plot property is optional.


4.1 General plot characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: general

   **Type**: *object*


The general plot characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-plot-general').toggle(300)">Plot General Example Data</button>
    <div id="example-data-plot-general" style="display: none;">

.. literalinclude:: _static/example-data/plot-general.json
   :linenos:

.. raw:: html

    </div>

4.1.1 Unique ID of the plot
---------------------------
.. topic:: Details:

   **Property name**: plotId

   **Reference**: *global-unique-id.json*


Globally Unique ID of the recording of the plot at a specific time and by a specific organisation.


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/global-unique-id.json"></script>


4.1.2 Farm ID
-------------
.. topic:: Details:

   **Property name**: farmId

   **Reference**: *global-unique-id.json*


To which farm belongs this plot


.. raw:: html

    <script src="_static/docson/widget.js" data-schema="../schema/global-unique-id.json"></script>


4.1.3 Plot boundary
-------------------
.. topic:: Details:

   **Property name**: boundary


The boundary of the plot


4.1.4 Plot area
---------------
.. topic:: Details:

   **Property name**: area

   **Type**: *number*

   **Minimum**: *0*


Area of the plot


4.1.5 Third-party identifier
----------------------------
.. topic:: Details:

   **Property name**: thirdPartyIds

   **Type**: *array*

   **Unique items**: *True*

   **Array items**: *global-unique-id.json*


When this dataset is reused by another organisation who needs to use their own Global Unique Identifier, the original identifier can be saved here, to track history and origin.


4.2 Economic plot characteristics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. topic:: Details:

   **Property name**: economic

   **Type**: *object*


The economic plot characteristics


.. raw:: html

    <button class="btn btn-example-data" onclick="$('#example-data-plot-economic').toggle(300)">Plot Economic Example Data</button>
    <div id="example-data-plot-economic" style="display: none;">

.. literalinclude:: _static/example-data/plot-economic.json
   :linenos:

.. raw:: html

    </div>

4.2.1 Yield
-----------
.. topic:: Details:

   **Property name**: yield

   **Type**: *number*

   **Minimum**: *0*


kgs of GBE (harvested)


4.2.2 Productivity
------------------
.. topic:: Details:

   **Property name**: productivity

   **Type**: *number*

   **Minimum**: *0*


Total revenue from coffee sales minus total costs for coffee production (Reported in USD/ha of coffee productive area.)


