# Before you Publish your data
## **Produce High-Quality Datasets**
1. **Clean and validate the data**

Cleaning and validating AI training data is another important step in ensuring that the data is accurate, reliable, and useful for machine learning. One of the main benefits of cleaning and validating data is the ability to reduce errors and biases in AI models. If training data contains inaccuracies, incomplete or irrelevant information, or outliers, it can lead to errors in the model development process and the resultant AI applications built on the datasets.

This process includes identifying and removing duplicates, outliers, inaccuracies, and irrelevant data. In this way, researchers can improve the quality and effectiveness of their AI models, ensuring that they are more accurate and reliable. 


2. **Publish in standard, machine-readable formats**

Using a standard, machine-readable format for AI training datasets is crucial for ensuring that the data is easy to use in different contexts and is readily consumed in machine learning pipelines. Machine-readable formats allow data to be read, interpreted, and processed by computers without additional pre-processing by most ML platforms. Using a standardized format also reduces the risk of errors and inconsistencies in data interpretation. Most hosting platforms and ML communities have already established acceptable formats in which the datasets can be published.


```
Acceptable formats for NLP-based data include JSON, CSV, TSV or txt. Each format has its own strengths and is chosen based on the specific requirements of the NLP task e.g. 
For simple sequence, labelling/classification plain text or CSV works.
Plain text - Each sample is one sentence or document in a text file, one per line. 
CSV - Comma or tab-separated values file with one or more text columns for the sample and label columns. 
For complex tasks requiring hierarchies with multiple levels of details, such as annotated corpora with metadata, etc. JSON or XML works better.
JSON - Each sample is a JSON object with text and labels as attributes.
XML - Samples and labels wrapped in XML tags
For sequence labelling tasks such as PoS and named entity recognition, CoNLL format works best
CoNLL - Tab-separated format that includes tokenization with labels for each token.
```


3. **Ensure that annotated data has consistent and accurate labels**

This is important in creating AI models trained on the dataset that are reliable and trustworthy. Use industry standards for annotating data where available, such as those established by the **CoNLL-2003 dataset for named entity recognition tasks.** These standards ensure that labels are consistent and accurate across different datasets and models.

Establish annotation guidelines that define the criteria for labelling data. These guidelines should include specific instructions for annotators, such as examples of correctly labelled data and rules for handling ambiguous cases. 

Validate the labels by comparing the annotations of different annotators or by using a gold standard dataset. This ensures that the labels are consistent and accurate across different annotators and that the annotations meet the required standards.

```
You can use inter-annotator agreement (IAA) measurements to test that different annotators largely agree on the assigned labels
```


4. **Test the data on various models **

Testing AI training data on various models is essential for ensuring that the data is robust and effective for machine learning purposes. By testing data on multiple models, researchers can identify any limitations in the data and improve its quality using the steps above. Additionally, testing on various models can ensure that the data is not biased towards specific models, ensuring that the resulting AI models are reliable and accurate. Where necessary, testing with models also enables you to correctly identify and declare biases in the dataset. Additionally, by testing the training data on multiple models, researchers can ensure that their work is reproducible and promotes transparency and accountability to other machine learning practitioners who will use the training datasets.

```
Test Models can be hosted as notebooks, e.g Jupyter Notebooks, or on Github when publishing your datasets.
This paper on the Kencorpus dataset  provides an example of how test models were as proof of concepts on a Question-Answering subset of the dataset.
```


### **Additional Resources**

**_(Links to the guidance resources by Datawise) _**
