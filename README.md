# BRAINIACS - Group 2 | Project 3 | Dementia diagnosis 


## Overview
The first part of this project aims to assist in the early detection of dementia by combining user-reported symptoms with MRI brain scan analysis. Users begin by entering a series of cognitive and behavioral symptoms, which help inform the diagnostic process. The MRI image is then processed by an image recognition model trained to identify patterns associated with dementia. Based on this analysis, the system assesses the presence and severity of the condition, offering a data-driven aid for medical evaluation. 

The second part of this project utilizes Google Gemini API to create a chatbot that can produce diagnosis of dementia based on patients symptoms. The chatbot is built using Langchain Google GenAI with Gemini Model 2.0 Flash. An API key is required to be able to run the code. Also, the end result is shown using Gradio front end interface.

**DISCLAIMER**: this tool is assistive only, it is an AI Bootcamp final group project, it is not to replace a doctor’s or clinical diagnosis.


## Objective
To develop an AI-powered tool that integrates symptom input and MRI image analysis to detect the presence and severity of dementia, supporting early diagnosis and enhancing clinical decision-making.


## Technologies, Libraries and Data References
* Dotenv
* Numpy
* Matplotlib
* Tensorflow
* Sklearn
* Seaborn
* ChatGoogleGenerativeAI
* Gemini 2.0 LangChain


## File(s) to Run

1.  [MRI_dementia_classification_CNN.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_CNN.ipynb). This Jupyter notebook file (as an exploratory notebook) creates the model (.keras) and history file (.pkl).
   
Keras files are too big to upload into GitHub, please go to [Dropbox shared folder](https://www.dropbox.com/scl/fo/mmtv94e8t4u9x7vgvqwvw/AEigp2bJ9nK4hC_juE2aVkY?rlkey=5s76fv2w7303kxymyccdinx0h&dl=0). This folder stores the .keras and the .pkl files. You have to download those Dropbox files and place them in a folder called "saved_models" before you can run the [MRI_dementia_classification_load_model.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_load_model.ipynb). 

**Note:** use the V10 .keras and .pkl files for the latest version you want to put in your local "saved_models" folder:
   * dementia_cnn_sequential_history_V10.pkl (this file is approximately 450 bytes)
   * dementia_cnn_sequential_model_V10.keras (this file is approximately 350MB)
 
2. [MRI_dementia_classification_load_model.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_load_model.ipynb). This Jupyter notebook file loads the pre-saved model (.keras) from step 1 and the history file to reproduce and verify F1 accuracy scores, as well as to load the .pkl file into the history to plot the accuracy curves.
   
3. [ai_chatbot_dementia_case.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/ai_chatbot_dementia_case.ipynb). This Jupyter notebook file shows a **simple AI** chatbot using Gradio where user can input patient's diagnostic, then the AI bot will determine if the patient has a very mild, mild, moderate, or no dementia at all.

4. [AI_Symptom_Gemini_Classifier_Fixed_With_Gemini_Functions.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/AI_Symptom_Gemini_Classifier_Fixed_With_Gemini_Functions.ipynb). This Jupyter notebook file shows a more advanced AI chatbot using Gradio where user can upload an MRI image of the brain and enter some diagnostic. The AI bot will determine if the patient has a very mild, mild, moderate, or no dementia at all.


## Summary of the Final Analysis
**Note:** [MRI_dementia_classification_RESNET_model.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_RESNET_model.ipynb). We tried using a Resnet model approach and recieved worse results, with an F1 score of 0.28.


## Team Members
1. [Ingrid Blankevoort](https://github.com/AIBC2024)
2. [Matt Le](https://github.com/mattledevs)
3. [Patrick McCourt](https://github.com/patrickjm7)
4. [Spencer Gerritsen](https://github.com/sppencerr)
5. [Vijay Srinivasula](https://github.com/vijaysrini-1982)


## Google Slide Deck Presentation
[Group presentation link](https://docs.google.com/presentation/d/11-YDMJ-GvNs3TQDsUWVUkeZt1o0UBaijmDvD_Gnt2As/edit?usp=sharing)



## References
1. [Kaggle Source For Dataset - source file 1](https://www.kaggle.com/datasets/matthewhema/mri-dementia-augmentation-no-data-leak)
2. [Kaggle Source For Dataset - source file 2](https://www.kaggle.com/datasets/uraninjo/augmented-alzheimer-mri-dataset)
