# An Integrated, Uncertainty-Aware Brain Tumor Analysis Pipeline Using DINO and SA-TransUNet

##### **Background**

According to the Godfather of AI, Geoffrey Hinton, hundreds of thousands of patients die from a medical misdiagnosis each year. While these numbers may seem staggering, advanced optimization techniques offer hope for addressing this. Neural network models have already proven less error-prone than humans in some diagnostic contexts when working with multiple agents, so developing technologies that build on this could eventually reduce the need for more medical physicians. As an educational exercise, we aim to develop a pipeline that determines whether a patient has a brain tumor from T1 MRI scans, identifies the tumor type, and generates corresponding segmentation masks.

##### 

##### **Overview**

This project uses a vision transformer from the DINO family to extract features from the BRISC MRI dataset's images to classify them into 4 classes: (G) glioma, (M) meningioma, (P) pituitary tumor, or (N) no tumor, as done in \[1\]. Using an SVM head yields better results than the MLP. For tumor-positive examples, we borrowed an SA-TransUNet model \[2\] to create segmentation masks. A final hardcoded Python script generates a report for each output showing the original MRI scans, the predicted tumor type, its corresponding mask, and suggested websites containing information about the tumor type, possible treatments, relevant information, and next steps.

##### **Results&nbsp;**

DINO extraction followed by SVM classification is by far the most effective method, with near perfect classficiations and little to no training time required. MLP heads perform decently well with either the EfficientNet-MLP and DINO-MLP model configurations.&nbsp;

##### **NEW Diagram Workflow**

Data preprocessing  \-\> NEURAL COMP1  \-\> NEURAL COMP2 \-\> Generate Diagnostic Report

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4-classifier             Segmentation

##### **Google Drive**

**NOTE:** When programming the .ipynb files, I hardcoded the paths, so they might need to be changed since I moved them to a single folder to share.

[https\://drive.google.com/drive/folders/10KGwKTI1Dsz\\\_qcMMu-1BI5BsthOh6k35?usp=sharing](https://drive.google.com/drive/folders/10KGwKTI1Dsz\\_qcMMu-1BI5BsthOh6k35?usp=sharing)

##### **References**

\[1\] [https\://doi.org/10.3390/electronics15050952](https://doi.org/10.3390/electronics15050952)

\[2\] [GitHub \- mohassan5286/Brain-Tumor-Segmentation-BRISC-2025 · GitHub](https://github.com/mohassan5286/Brain-Tumor-Segmentation-BRISC-2025)&nbsp;