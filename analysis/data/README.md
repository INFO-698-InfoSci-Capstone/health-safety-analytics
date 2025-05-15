# README for data used in Health and Safety Analytics

## Overview 
This dataset consists of real-world job descriptions provided by our industry partner. Each description has been annotated by three certified health and safety experts with one or more potential injury body part labels. These annotations are used as ground truth for evaluating model performance in injury prediction and safety recommendation tasks. 

To support retrieval-augmented generation (RAG) and enhance contextual reasoning, the project also integrates supplemental domain-specific knowledge sources, including: 
- MSHA regulatory documents (Title 30 CFR)
- New Miner & Annual Refresher Training Student Guide
- Accident Prevention Activity Reports from our industry collaborator

***

## Structure of the data
#### Data set #1 (`data.csv`, Job Descriptions and Annotations)  
- `description`: Text of the job description or observation (string)  
- `annotator_1_label`, `annotator_2_label`, `annotator_3_label`: Body part(s) labeled as potential injury risk (categorical; one or more of: `Ankle`, `Back`, `Eye`, `Hand`, `Knee`, `Shoulder`, `Other`)  

#### External domain knowledge files
Additional unstructured text sources are included to support RAG. They serve as external domain knowledge:

- `regulations.txt`: Excerpts from MSHA regulatory documents (Title 30 CFR)  
- `training_guide.txt`: Content from the New Miner & Annual Refresher Training Student Guide  
- `incident_reports.txt`: Accident Prevention Activity Reports provided by our industry collaborator


#### Prompt files for few-shot learning
We use different few-shot prompts to guide large language models (LLMs) in three tasks:

- `predict_label_and_cause_prompt.txt`:  
  Prompts the model to identify potential injury body part(s) and explain the likely cause(s) based on the job description.

- `recommendation_prompt.txt`:  
  Prompts the model to generate tailored safety recommendations based on the predicted injury body part(s), without using external knowledge sources.

- `recommendation_with_rag_prompt.txt`:  
  Prompts the model to generate recommendations with RAG, using content retrieved from external domain knowledge sources.

Each prompt file contains 7 expert-reviewed few-shot examples and an instruction block to guide model outputs. All seven injury label categories (`Ankle`, `Back`, `Eye`, `Hand`, `Knee`, `Shoulder`, `Other`) are represented across the examples to ensure comprehensive coverage.

***
