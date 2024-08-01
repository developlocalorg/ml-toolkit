Creating accessible datasets is an essential aspect of ensuring the sustainability of AI training datasets. 

## 1. Publish in widely acceptable and available data-sharing platforms 
Researchers can promote accessibility by archiving and sharing the training data through widely accepted and available data repositories. Per Lacuna Fund requirements, these repositories should be public and open-access. 

Archiving data through these platforms ensures that the data is preserved for the long term, enabling other researchers and stakeholders to access and reuse the data for future research and applications. Additionally, these platforms provide a stable, persistent and reliable environment for data storage. The choice of hosting on widely accepted platforms makes it easier for researchers to discover and access relevant datasets, promoting the reuse and impact of your dataset.

Most machine-learning communities have established go-to repositories to find training datasets for their models. Additionally, the choice of platform depends on your intended audience and the use cases for your dataset.

_Refer to the [Hosting Guidelines ](https://docs.google.com/document/d/13-T_x3Eka0207QKRAGyAVuO20RQw_csd/edit)for other considerations when selecting a publishing platform._


    


---

!!! Example

    Some hosting platforms to consider: 

    [Havard Dataverse](https://dataverse.harvard.edu/)

    [Kaggle](https://www.kaggle.com/) 

    [Github](https://github.com/) 

    [Zenodo](https://zenodo.org/) 





## 2. License the data with appropriate open-source licenses 
Licensing AI training datasets with appropriate open-source licenses is critical for promoting the accessibility and reuse of the data. While accessibility in the context of FAIR does not necessarily mean free access for all, the Lacuna Fund grant agreement provides additional guidelines on which appropriate open-source licensing to use including [Apache 2.0](https://opensource.org/licenses/Apache-2.0) for any code or other inventions, [CC-BY 4.0 International](https://creativecommons.org/licenses/by/4.0/), or [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) for any other intellectual property (e.g., creative works that are not code or patentable). Open-source licenses provide a legal framework for sharing and using data, enabling others to access and build on your training datasets in accordance with the prescribed requirements attached to the license.  




---

!!! Example

    Some commonly used licenses included Creative Commons Licenses  and MIT licenses.

    The Creative Commons license is a widely used license that provides a flexible and standardized way for dataset owners to license data, allowing others to use the data while respecting the original creator's rights. Most publishing platforms automatically apply a license to the dataset during the publication process.





## 3. Compress the data 
Compressing your AI training data is an effective way to reduce the storage space and bandwidth required to transfer large datasets. It also provides researchers with an opportunity to minimize the cost of access and the environmental impact of their datasets by reducing energy consumption during the processing and storage of data. There are several techniques that researchers can use to compress data, including lossless compression and lossy compression.

Lossless compression techniques enable data to be compressed without any loss of information. This means that the original data can be fully reconstructed from the compressed data. Common lossless compression techniques include the gzip and zip formats, which are widely used for compressing text-based data such as CSV or TXT files. These formats can reduce the size of data by up to 70% without any loss of information.

Lossy compression techniques enable data to be compressed by sacrificing some level of detail or accuracy. These techniques are commonly used for compressing image or audio data, where small losses in quality are often imperceptible. Common lossy compression techniques include JPEG for image data and MP3 for audio data. These formats can reduce the size of data by up to 90% or more, but at the cost of some loss of detail or accuracy.

Data compression for  image datasets is usually required by some deep learning models and this compression can be done before publishing the datasets. 


