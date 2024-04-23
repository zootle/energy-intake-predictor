![Predicting Energy Intake from Recipe Ingredients](assets/images/github-header.png "Predicting Energy Intake from Recipe Ingredients")

# Datasheet for Predicting Energy Intake from Recipe Ingredients

Please find information on the McCance and Widdowson's Composition of Foods Integrated Dataset (CoFID) dataset included in this project.

## Motivation

**For what purpose was the dataset created?**

The McCance and Widdowson's Composition of Foods Integrated Dataset (CoFID) 2021 version was created to support the National Diet and Nutrition Survey and for ongoing nutrient analysis of foods commonly consumed in the UK. The specific goals of the dataset include:

- Support Nutritional Research: The dataset serves as a foundational resource for researchers studying diet, nutrition, and their impacts on health. It allows scientists to conduct studies on dietary intake, nutrient analysis, and the role of diet in disease prevention and management.
- Guide Public Health Policy: By offering comprehensive data on the nutritional content of foods, the dataset aids policymakers in designing public health initiatives and nutritional guidelines. This includes efforts to combat nutritional deficiencies, manage obesity rates, and promote overall public health through better dietary choices.
- Educate and Inform: CoFID is a resource for dietitians, nutritionists, and educators who need accurate information to advise patients, clients, and students about healthy eating practices. It supports dietary planning and helps in creating educational materials that promote nutrition awareness.
- Regulate Food Industry Practices: The dataset is used by the food industry for product development, nutritional labelling, and to ensure compliance with government regulations regarding food nutrition content and claims. This helps consumers make informed choices and promotes transparency in the food market.
- Support Dietary Assessment Tools: It provides the data backbone for software and tools used in dietary assessment and planning. Health professionals use these tools to analyse dietary intake and offer personalised nutritional advice based on scientifically validated data.

The dataset promotes better understanding of nutrition and its effects on health, which can lead to improved dietary choices and health outcomes.

**Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organisation)?**

Initially, the work on this dataset began with Dr. Robert McCance and Dr. Elsie Widdowson, who were pioneering researchers in nutrition science. Their work has been continued and expanded under the auspices of various public health and government entities.

The dataset was created by Public Health England (PHE) with significant contributions from:
- Mark Roe and Rachel Berry on behalf of Quadram Institute Bioscience.
- Sakhi Dodhia, Melanie Farron-Wilson, Joanne McArdle, Danielle Weiner, Gillian Swan and Mark Bush on behalf of Public Health England.
- Hannah Koffman and Debby Webb on behalf of the Department of Health and Social Care.

Data from this work, and complementary data from other sources are published as McCance and Widdowson’s ‘The Composition of Foods’ – the UK food composition tables.

**Who funded the creation of the dataset?**

Key funding and support for the dataset have historically come from:

- Public Health England (PHE): Before it was restructured, PHE was directly involved in the updating and maintenance of the dataset.
- The Department of Health and Social Care (DHSC): As the overseeing body for PHE and its successor organisations, the DHSC has provided both funding and strategic direction for public health projects including nutritional data research.
- UK Food Standards Agency: In some editions and updates, the Food Standards Agency has collaborated or contributed, especially in aspects related to food safety and standards.
 
## Composition

**What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?**

The instances in the McCance and Widdowson's Composition of Foods Integrated Dataset (CoFID) represent individual food items. Each instance in the dataset provides detailed nutritional information about a specific food item commonly consumed in the UK. This information typically includes:

- Macronutrients: Such as fats, proteins, and carbohydrates, including details on sugars and dietary fibre.
- Micronutrients: Including vitamins and minerals.
- Other Nutritional Components: Such as water content, alcohol, organic acids, and cholesterol.

Each food item in the dataset is analysed and recorded with comprehensive details about its nutritional composition. The purpose of these entries is to provide a reliable source of nutritional data for use in research, dietary planning, public health policymaking, and educational purposes. The dataset does not contain documents, photos, people, or countries but focuses solely on the nutritional aspects of food items.

It is made available in an MS Excel Spreadsheet, named McCance and Widdowson's composition of foods integrated dataset (Ref: PHE publications gateway number: GW-2010, MS Excel Spreadsheet, 4.42 MB)

**How many instances of each type are there?**

For each food ingredient there are the following tables of data related to specific nutritional research.

