### Technical Articles & Projects:
#### 1. *Building and Deploying a Multistage Multimodal Recommender system on Amazon Elastic Kubernetes Service*
   **Towards Data Science Post**: https://towardsdatascience.com/deploying-a-multistage-multimodal-recommender-system-on-amazon-eks-featuring-bloom-filters-feature-caching-and-contextual-recommendations
   **Medium article:** https://mustaphaunubi.medium.com/building-a-production-multistage-recommender-system-on-kubernetes-featuring-multimodal-embeddings-5bcd6d7bbf56?postPublishedType=repub
   
   **Code**: https://github.com/MustaphaU/Multistage-Multimodal-Recommender-System-on-Amazon-EKS-with-NVIDIA-Merlin  
   **Short Demo**: https://www.youtube.com/watch?v=rwUwrISzDEQ
   
   ![Model Serving Pipeline](https://github.com/MustaphaU/MustaphaU/blob/main/Assets/Blank%20document%20-%20Page%2010%20(4).png)
   Figure 1: The model serving pipeline   
   
This project presents a multistage multimodal recommender system built and deployed on Amazon Elastic Kubernetes Service. It features online and offline feature stores backed by Athena+S3 and Valkey (Redis) respectively. User cold-start is managed via Feature masking, context-aware retrieval & ranking, and near real-time personalization with online feature updates. The system also ingests multimodal item features which can improve the content based signal and item cold-starts. Recently interacted items are filtered using a Valkey (Redis) backed Bloom filter.
  ```bibtex
@article{momoh2026multistage,
  title={Deploying a Multistage Multimodal Recommender System on Amazon Elastic Kubernetes Service},
  author={Momoh, Mustapha Unubi},
  platform={Towards Data Science},
  year={2026},
  month={May},
  url={https://towardsdatascience.com/deploying-a-multistage-multimodal-recommender-system-on-amazon-eks-featuring-bloom-filters-feature-caching-and-contextual-recommendations}
}
```
The system is operationalized with Kubeflow pipelines. One pipeline orchestrates the initial feature setup, training the models, and deploying the NVIDIA Triton Inference server. The second pipeline manages the periodic incremental fine-tuning of the query tower and the ranker.  
![The MLOps architecture](https://github.com/MustaphaU/MustaphaU/blob/main/Assets/Blank%20document%20-%20Page%209%20(11).png)
Figure 2: MLOps architecture

#### 2. *Deploying a Ranking only recommender system based on Deep Cross Network (DCN) with AUC based drift triggered fine-tuning.*
   **Medium Article**: https://mustaphaunubi.medium.com/building-a-recommender-system-with-continuous-retraining-on-amazon-eks-with-nvidia-merlin-hugectr-5b734c71bbc5  
   
   **Code**: https://github.com/MustaphaU/Merlin-RecSys-MLOps-on-AWS  

   ![MLOps](https://github.com/MustaphaU/MustaphaU/tree/main/Assets/arch___.png)
   Figure 1: Ads-ranking MLOps with monitoring component for drift detection and auto-retraining 

In this project, the DCN based recommendation model is trained on a subset of the Criteo 1TB logs dataset to predict Click Through Rates (CTR). The system includes a monitoring component that watches the system for performance drift and triggers incremental training run once drift is detected. The NVIDIA Triton Inference Server is autoscaled based on a custom latency metric via two options: Kubernetes HPA & Karpenter OR Kubernetes HPA & Cluster Autoscaler. 
   ```bibtext
  @article{momoh2026continuous,
    title={Building a single-stage Recommender System with Continuous Retraining on Amazon EKS with NVIDIA Merlin, HugeCTR, NVIDIA Triton Inference Server, and Kubeflow Pipelines},
    author={Momoh, Mustapha Unubi},
    platform={Medium},
    year={2026},
    month={March},
    url={https://mustaphaunubi.medium.com/building-a-recommender-system-with-continuous-retraining-on-amazon-eks-with-nvidia-merlin-hugectr-5b734c71bbc5}
  }
   ```
<!---
### About Me
---
I am Mustapha Unubi Momoh. I have worked mostly in applied machine learning. My recent experience includes information retrieval, specifically personalized search, recommender systems, and experimentation. I have also worked as a GenAI scientist, consulting for companies to build proof of concept (POC) applications utilizing diffusion models, large language models (LLMs), RAG techniques, vector databases, and graph databases. I also have experience in computer vision and took graduate-level computer vision courses while at the University of Waterloo.

My graduate research combined causal inference, human–computer interaction, and virtual reality (VR). I studied telehealth adoption by modeling the impact of socio-demographic variables such as technology affinity on comfort with diagnosis in VR-based telehealth. This involved Bayesian beta regression and regression discontinuity design (RDD) for estimating treatment effects.

### Academic Qualifications:
---
* Master of Applied Science (MASc.) in Systems Design Engineering, University of Waterloo (2022 - 2024)

  Thesis: [Remote Medical Diagnosis in Virtual Reality: A mixed-methods Approach to Understanding the Perceptions of Patients and Physicians](https://uwspace.uwaterloo.ca/items/ed73fad6-81d0-447d-b3ac-153c3e103fba).
  Relevant skills: Causal Inference, Bayesian Modeling, Beta regression, and Factor analysis

  ## Selected Coursework:
  1. Graphical Deeplearning  
  2. Time series analysis
  3. Information Visualization for AI Explainability
  4. Data Structures in Health Informatics.
  
### Professional Experience
---
Recently, I have worked professionally as a Machine Learning Engineer at [Pixite Inc.](https://pixiteapps.com/) (2024 - 2025), Data Engineer at [EveryRate](http://everyrate.ca/) (2024-2024) and Generative AI Engineer consultant at [Capgemini](https://www.capgemini.com/ca-en/) (2023-2024). 

In the past, I taught Python and data science with the Data Scientists Network (DSN), and founded Karaam Analytics Limited to continue these efforts.
--->

### Contact:
Email: mustaphaunubi@gmail.com.



