# Produce High-Quality Datasets

## 1. Clean and validate the data

Cleaning and validating AI training data is the first important step in ensuring that the data is accurate, reliable, and useful for machine learning. One of the main benefits of cleaning and validating data is the ability to reduce errors and biases in AI models. If training data contains inaccuracies, incomplete or irrelevant information, or outliers, it can lead to errors in the model development process and the resultant AI applications built on the datasets.

This process includes identifying and removing duplicates, outliers, inaccuracies, and irrelevant data. In this way, researchers can improve the quality and effectiveness of their AI models, ensuring that they are more accurate and reliable. 


## 2. Use established or standardized naming conventions for variables

Use standard vocabularies and ontologies to describe the data and its attributes. This promotes consistency and interoperability across different datasets and makes it easier to combine and analyze data from multiple sources, as variables with the same name have the same meaning and interpretation. Using descriptive names makes the dataset contents and tasks clear without needing to consult external documentation. Research similar datasets published and where appropriate use similar naming conventions for your variables. Ensuring that training datasets are interoperable is essential for enabling data sharing and reuse across different platforms and applications. Interoperable datasets can be easily integrated with other datasets, making it possible to perform cross-dataset analysis and training of AI models. 

---

!!! Note ""
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




## 3. Publish in standard, machine-readable formats

Using a standard, machine-readable format for AI training datasets is crucial for ensuring that the data is easy to use in different contexts and is readily consumed in machine learning pipelines. Machine-readable formats allow data to be read, interpreted, and processed by computers without additional pre-processing by most ML platforms. Using a standardized format also reduces the risk of errors and inconsistencies in data interpretation. Most hosting platforms and ML communities have already established acceptable formats in which the datasets can be published.


---

!!! Example

    Acceptable formats for NLP-based data include JSON, CSV, TSV or txt. Each format has its own strengths and is chosen based on the specific requirements of the NLP task e.g.

    - For simple sequence, labelling/classification plain text or CSV works.
        * Plain text - Each sample is one sentence or document in a text file, one per line. 
        * CSV - Comma or tab-separated values file with one or more text columns for the sample and label columns. 

    - For complex tasks requiring hierarchies with multiple levels of details, such as annotated corpora with metadata, etc. JSON or XML works better.
        * JSON - Each sample is a JSON object with text and labels as attributes.
        * XML - Samples and labels wrapped in XML tags

            
    - For sequence labelling tasks such as PoS and named entity recognition, CoNLL format works best
        * CoNLL - Tab-separated format that includes tokenization with labels for each token.



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



### Additional Resources

**_(Links to the guidance resources by Datawise) _**