- Factors 
- Proximates
- Inorganics
- Vitamins
- Vitamin Fractions
- Saturated fatty acids per 100g fatty acids
- Saturated fatty acids per 100g food
- Monounsaturated fatty acids per 100g fatty acids
- Monounsaturated fatty acids per 100g food
- Polyunsaturated fatty acids per 100g fatty acids
- Polyunsaturated fatty acids per 100g food
- Phytosterols
- Organic acids

A user guide and a further dataset of old ingredients is supplied.

These are the two accompanying documents:
- McCance and Widdowson’s The Composition of Foods Integrated Dataset 2021: user guide (Ref: PHE publications gateway number: GW-2010, PDF, 759 KB, 37 pages)
- McCance and Widdowson's composition of foods: old foods (Ref: PHE publications gateway number: GW-2010, MS Excel Spreadsheet, 634 KB)

An option is available to request the dataset in an accessible formats for use with assistive technology.

**Is there any missing data?**

The extent and nature of missing data can vary depending on several factors, such as the availability of information, changes in food products, and the methods used to analyse food components. 

Here are some typical scenarios where the data appears to be missing:

- Limited Data on Certain Nutrients: Some nutrients might be harder to analyse or less frequently analysed due to the cost, complexity of analysis, or because they are not a mandatory part of nutritional labelling requirements.
- Newly Introduced Foods: For new food products or less common ingredients, comprehensive nutritional data might not be immediately available.
- Variability in Food Items: Natural products like fruits and vegetables can show significant variability in nutrient content depending on factors like seasonality, cultivation methods, and geographic origin. Sometimes, it might be challenging to provide precise nutrient values for every instance.
- Updates and Revisions: As food compositions change due to factors like reformulations or new agricultural practices, previously collected data might become outdated, and there may be a lag before the dataset is updated.

Within the main elements used in this project there is no missing data in the file.

**Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?**

It is made available to the public and considered free from issues related to confidentiality or privacy.

## Collection process

**How was the data acquired?**

