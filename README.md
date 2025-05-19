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

**Note:** use the V2 .keras and .pkl files for the latest version you want to put in your local "saved_models" folder:
   * dementia_cnn_sequential_history_V2.pkl (this file is approximately 436 bytes)
   * dementia_cnn_sequential_model_V2.keras (this file is approximately 268MB)
 
2. [MRI_dementia_classification_load_model.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/MRI_dementia_classification_load_model.ipynb). This Jupyter notebook file loads the pre-saved model (.keras) from step 1 and the history file to reproduce and verify F1 accuracy scores, as well as to load the .pkl file into the history to plot the accuracy curves.
   
3. [ai_chatbot_dementia_case.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/ai_chatbot_dementia_case.ipynb). This Jupyter notebook file shows a **simple AI chatbot** using Gradio where user can input patient's diagnostic, then the AI bot will determine if the patient has a very mild, mild, moderate, or no dementia at all.

4. [AI_Symptom_Gemini_Classifier_Fixed_With_Gemini_Functions.ipynb](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/blob/main/AI_Symptom_Gemini_Classifier_Fixed_With_Gemini_Functions.ipynb). This Jupyter notebook file shows a **more advanced AI chatbot** using Gradio where user can upload an MRI image of the brain and enter some diagnostic. The AI bot will determine if the patient has a very mild, mild, moderate, or no dementia at all. You can use the provided file in the Github folder called [MRI_image_samples_for_chatbot_demo](https://github.com/AIBC2024/Group2_Project3_AI_Chatbot/tree/main/MRI_image_samples_for_chatbot_demo). 

**Note:** as mentioned in the presentation file, we use a multi-modal diagnostic approach by combining MRI brain scan analysis (60% weighting) with symptom text analysis (40% weighting) to provide a comprehensive dementia classification. In addition of using the pre-trained MRI image to acknowledge the test MRI image, our system includes an advanced AI language model called BERT that reads and understands the clinician's notes about the patient. It analyzes not just specific keywords, but the overall tone and context of the description. If descriptions contain negative language patterns that often correlate with cognitive decline, it increases the probability of a dementia diagnosis. This provides a complementary perspective to both our image analysis and our rule-based symptom matching, creating a more comprehensive assessment system that mimics how healthcare professionals evaluate patients from multiple angles.


## Summary of the Model Analysis - CNN V2
CNN Model V2 was found to be the best peforming with an accuracy of 0.87 and F1 Score of 0.88. Iterations of the model all the way to 12 versions which included experimenting with various settings as well as using trained models like VGG-16 and RESNET were found to be overcomplicating the model. A simpler model was found to the best approach. 

![Confusion Matrix - CNN Model V2](/CNN_model_notebook_figures/confusion-matrix-V2.png "Confusion Matrix - CNN Model V2")

### Classification Report - CNN Model V2
![Classifcation Report - CNN Model V2](/CNN_model_notebook_figures/classification-report-V2.png "Classifcation Report - CNN Model V2")

![Model Accuracy - CNN Model V2](/CNN_model_notebook_figures/model-accuracy-V2.png "Model Accuracy - CNN Model V2")

![Model Loss - CNN Model V2](/CNN_model_notebook_figures/model-loss-V2.png "Model Loss - CNN Model V2")


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
