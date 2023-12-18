Maintaining detailed documentation, including data provenance, annotation guidelines, and any preprocessing steps shows transparency about data sourcing, annotation methodologies and the intended use of the dataset. The following are suggested methods of dataset documentation:



## 1. Create a data sheet 

Creating a data fact sheet is an important step in ensuring that AI training datasets are transparent and trustworthy. The data sheet can include the following components:


* **A comprehensive description of the data itself**: This should include descriptions of what fields/variables the dataset contains.
* **A description of the provenance of the data**: includes information about the source of the data, sampling methodology, data collection instruments and protocols, and any relevant information about the data collection process. 
* **A description of the data cleaning and preprocessing steps** e.g. if duplicates were removed, outliers were corrected, or missing values were imputed, provide details about these steps and their rationale.
* **Information about any annotations or labels**: This includes information about any annotations or labels that were applied to the data, including information about the labelling process, any standards or guidelines used, and the accuracy or reliability of the labels.
* **Relevant metadata**: This includes catalogue information about the dataset’s origin, purpose, time of creation, creator, formats, file size, and any other relevant standards used that can help users understand and work with the data. This should also include the version of the dataset if various iterations of the dataset are to be published.
* **Contact information for the data owner** in case users need clarification or further information about the data.




---

!!! tip
    Datasheets are useful tools for documenting the datasets used for training and evaluating machine learning models. Datasheets contain questions about dataset motivation, composition, collection, pre-processing, labelling, intended uses, distribution, and maintenance. The following is a good template for dataset documentation and an example in use: 

    [**Datasheet for datasets**](https://arxiv.org/pdf/1803.09010.pdf)

    [**Datasheets: Multimodal datasets for Bemba Language**](https://github.com/csikasote/bigc/blob/main/Datasheet_for_Dataset_DRAFT.pdf)
    
    ---
    Documenting metadata in standardised metadata formats and schemas is crucial for interoperability. The Dublin Core is a good standard to use. It consists of a set of vocabulary terms used to describe web resources such as video, images, web pages, and, importantly, datasets. It includes 15 core elements like title, creator, subject, description, and more. Applying Dublin Core standards to your dataset ensures that the basic and essential metadata is captured in a standardized way.




## 2. Document any models used to augment or annotate the data

If using a model to augment or annotate the data, it is important to use explainable methods and document the intended use cases, the data, model inputs, and the accuracy of the model to make it easy to reproduce the results. 

Document the original data and inputs used to train the model, including any preprocessing steps or transformations that were performed. Include documentation of any parameters or hyperparameters that were set. This helps to ensure that this augmentation process can be easily reproduced. It is also important to include the accuracy of the model and provide information about any metrics or evaluation techniques used to measure model performance. 

Document the code for the test models as well as all the necessary dependencies for the code to run to make it easier for other researchers to replicate your setup. Sharing the models on **Jupyter notebooks or on Github** can help ensure your models are reproducible.



## 3. Version the dataset 

Versioning the AI training dataset enables other researchers to track changes to the dataset, roll back to previous versions if necessary, and maintain consistency and reliability in the data used for analysis. Using a version control system such as Git enables you to track each new change or update to the dataset. Each update to the dataset should include a description of the changes made, such as adding new data, removing duplicates, or modifying annotations. If you have variations to your datasets for different purposes, it is important to also tag each version of the dataset e.g. if used for specific experiments or publications. This makes it easy to identify specific versions of the dataset that were used for different purposes.

