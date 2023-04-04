# Sure-Tomorrow_11thProject
This is my project in sprint 11, which is Linear Algebra.

In this sprint, I learned the key concepts in linear algebra: vectors, matrices, and linear regression.

# Project Overview
The insurance company "Sure Tomorrow" is seeking to solve some problems with the help of machine learning, and you have been asked to evaluate the feasibility of this.

**Task 1: Find clients who are similar to a certain set of criteria. This task will make it easier for the company to carry out marketing.**

I completed this task using the kNN algorithm and based on the experiments, it was found that unscaled data produces relatively similar neighboring data indices up to index 5, while scaled data produces relatively similar neighboring data indices up to index 3. Therefore, I concluded that in the kNN algorithm, unscaled data will produce more similar indices, but I still recommend using scaled data as it can reduce the potential subjective order of neighboring data indices due to the same distance values.

**Task 2: Predict the likelihood of a new client taking out an insurance claim. Determine if the prediction model is better than the dummy prediction model.**

In evaluating this model, the f1 score was used as a metric because the company wants to avoid high values of:
 
  FP -> Customers who will not receive insurance benefits but are predicted to do so, which will decrease the company's profits.
  FN -> Customers who will receive benefits but are predicted not to, resulting in increased company expenditures.

Based on the results of the machine learning training, it was found that the model performs better when trained on scaled data. Interestingly, when the data is scaled, the model produces a FN score of zero, which means that the model can accurately predict which customers will receive benefits, thus preventing the company from incurring losses due to providing benefits to the wrong customers.

**Task 3: Protect clients' personal data without compromising the model from the previous tasks.**

In this section, I performed data masking to protect customer data by creating a random square matrix with the same number of columns and rows as the original matrix. The original matrix can still be retrieved using the inverse matrix of the masking matrix after transformation.

After analyzing and creating the model, the following is a summary of the project:

1.	Scaling numeric data can help to predict more specific numeric values, even after the decimal point. This can be very useful when looking for clusters of data.
2.	The metric for evaluating a model should be chosen based on the risks or negative outcomes that need to be avoided in the model building process.
3.	Data obfuscation techniques can be used to protect private and confidential data. These techniques do not affect the evaluation metric of the model.
