# README

This is a project for Problem A of 2021 SYSU MCM.

In this project, we try to figure out the differences between normal people's EEG (Electroencephalogram) and the EEG of patients with epilepsy as well as hope to build effective classifiers to automatically discern the epileptiform EEG. 

To reach this goal, we firstly explore and visualize the data, hoping to find some clues of probably prominent features(**"EEG-1 Explore.ipynb"**). Then, based on what we have observed, we choose 4 features (Root-Mean-Square Amplitude, Mean Frequency, Number of Peeks, and Approximate Entropy) to describe the EEG samples, and extract them in the file **"EEG-2 Feature extraction.ipynb"**. As soon as we get those features, we conduct some basic statistics, including drawing the histogram and density curve of each feature to visualize the distribution and conducting Mann-Whitney U Test to exam the significance of differences between the two groups (**"EEG-3 Basic statistical analysis.ipynb"**). Finally, we build two classifiers based on the SVM algorithm and the Decision Tree algorithm, both of which reach a high accuracy of about 96% (**"EEG-4 Classification.ipynb"**). The classifiers are visualized in the file **"EEG-5 Visualization of the classifier".**

## Files

- CODE: The function of each code file has been described above. Notice that all the codes are written in the environment of Python 3.8.10 **EXCEPT "EEG-3 Basic statistical analysis.ipynb"**, which is written in R (3.6.1). (If you want to use this code, do remember to shift the kernel to "R kernel" in Jupyter Notebook. Or you can simply copy the code and create a new R file.) And also, codes in **"EEG-4 Classification.ipynb"** only show two examples (SVM based on feature RMSA and ApEn, Decision Tree based on all features). To use different features to build the classifier, you can simply alter the code. It's not difficult since the framework is just the same and what you have to do is just to change the variables fed into the model.

- DATA: Two files are included in the folder "data": "Epileptic Seizure Recognition.csv" which is the source data collected from [Epileptic Seizure Recognition | Kaggle](https://www.kaggle.com/harunshimanto/epileptic-seizure-recognition), and "feature.csv" which is the output of the second code file (**"EEG-2 Feature extraction.ipynb"**).
- OUTPUT: Images are all stored in this folder.
- CLASSIFICATION: Two folders are included: "DT" and "SVM", and each folder also has two folders which are for models based on different features. The training sets and the testing sets are stored in this folder, and the classifiers (".m") are also included. To use the classifiers, please use Joblib ([Joblib: running Python functions as pipeline jobs — joblib 1.1.0.dev0 documentation](https://joblib.readthedocs.io/en/latest/)) to load them.
- EXPLORE: This folder includes the drafts written in the initial stage of the project. Probably most of the codes in it are not executable. I put them here just for the record. (Oh...just 20 days before I finally finished this project I almost knew nothing about what to do...quq)

## Contributors

All of the three members in our teams are students in Zhongshan School of Medicine, SYSU.

To contact us, you can email us at huangzw29@mail2.sysu.edu.cn  

The thesis of this project is available by contacting us through the E-mail address above if you have a proper reason.

Thanks for your viewing.

