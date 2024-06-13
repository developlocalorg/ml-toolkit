# Produce High-Quality Datasets

## 1. Clean and validate the data

Cleaning and validating AI training data is the first important step in ensuring that the data is accurate, reliable, and useful for machine learning. One of the main benefits of cleaning and validating data is the ability to reduce errors and biases in AI models. If training data contains inaccuracies, incomplete or irrelevant information, or outliers, it can lead to errors in the model development process and the resultant AI applications built on the datasets.

This process includes identifying and removing duplicates, outliers, inaccuracies, and irrelevant data. In this way, researchers can improve the quality and effectiveness of their AI models, ensuring that they are more accurate and reliable. 

---
!!! Note ""
    Suggested steps to clean and validate your datasets include:
    
     1. **De-duplication**: Remove duplicate records to ensure each entity or occurence is represented only once.
     2. **Handling Missing Data**: Use imputation techniques or interpolation to fill in missing values. Alternatively, completely remove records with excessive missing data.
     3. **Standardization**: Convert your data or variables within the dataset to a common format or unit for consistency.
     4. **Removing Noise**: Filter out irrelevant data points that do not contribute to meaningful analysis.
     5. **Outlier Detection**: Identify and correct or remove outliers that may be due to data entry errors or device malfunctions (in the case of images, these could be photos with occlusion).
     6. **Cross-Validation**: Validate data against other reliable sources or benchmark datasets to ensure accuracy and consistency.
     7. **Consistency Checks**: Ensuring data consistency across different fields, records, and over time.
     8. **Expert Review**: Co-opt domain experts to review the data for accuracy, relevancy, and plausibility.
     9. **Ground-Truthing**: Validate data against ground-truth data collected through field surveys or manual annotations.
     10. **Temporal and Spatial Consistency**: If relevant, check for consistency of values over time and across different spatial locations.
     11 **Image Quality**: As needed, ensure sufficient overlap between consecutive images (e.g. in the case of satellite imagery) to enable accurate stitching and depth perception while also ensuring that the area of interest is completely.
     11. **Model Validation**: Validating data by running models and comparing the output with observed or historical data.



## 2. Use established or standardized naming conventions for variables

Use standard vocabularies and ontologies to describe the data and its attributes. This promotes consistency and interoperability across different datasets and makes it easier to combine and analyze data from multiple sources, as variables with the same name have the same meaning and interpretation. Using descriptive names makes the dataset contents and tasks clear without needing to consult external documentation. Research similar datasets published and where appropriate use similar naming conventions for your variables. Ensuring that training datasets are interoperable is essential for enabling data sharing and reuse across different platforms and applications. Interoperable datasets can be easily integrated with other datasets, making it possible to perform cross-dataset analysis and training of AI models. 

---

!!! Note ""

    === "NLP"

        Some common variable naming conventions for NLP datasets include: 

        * **text** - Raw input text
        * **context** - Surrounding text 
        * **document** - Long documents
        * **question** - Question text
        * **answer** - Answer text
        * **label** - Classification labels  
        * **sentiment** - Sentiment polarity labels 
        * **entities** - Named entities
        * **relations** - Relations
        * **id** - Unique identifier
        * **topic** - Document topic
        * **annotations** - Additional annotations

    === "Health"
    
        Typically health datasets, especially image-based datasets produced for AI tend to be multidimensional e.g. imaging datasets like MRI and X-ray that include 2D and 3D images,time-series data, and multi-parametric data that combine different types of health measurements. The effectiveness of clinical data standards is determined by the semantic interoperability.
        
         Some common variable naming conventions for these datasets include: 
        
        * **Study and Series Identifiers**: Each imaging study and series within it typically has a unique identifier.
        * **Patient Identifiers**: Patient-specific information like ID, age, sex, and sometimes anonymized names.
        * **Date and Time Stamps**: Indicating when the study was conducted.
        * **Modality**: Type of imaging (e.g., MRI, CT, X-ray).
        * **Body Part Examined**: The anatomical region imaged.
        * **View Position**: For radiographs, the view or angle of the image (e.g., AP for anterior-posterior).
        * **Imaging Parameters**: Such as slice thickness, echo time, repetition time in MRI.
        * **Conventional Disease Names**: Derived from the International Classification of Diseases(ICD)
        
        Additionally you may want to consider using a file naming conventions such as a combination of patient identifiers, study date, modality, and other relevant metadata for interoperability, ease of sorting and retreiving data files.

    === "Climate/Agriculture/Energy"

        Datasets produced for climate, energy, and agriculture contexts, despite their distinct applications, share several commonalities (therefore, examples are grouped for these domains): 
        
        * They have both **temporal and spatial** dimensions: i.e. over time and over various locations e.g. climate datasets include weather patterns over time, energy datasets may track consumption or production across different regions over periods, and agriculture datasets can show crop yields or soil conditions across various locations and seasons.
        
        * They are **multivariate** in nature: For climate, this could be temperature, humidity, precipitation, and wind speed; for energy, it might include consumption levels, production sources, and energy prices; in agriculture, variables could include crop type, yield, soil quality, and weather conditions.

        * They have common ontologies for weather, agriculture, ecology which provides semantic interoperability across datasets.



