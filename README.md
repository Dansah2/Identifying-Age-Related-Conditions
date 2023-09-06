# Identifying-Age-Related-Conditions
Predict whether a subject has or has not been diagnosed with a condition-- a binary classification problem.

Goal

The goal is to predict if a person has any of three medical conditions. If the person has one or more of any of the three medical conditions (Class 1), or none of the three medical conditions (Class 0). Create a model trained on measurements of health characteristics.

To determine if someone has these medical conditions requires a long and intrusive process to collect information from patients. The data consists of characteristics relative to the conditions, that are encoded to protect the patient information.

Context

They say age is just a number but a whole host of health issues come with aging. From heart disease and dementia to hearing loss and arthritis, aging is a risk factor for numerous diseases and complications. The growing field of bioinformatics includes research into interventions that can help slow and reverse biological aging and prevent major age-related ailments. Data science could have a role to play in developing new methods to solve problems with diverse data, even if the number of samples is small.

Currently, models like XGBoost and random forest are used to predict medical conditions yet the models' performance is not good enough. Dealing with critical problems where lives are on the line, models need to make correct predictions reliably and consistently between different cases.

Founded in 2015, data host InVitro Cell Research, LLC (ICR) is a privately funded company focused on regenerative and preventive personalized medicine. Their offices and labs in the greater New York City area offer state-of-the-art research space. InVitro Cell Research's Scientists are what set them apart, helping guide and defining their mission of researching how to repair aging people fast.

Each observation is either of class 0 or of class 1. For each observation, you must submit a probability for each class. The formula is then:

Log Loss=−1𝑁0∑𝑁0𝑖=1𝑦0𝑖log𝑝0𝑖−1𝑁1∑𝑁1𝑖=1𝑦1𝑖log𝑝1𝑖2

where (N_{c}) is the number of observations of class (c), (\log) is the natural logarithm, (y_{c i}) is 1 if observation (i) belongs to class (c) and 0 otherwise, (p_{c i}) is the predicted probability that observation (i) belongs to class (c).

The submitted probabilities for a given row are not required to sum to one because they are rescaled prior to being scored (each row is divided by the row sum). In order to avoid the extremes of the log function, each predicted probability 𝑝 is replaced with max(min(𝑝,1−10−15),10−15).