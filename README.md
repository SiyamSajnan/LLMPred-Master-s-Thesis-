# LLMPred: Fine-Tuned Large Language Model Embeddings for Drug Side Effect Frequency Prediction
## Currently finalizing the research paper so the code will be uploaded soon

## Project Description
LLMPred is a research thesis that utilizes fine-tuned embeddings from large language models (LLMs) to predict the frequency of drug side effects. By leveraging advanced embedding techniques, the study aims to improve prediction accuracy in identifying drug-related side effects, which could range from mild symptoms to severe health complications. This project highlights the importance of LLM embeddings in enhancing drug safety and aiding clinical decision-making.


## Research Objective
- **Problem Statement**: Develop a model to predict drug side effect frequency (DSF) and high frequency (DSHF) by utilizing a drug-side effect network. The study aims to use embeddings generated from LLMs to address challenges in the domain of drug safety.
- **Motivation**: Predicting side effect frequency can inform the therapeutic efficacy and safety profile of drugs in clinical settings, enabling better risk assessment.

## Models Employed
- **ChemBERTa-2**: Fine-tuned on SMILES strings for chemical structure embedding.
- **SimCSE**: Utilizes contrastive learning to optimize semantic embeddings for textual descriptions of drugs and side effects.
- **Combined Embeddings**: Leveraging both ChemBERTa-2 and SimCSE embeddings to enrich predictive accuracy.

## Features
- **Data Acquisition**: Data obtained from Galeano et al.’s benchmark dataset, DrugBank, and SIDER, including drug SMILES representations and biomedical descriptions.
- **Embedding Techniques**:
  - **ChemBERTa-2**: Optimized for chemical data.
  - **SimCSE**: Focuses on meaningful sentence embeddings.
  - **Fine-Tuning with Custom Loss Functions**: Combined CoSENT, In Batch Negative (IBN), and AnglE losses to optimize embedding alignment and predictive power.
- **Frequency Prediction**: Multilayer Perceptron (MLP) used to predict DSF and DSHF using generated embeddings.

## Methodology
- **Embedding Generation**: Drug and side effect embeddings are generated using ChemBERTa-2 for chemical structures and SimCSE for semantic descriptions.
- **Fine-Tuning**: Embeddings are fine-tuned with a combined loss function to maximize similarity between positive samples and minimize it for negative ones, improving model performance in distinguishing frequent vs. infrequent side effects.
- **Model Training**: Predictive model trained on MLP, evaluating its performance with metrics like SCC, MAE, RMSE, AUC-ROC, and AUPRC.

## Results & Analysis
- **DSF Metrics**: LLMPred achieved a Spearman’s Rank Correlation of 0.707, outperforming previous models.
- **DSHF Metrics**: LLMPred showed high accuracy (82.26%), with AUC-ROC at 0.8248 and AUPRC at 0.8337, surpassing previous benchmarks.

