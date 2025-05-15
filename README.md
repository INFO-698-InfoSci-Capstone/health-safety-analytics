# Health & Safety Analytics: Applying Generative Models for Job Planning and Risk Management in Mining

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Overview
Mining is a high-risk industry, yet most safety systems are reactive, responding only after accidents occur. However, job descriptions and site records hold valuable insights that could help prevent injuries. We propose ***MineGuard*** — a proactive system that leverages textual mining job descriptions to predict potential injury body parts and generate safety recommendations, aiming to enhance prevention and improve worker safety awareness.

MineGuard uses large language models (LLMs) with few-shot prompting to identify injury risks and their likely causes. We integrate external domain knowledge through retrieval-augmented generation (RAG), incorporating MSHA regulations, safety training materials, and accident prevention reports provided by our industry collaborator. We plan to implement a validation agent to fact-check model-generated recommendations and improve trustworthiness. Model performance is evaluated against expert-annotated labels using standard metrics such as F1 score. We will integrate more expert reviews and feedback from safety and health professionals to iteratively enhance the system’s reliability in real-world settings.

## 🚀 Live Demo

Try the MineGuard system in action:  
**🔗 [Launch Demo](https://huggingface.co/spaces/yanyandong/hs-demo?logs=container)**

Enter a mining job description and get predicted injury body parts and likely causes, powered by large language models.


## File Organization

    analysis/
    |
    ├── logs/
    │   └── log_yanyan-dong.md # log of any progress or relevant information
    |
    |
    ├── data/
    |   ├── README.md           # describes the dataset structure. Data files are not public,
    │                           # so this README outlines file format, fields, and usage.
    |   
    └── Materials/
        ├── Figures/     
        |                      #  figures for the main manuscript
        └── Tables/      
                               # supplementary tables for the main manuscript 
    
## Code Repository (Private Access)

The full analysis code is stored in a *private GitHub repository* due to project confidentiality. Access has been granted to the project advisor.

📁 Repository link (restricted access):  
[github.com/yanyan-dong/mineguard](https://github.com/yanyan-dong/mineguard)


        