## 3. Publish in standard, machine-readable formats

Using a standard, machine-readable format for AI training datasets is crucial for ensuring that the data is easy to use in different contexts and is readily consumed in machine learning pipelines. Machine-readable formats allow data to be read, interpreted, and processed by computers without additional pre-processing by most ML platforms. Using a standardized format also reduces the risk of errors and inconsistencies in data interpretation. Most hosting platforms and ML communities have already established acceptable formats in which the datasets can be published.


---

!!! Example
    === "NLP"

        Acceptable formats for NLP-based data include JSON, CSV, TSV or txt. Each format has its own strengths and is chosen based on the specific requirements of the NLP task e.g.

        - For simple sequence, labelling/classification plain text or CSV works.
            * Plain text - Each sample is one sentence or document in a text file, one per line. 
            * CSV - Comma or tab-separated values file with one or more text columns for the sample and label columns. 

        - For complex tasks requiring hierarchies with multiple levels of details, such as annotated corpora with metadata, etc. JSON or XML works better.
            * JSON - Each sample is a JSON object with text and labels as attributes.
            * XML - Samples and labels wrapped in XML tags

        - For sequence labelling tasks such as PoS and named entity recognition, CoNLL format works best
            * CoNLL - Tab-separated format that includes tokenization with labels for each token.

    === "Health"

        **DICOM (Digital Imaging and Communications in Medicine)** is the most widely used standard for storing and transmitting medical imaging information and related data. DICOM standardizes the formats for medical images, the protocols for imaging techniques (such as MRI and X-rays), and other vital data related to medical imaging.
        
        For associated non-imaging data (like clinical data), formats like CSV, JSON, or XML might be used, with standardized field names and structures.

    === "Climate/Agriculture/Energy"
    
        Examples of naming conventions and schemas to observe include:
        
        1. **Descriptive Names that include Time Frames**: Use descriptive names that clearly indicate the dataset's content. For example, `GlobalSurfaceTemperature_1980_2020`.
        2. **Standard Abbreviations**: Utilize standard abbreviations (e.g., `temp` for temperature, `prod` for production) and indicate units of measurement e.g. Celsius (`temp_C`) or energy in megawatts (`energy_MW`).
        3. ** Spatial Resolution**: If applicable, include spatial resolution, e.g., `AirQuality_10kmGrid`.
        4. **Standardized  Names** for variables, e.g., using `date` for dates, `latitude` and `longitude` for geographical coordinates.

## 4. Ensure that annotated data has consistent and accurate labels

This is important in creating AI models trained on the dataset that are reliable and trustworthy. Use industry standards for annotating data where available, such as those established by the **CoNLL-2003 dataset for named entity recognition tasks.** These standards ensure that labels are consistent and accurate across different datasets and models.

Establish annotation guidelines that define the criteria for labelling data. These guidelines should include specific instructions for annotators, such as examples of correctly labelled data and rules for handling ambiguous cases. 

Validate the labels by comparing the annotations of different annotators or by using a gold standard dataset. This ensures that the labels are consistent and accurate across different annotators and that the annotations meet the required standards.

---

!!! tip

    You can use inter-annotator agreement (IAA) measurements to test that different annotators largely agree on the assigned labels



## 5. Test the data on various models


Testing AI training data on various models is essential for ensuring that the data is robust and effective for machine learning purposes. By testing data on multiple models, researchers can identify any limitations in the data and improve its quality using the steps above. Additionally, testing on various models can ensure that the data is not biased towards specific models, ensuring that the resulting AI models are reliable and accurate. Where necessary, testing with models also enables you to correctly identify and declare biases in the dataset. Additionally, by testing the training data on multiple models, researchers can ensure that their work is reproducible and promotes transparency and accountability to other machine learning practitioners who will use the training datasets.

!!! Example

    Test Models can be hosted as notebooks, e.g Jupyter Notebooks, or on Github when publishing your datasets.

    [This paper on the Kencorpus dataset](https://dl.acm.org/doi/full/10.1145/3578553)  provides an example of how test models were as proof of concepts on a Question-Answering subset of the dataset.




