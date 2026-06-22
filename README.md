\# Smart Email Classification and Summarisation System using NLP and Minimal Azure Integration



Author: Aishwarya Mudravalli Ningaraju  



\---



\## 📝 Project Abstract

Email overload presents a persistent challenge to organizational productivity and corporate security. This Master's project introduces an end-to-end, reproducible NLP data intelligence pipeline utilizing the Enron Email Corpus. The entire system is built as a unified pipeline capable of executing three distinct corporate mail operations:



1\. Folder Classification (Multi-class): Automatically routes emails to operational directories (`sent`, `inbox`, `deleted`). Compares classical machine learning baselines (TF-IDF with Naïve Bayes, Linear SVM, and Random Forest) against a contextual, fine-tuned DistilBERT transformer model.

2\. Spam Detection (Binary): Addresses missing ground-truth constraints using a weak supervision framework to label and isolate spam/noise.

3\. Email Summarisation (Seq2Seq): Condenses dense, multi-sentence business correspondence into scannable summaries, evaluating baseline `Lead-N` metrics against abstractive DistilBART/BART architectures.

4\. Storing into Azure blob storage



\---



\## ☁️ Cloud Infrastructure \& Engineering

\*Data Persistence: Raw/processed training partitions, model prediction dumps, and mathematical evaluation matrices are directly serialised and streamed to Azure Blob Storage.

\*Security \& Compliance: To align with academic software security standards, all cloud access keys and connection strings are managed dynamically via runtime environment configurations rather than being hardcoded.



\---



\## 🚀 How to Run the Unified Pipeline

The entire codebase for data preprocessing, baseline model training, transformer fine-tuning, and evaluation is contained within a single notebook file.



1\. Create a new repository clone locally or download the `smart\_email\_pipeline.ipynb` notebook.

2\. Upload the notebook into Google Colab.

3\. Open the Secrets panel on the left side of Google Colab.

4\. Add a new secret credential:

&#x20;  \* Name: `AZURE\_CONNECTION\_STRING`

&#x20;  \* Value: \*\[Your actual Azure Blob Storage connection string]\*

&#x20;  \* Toggle Notebook Access to `ON`.

5\. Run the cells sequentially from top to bottom. All critical dependencies (such as `transformers`, `azure-storage-blob`, `scikit-learn`, and `torch`) are installed automatically in the initial execution block.

