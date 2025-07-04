---
layout: pw43-project

permalink: /:path/

project_title: Extraction of Orofacial Pain Comorbidities from Clinical Notes Using Large Language
  Models
category: Quantification and Computation

key_investigators:

- name: Alban Gaydamour
  affiliation: University of Michigan
  country: USA

- name: Lucia Cevidanes
  affiliation: University of Michigan
  country: USA

- name: Steve Pieper
  affiliation: Isomics
  country: USA

- name: David Hanauer
  affiliation: University of Michigan
  country: USA

- name: Juan Prieto
  affiliation: University of North Carolina
  country: USA

- name: Lucie Dole
  affiliation: University of North Carolina
  country: USA

---

# Project Description

<!-- Add a short paragraph describing the project. -->


Temporomandibular Disorders (TMDs) are often linked with complex comorbidities that are difficult to extract from long free-text clinical notes. This project leverages Large Language Models (LLMs) to identify and summarize these comorbidities, enabling structured analysis and visualization across patient cohorts.



## Objective

<!-- Describe here WHAT you would like to achieve (what you will have as end result). -->


1. Fine-tune open-source LLMs to extract a curated list of TMD-related comorbidities from clinical notes.
2. Generate structured patient-level outputs from model predictions.
3. Visualize comorbidity data using an interactive dashboard.
4. Compare model performance to determine the most clinically effective approach.



## Approach and Plan

<!-- Describe here HOW you would like to achieve the objectives stated above. -->


1. Annotate clinical notes with summaries across 56 comorbidity criteria.
2. Fine-tune LLMs such as `facebook/bart-large-cnn` and `deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B` using chunked note inputs.
3. Generate structured outputs and compile them into a CSV.
4. Visualize cohort-level trends using a Python-based dashboard.
5. Evaluate model performance and deploy the tool to be accessible in 3D Slicer.



## Progress and Next Steps

<!-- Update this section as you make progress, describing of what you have ACTUALLY DONE.
     If there are specific steps that you could not complete then you can describe them here, too. -->


1. Deidentified clinical notes were obtained and manually summarized for 500.
2. Fine-tuned `facebook/bart-large-cnn` and `deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B` on these summaries to generate structured outputs across 56 comorbidity fields.
3. Generated CSV outputs from model summaries and created a dashboard to visualize cohort-level patterns.
4. Currently working on fine-tuning larger models and expanding the dataset.
5. Next steps include completing 500 patient summaries, comparing model performance, and deploying the tool for use in 3D Slicer.



# Illustrations

<!-- Add pictures and links to videos that demonstrate what has been accomplished. -->


### Table 1. Metrics from BART training

|Fold|ROUGE-1|ROUGE-2|ROUGE-L|ROUGE-L sum|
|---|---|---|---|---|
|Fold1|83.68|71.99|83.50|83.49|
|Fold2|83.48|73.40|83.11|83.14|
|Fold3|84.93|74.23|84.38|84.57|
|Fold4|85.50|74.73|85.11|85.21|
|Fold5|85.47|74.64|84.98|85.01|
|Average|84.61|73.80|84.22|84.29|

### Table 2. Metrics from DeepSeek training

|Fold|ROUGE-1|ROUGE-2|ROUGE-L|ROUGE-L sum|
|---|---|---|---|---|
|Fold1|86.55|86.49|86.53|86.54|
|Fold2|84.90|84.79|84.86|84.82|
|Fold3|86.08|86.09|86.10|86.11|
|Fold4|85.96|85.91|85.95|85.92|
|Fold5|85.21|85.70|85.17|85.21|
|Average|85.74|85.70|85.72|85.72|

### Figure 1. Dashboard summary from 500 cases extracted manually
![Dashboard summary from 500 cases extracted manually](https://github.com/user-attachments/assets/29e17ece-13d4-417a-ae64-955ce6d66cfc)

### Figure 2. Dashboard summary from 500 cases extracted by fine-tuned BART
![Dashboard summary from 500 cases extracted automatically by BART](https://github.com/user-attachments/assets/b0edb217-d825-4a37-ac95-3226689d7c1a)

### Figure 3. Dashboard summary from 500 cases extracted by fine-tuned DeepSeek
![Dashboard summary from 500 cases extracted automatically by DeepSeek](https://github.com/user-attachments/assets/54e0cb4b-d307-4b38-ba45-02f99a906ed4)



# Background and References

<!-- If you developed any software, include link to the source code repository.
     If possible, also add links to sample data, and to any relevant publications. -->


- Github Page: [https://github.com/DCBIA-OrthoLab/MedEx](https://github.com/DCBIA-OrthoLab/MedEx)
- Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Veselin Stoyanov, and Luke Zettlemoyer. 2020. BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension. *Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics*, pages 7871–7880.
- DeepSeek-AI, Guo D, Yang D, et al. DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning. Preprint at *arXiv*, 2025. Available from: [https://arxiv.org/pdf/2501.12948](https://arxiv.org/pdf/2501.12948).