The analytical survey reports on how the data was acquired is available from [Food & Nutrition National Bioscience Research Infrastructure (NBRI)](https://fnnbri.quadram.ac.uk).

The dataset was acquired via download from the Gov.uk website where it is publicly available as guidance. It can be downloaded [here](https://www.gov.uk/government/publications/composition-of-foods-integrated-dataset-cofid).

The data for Food Groups was extracted from the User Guide alongside the Proximates and Vitamins, which have all been merged to form a singular dataset suitable for purpose.

**If the data is a sample of a larger subset, what was the sampling strategy?**

A smaller subset has been sampled for use in this project through exporting MS Excel sheets to CSV format for importing into the project.

**Over what time frame was the data collected?**

The original work by Dr. Robert McCance and Dr. Elsie Widdowson, which laid the foundation for this dataset, began in the 1940s. Since then, the dataset has been updated and expanded regularly to reflect changes in food composition, new foods entering the market, and advances in nutritional science.

- Initial Editions: The earliest data collection started in the 1940s and the first comprehensive edition was published in 1940.
- Subsequent Updates: There have been multiple updates and revisions, with major editions released in the 1960s, 1980s, 1990s, and more recent updates in the 2000s and 2010s.

The Composition of Foods series of publications in book form are listed below:

- Cereals and Cereal Products, supplement (1988)
- Milk Products and Eggs, supplement (1989)
- Vegetables, Herbs and Spices, supplement (1991)
- Fifth Summary Edition (1991)
- Fruit and Nuts, supplement (1992)
- Vegetable Dishes, supplement (1992)
- Fish and Fish Products, supplement (1993)
- Miscellaneous Foods, supplement (1994)
- Meat, Poultry and Game, supplement (1995)
- Meat Products and Dishes, supplement (1996)
- Fatty Acids, supplement (1998)
- Sixth Summary Edition (2002)
- Seventh Summary Edition (2015)

## Pre-processing, cleaning and labelling

**Was any pre-processing/cleaning/labelling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the remaining questions in this section.**

Yes, pre-processing, cleaning, and labelling has been undertaken to ensure the accuracy, consistency, and usability of the dataset. Here are some steps that might have been involved:

- Cleaning and Standardisation: Outliers that are significantly different from other observations and likely due to errors in data entry or measurement might be removed or corrected. Measurements have been aligned in grams, milligrams, etc.
- Labelling:  Foods have been grouped into categories (e.g., fruits, vegetables, meats) to facilitate analysis and usage.
- Data Formatting: Organising the data into a format that is easy to access and analyse, such as tables with clearly defined columns for each nutrient.
- Handling Missing Data: Missing values might have been handled by various imputation techniques where values are estimated based on other available data.

**Was the “raw” data saved in addition to the pre-processed/cleaned/labelled data (e.g., to support unanticipated future uses)?**

The specific data is not explicitly detailed in publicly available information, however in most scientific and nutritional databases, especially those used for ongoing research and public health monitoring, it is common practice to retain raw data. 
 
## Uses

**What other tasks could the dataset be used for?**

There is significant potential to use the data for Nutritional Research and Education, Dietary Planning and Assessment, Public Health Policy and within the Food Industry for managing nutrient and dietary information.

**Is there anything about the composition of the dataset or the way it was collected and pre-processed/cleaned/labelled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms?**

The dataset is a highly regarded source for nutritional data, but like any dataset, there are aspects of its composition, collection, and pre-processing that users should be aware. Here are some potential concerns:

- **Representativeness and Bias** - The dataset contains is focused on the UK, so is highly representative of that demographic and excludes dietary advice for those consuming non-Western diets. It is therefore culturally biased and consideration would be needed to supplement the dataset with additional regions and cultures for more broad applicability.
- **Outdated information** - Nutritional data can become outdated as food manufacturing processes and ingredients change over time.
- **Methodology** - Variations in how food components are measured (e.g., preparation methods, analytical techniques) can lead to inconsistencies or inaccuracies in the data.
- **Generalisation** - Misinterpretation of the data can occur if users generalise findings to populations or conditions outside the dataset’s scope, leading to nutritional misguidance or health risks.
- **Financial Risks** - Inaccurate data could lead to financial harm if used to formulate products, influence stock control, or guide business decisions in the food industry.

To mitigate these issues it could be prudent to consult researchers and practitioners to consider suitability for the demographic, check for regular updates, verify the data through multiple sources, pilot test any dependant decision-making, consider the methodologies for data collection more closely and determine whether any bias might have ethical considerations.

**Are there tasks for which the dataset should not be used? If so, please provide a description.**

While the dataset is a valuable resource for many nutritional and food-related tasks, there are certain applications for which it may not be appropriate or reliable:

- **Clinical or Medical Diagnoses** - using it to directly support medical diagnoses or therapeutic interventions without considering individual patient conditions, medication interactions, and specific nutrient absorption rates can be misleading and potentially harmful.
- **Ethnic or Regional Dietary Analysis** - Given the dataset focuses on the UK, it might not adequately represent the diversity of foods consumed globally, particularly those specific to non-Western diets or regional specialties not widely consumed in the UK.
- **Forecasting Food Trends or Consumption Patterns** - While the dataset provides comprehensive nutritional information, it does not contain data on consumption patterns, consumer behaviour, or trend analysis, which are essential for forecasting in the food industry or market research.
- **Socioeconomic Studies Involving Food Security** - The dataset does not include information about food costs, accessibility, or socioeconomic factors affecting food choices, which are crucial for studies on food security and socioeconomic impacts on diet.
- **Legal Compliance and Food Labelling Outside the UK** - Nutritional standards and labelling requirements can vary significantly by country, where it might not meet local regulatory requirements.

## Distribution

**How has the dataset already been distributed?**

The dataset has been widely updated over many years. The Composition of Foods series of publications in book form are listed below:

- Cereals and Cereal Products, supplement (1988)
- Milk Products and Eggs, supplement (1989)
- Vegetables, Herbs and Spices, supplement (1991)
- Fifth Summary Edition (1991)
- Fruit and Nuts, supplement (1992)
- Vegetable Dishes, supplement (1992)
- Fish and Fish Products, supplement (1993)
- Miscellaneous Foods, supplement (1994)
- Meat, Poultry and Game, supplement (1995)
- Meat Products and Dishes, supplement (1996)
- Fatty Acids, supplement (1998)
- Sixth Summary Edition (2002)
- Seventh Summary Edition (2015)

**Is it subject to any copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?**

The data is available under [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/). This license allows users to copy, modify, distribute, and use the data freely for commercial or non-commercial purposes, provided they attribute the source as specified by the terms of the licence.

## Maintenance

**Who maintains the dataset?**

The McCance and Widdowson's Composition of Foods Integrated Dataset (CoFID) is maintained by Public Health England (PHE), which, following organisational changes, has now become part of the UK Health Security Agency and the Office for Health Improvement and Disparities. These agencies are responsible for updating and ensuring the accuracy of the dataset, as well as for publishing new editions and managing the dissemination of the data.

