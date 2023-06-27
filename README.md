# Model-performance-Estimator

Model performance Estimator evaluates and monitors the performance of regression and classification models given the control limits of performance estimators. Additionally, it can detect any potential data drifts in individual features of dataset. This solution provides a proactive approach to model performance estimation enabling improved data driven decision making process. It uses various evaluation metrics like accuracy, f1 score, etc. to measure models’ performance and return alerts using text messages, charts and tables for given timestamps or index chunks. The solution draws attention to statistically significant events and gives appropriate warnings of data drifts that impact performance of the model post deployment.

## Amazon SageMaker



### Input :

The input has to be a '.zip' file containing 4 files namely(reference_data.csv; analysis_data.csv; nannyml_model.sav; nannyml.json):
1. Reference_data(.csv) data with ground truth on which the model is trained
2. Analysis_data(.csv) file data without the ground truth for which we want to predict the metrics
3. Nannml_model(.sav)file ML model trained on your reference data
4. Nannyml(.josn) file specifing the type of task, name of the target variable and and timestamp column name(if any)




### Output:



Content type: application/zip



### Invoking endpoint



AWS CLI Command
If you are using real time inferencing, please create the endpoint first and then use the following command to invoke it:



`aws sagemaker-runtime invoke-endpoint --endpoint-name "endpoint-name" --body fileb://input.zip --content-type application/zip --accept application/zip responce.zip`



**Substitute the following parameters:**



* "endpoint-name" - name of the inference endpoint where the model is deployed
* input.zip - input file
* application/zip - MIME type of the given input file (above)
* responce.zip - filename where the inference results are written to.



## Resources



1. [Sample Notebook](https://github.com/Mphasis-ML-Marketplace/Model-performance-Estimator/blob/main/Model-performance-Estimator.ipynb) 
2. [Sample Input](https://github.com/Mphasis-ML-Marketplace/Model-performance-Estimator/blob/main/Input/input.zip)
3. [Sample Output](https://github.com/Mphasis-ML-Marketplace/Model-performance-Estimator/blob/main/Output/response.zip) 
