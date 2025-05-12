# BRAINIACS - Group 2 | Project 3 | Dementia diagnosis 


## Overview
The first part of this project aims to assist in the early detection of dementia by combining user-reported symptoms with MRI brain scan analysis. Users begin by entering a series of cognitive and behavioral symptoms, which help inform the diagnostic process. The MRI image is then processed by an image recognition model trained to identify patterns associated with dementia. Based on this analysis, the system assesses the presence and severity of the condition, offering a data-driven aid for medical evaluation. 

The second part of this project utilizes Google Gemini API to create a chatbot that can produce diagnosis of dementia based on patients symptoms. The chatbot is built using Langchain Google GenAI with Gemini Model 2.0 Flash. An API key is required to be able to run the code. Also, the end result is shown using Gradio front end interface.

DISCLAIMER: this tool is assistive only, it is an AI Bootcamp final group project, it is not to replace a doctor’s or clinical diagnosis.


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

1.  [MRI_dementia_classification_load_model.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_load_model.ipynb). This Jupyter notebook file loads the pre-saved model (.keras) to run on the test data to verify F1 accuracy scores, as well as to load the .pkl files into the history to plot the accuracy curves.
   
2.  Keras files are too big to upload into GitHub, please go to [Dropbox shared folder](https://www.dropbox.com/scl/fo/mmtv94e8t4u9x7vgvqwvw/AEigp2bJ9nK4hC_juE2aVkY?rlkey=5s76fv2w7303kxymyccdinx0h&dl=0). This folder stores the .keras and the .pkl files. You have to download those Dropbox files and place them in a folder called "saved_models" before you can run the [MRI_dementia_classification_load_model.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_load_model.ipynb).
 
3. [MRI_dementia_classification_CNN.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_CNN.ipynb). This Jupyter notebook file loads the three models (.keras) to run on the test data to get better F1 accuracy scores, as well as to load the .pkl files into the history to plot the accuracy curves.
   
4. [ai_chatbot_dementia_case.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/ai_chatbot_dementia_case.ipynb). This Jupyter notebook file shows a simple AI chatbot using Gradio where user can input patient's diagnostic, then the AI bot will determine if the patient has a mild, moderate, or severe dementia, or no dementia at all.


## Summary of the Final Analysis
TBD


## Team Members
1. [Ingrid Blankevoort](https://github.com/AIBC2024)
2. [Matt Le](https://github.com/mattledevs)
3. [Patrick McCourt](https://github.com/patrickjm7)
4. [Spencer Gerritsen](https://github.com/sppencerr)
5. [Vijay Srinivasula](https://github.com/vijaysrini-1982)


## Google Slide Deck Presentation
[Group presentation link](https://docs.google.com/presentation/d/11-YDMJ-GvNs3TQDsUWVUkeZt1o0UBaijmDvD_Gnt2As/edit?usp=sharing)



## References
https://www.kaggle.com/datasets/matthewhema/mri-dementia-augmentation-no-data-leak

