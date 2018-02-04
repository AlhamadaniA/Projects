# Predictive-Analytics-of-Cell-Types-Using-Single-Cell-Gene-Expression-Profiles
The advancement in DNA sequencing technology has allowed sequencing molecular profiles at a single cell resolution. This has allowed obtaining expression profiles of each of the 20,000 protein coding genes in thousands of cells belonging to different types but from the same tissue. Even though the amount of data that has been generated using this technique has been increasing, there has been very little attempt to explore the application of predictive modeling to predict the cell types based on numerical values of the gene expressions. This project will apply predictive models using the gene expression as predictors to accurately predict the cell type. The main focus is to extract an optimal set consisting of few hundred predictors, which can accurately predict the cell types. We hypothesize that using expression profiles of a couple hundred genes, we can accurately predict the type of cell in any biological system.
For our project, the data is expression profiles of about 20,000 genes in 500 cells which are either at S, G2, or G1 phase of cell cycle process. The main component of our analysis is to apply predictive models using the gene expression as predictors to accurately predict the cell type (what stage of the cell cycle process the cell is at). One of the crucial parts is understanding, selecting and cleaning the data. After examining the imbalance of the class distribution in the data, Synthetic Minority Sampling Technique (SMOTE) is applied to achieve class balance in the data. Then, we use a series of steps to reduce the number of features (genes or predictors) in the data. First, the genes which are lowly expressed in the data are removed. To extract only statistically highly significant genes between the different cell cycle stages, we employ some statistical algorithms, one of which is ANOVA. Our filtering is based on the p-values or FDR (False Discovery Rate) values after applying ANOVA test. This reduces the 20,000 predictors to only very few thousands of genes or predictors. 
To further reduce the number of predictors; next, a fast-linear predictive multinomial penalized LASSO logistic regression technique is applied. This is one of the most popular tools for simultaneous shrinkage and variable model with an embedded feature selection process. At this point, the data is ready to be used for predictive modeling. We normalize the data first so that values of each predictors are in the range of -1 and 1 with a mean of 0. Then, we need to split our sample data to training (75%) and testing sets (25%). We utilize many predictive models and run them on the obtained data. Some of the predictive models are Random Forest, K- Nearest Neighbors, Support Vector Machines, Neural Network, Decision Trees, and Naïve Bayes.
We determine the performance of the models based on certain criteria one of which we will be using is the prediction Accuracy. After calculating the accuracy, we can check for variables importance using a target shuffling procedure. At this stage, we further check if by using a handful of predictors can we predict the type of cell. The target shuffling technique gives the importance of each gene in the predictive model. The top 20 genes will be selected and a recursive feature selection or elimination algorithm is used to get the optimal set of predictors. Different predictive models will be incorporated in this process. Model comparison will again be done using Accuracy, Kappa, Precision and Recall. We can compare the results and decide on which way is more beneficial for us. We can take a further step to expand this project by applying the same data mining pipeline to further datasets with other cell types using different genes profiles to test the generalization of the results. Therefore, we took our project one step further and we applied the same data mining pipeline to two more similar datasets of pancreatic cell types and we were able to obtain the same successful results. There was a slight difference in the generalization of the data mining pipeline only in the data wrangling or pre-processing step.

Datasets 2& 3 for Code files 2 and 3: They are not available in this repository due to their massive size.
Datasets 2& 3: Diabetic and non-diabetic Pancreatic Cell Types: Each data set will have 4 cell types (which are the classes). You have to transpose the data so that the predictors are in a column and the cells are in rows.
