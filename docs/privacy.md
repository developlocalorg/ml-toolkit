Privacy-preserving techniques are essential when publishing training datasets in open formats, as they help protect the sensitive information of individuals in the dataset. Several techniques can be employed to ensure privacy while maintaining the utility of the data for research and development purposes as shown in the examples below.

---

!!! Example ""

    === "NLP"

        The technique employed is highly dependent on the NLP task intended for the datasets e.g. carrying out Name Entity Recognition (NER) tasks to categorise the entities appropriately then can eliminate Nouns such as Personally-Identifying Information as needed. It might be helpful to consider leaving the tokenized entities in the datasets for various use cases.

        Other techniques useful for NLP dataset anonymization include:

        * **Noise Addition**: Randomly swap words/characters with plausible alternatives using rules or language models. Maintains general statistics while obfuscating details.
        * **K-Anonymity Filtering**: Keep sentences that occur a minimum number of times k reducing the chance of identifying rare sentences.
        * **Differential Privacy**: Allows the performance of aggregate analytics over textual data while preserving individual privacy and works by adding calculated noise to aggregated statistics like word frequencies, co-occurrence counts etc.
        * **Synthetic Data Generation**: This technique involves using algorithms to generate new textual data that can mimic human language patterns.

    === "Agriculture"

        In the case of geospatial and earth observation data, you can consider privacy-preserving mechanisms for AI training datasets that contain sensitive information e.g. farm boundaries including:
        
        * **Generalization**: Aggreate and replace individual farm coordinates with regions (e.g.use of administrative zones such as adm3 typically used for wards/divisions).
        * **Geospatial obfuscation and differential privacy**: Include random/controlleed noise to location data while maintaining statistical properties or use bounding boxes instead of precise farm polygons.

    === "Health"
    
        Anonymising health data is a delicate balance between protecting patient privacy and retaining the data's utility for research. It's important to regularly review and update anonymization practices to align with evolving technology, regulations, and ethical standards. Multiple peer reviewers can quality check the final dataset contents and metadata before publication. Some approaches to consider include:

        * **Data anonymization**: Remove personally identifiable information (PII) from the dataset, such as names, addresses, phone numbers, and email addresses. This process reduces the risk of re-identification of individuals.
        * **Pseudonymization**: Replace identifiers with pseudonyms or codes that can be used to re-identify the data if necessary, but only with access a the key.
        * **Data aggregation: Combine individual data points into aggregated groups, summarizing the data while reducing the risk of identifying individual entries. For example, instead of sharing exact ages, group them into age ranges.
        * **Data Perturbation**: Modify data slightly e.g. altering dates (such as birth dates, admission, and discharge dates) by a random amount to prevent identification but maintaining the relative sequence of events to prevent identification while preserving the overall utility of the dataset.
        * **Masking**: For images that capture facial features blurring, pixelation, or masking can be used to obscure the face.
        * **Redaction**:Manually or automatically redact text e.g. in clinical notes or image annotations that might contain identifiable information.



It is important when creating datasets for sharing and publishing to follow all relevant laws and regulations, such as GDPR and HIPAA for data protection and privacy. Many countries also have [localized  data protection regulations](https://unctad.org/page/data-protection-and-privacy-legislation-worldwide) that can be referenced before publication. 

Where these laws are lacking or limited, you can also create a **code of ethics/data governance policy** proscribing irresponsible and unethical use of the datasets, especially where no specific law or data protection legal structure exists to be adhered to.    
