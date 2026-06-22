Smart Email Classification and Summarisation System using NLP and Minimal Azure Integration

Author: Aishwarya Mudravalli Ningaraju

Degree: Master of Science in Data Science

**Project Abstract**
Email overload presents a persistent challenge to organizational productivity and corporate security. This Master's project introduces an end-to-end, reproducible NLP data intelligence pipeline utilizing the Enron Email Corpus. The entire system is built as a unified pipeline capable of executing four distinct corporate mail and artifact operations:

Folder Classification (Multi-class): Automatically routes emails to operational directories (sent, inbox, deleted). Compares classical machine learning baselines (TF-IDF with Naïve Bayes, Linear SVM, and Random Forest) against a contextual, fine-tuned DistilBERT transformer model.

Spam Detection (Binary): Addresses missing ground-truth constraints using a weak supervision framework to label and isolate spam or noise.

Email Summarisation (Seq2Seq): Condenses dense, multi-sentence business correspondence into scannable summaries, evaluating baseline Lead-N metrics against abstractive DistilBART or BART architectures.

Azure Storage Blob Integration: Connects the data pipeline directly to cloud infrastructure to stream, serialize, and safely save raw/processed partitions, model prediction outputs, and evaluation metrics.

**Dataset and Setup**
This project utilizes the official Enron Email Dataset hosted on Kaggle.

**Dataset Link**: https://www.kaggle.com/datasets/wcukierski/enron-email-dataset

Storage Configuration: For execution in Google Colab, the downloaded dataset (emails.csv) was placed into Google Drive and mounted locally via runtime environment configurations to process the high-volume mail threads.

**Cloud Infrastructure and Engineering**
Data Persistence: Raw or processed training partitions, model prediction dumps, and mathematical evaluation matrices are directly serialized and streamed to Azure Blob Storage.

Security and Compliance: To align with academic software security standards, all cloud access keys and connection strings are managed dynamically via runtime environment configurations (Colab Secrets) rather than being hardcoded in the file.

**How to Run the Unified Pipeline**
The entire codebase for data preprocessing, baseline model training, transformer fine-tuning, and evaluation is contained within a single notebook file.

Download the smart_email_pipeline.ipynb notebook from this repository.

Download the emails.csv file from the Kaggle Dataset Link provided above.

Upload the dataset to your Google Drive and upload the notebook into Google Colab.

Open the Secrets panel (the key icon) on the left side of Google Colab and add your Azure credentials:
Name: AZURE_CONNECTION_STRING
Value: Your actual Azure Blob Storage connection string
Toggle Notebook Access to ON.

Update the path in the notebook to point to where you saved the Kaggle file in your Google Drive, then run the cells sequentially from top to bottom.
