# Model-performance-Estimator

Model performance Estimator evaluates and monitors the performance of regression and classification models given the control limits of performance estimators. Additionally, it can detect any potential data drifts in individual features of dataset. This solution provides a proactive approach to model performance estimation enabling improved data driven decision making process. It uses various evaluation metrics like accuracy, f1 score, etc. to measure models’ performance and return alerts using text messages, charts and tables for given timestamps or index chunks. The solution draws attention to statistically significant events and gives appropriate warnings of data drifts that impact performance of the model post deployment.

## Amazon SageMaker



### Input :



**Usage Methodology for the algorithm:**



The input has to be a '.txt' file with 'utf-8' encoding. PLEASE NOTE: If your input .txt file is not 'utf-8' encoded, model will not perform as expected
1. To make sure that your input file is 'UTF-8' encoded please 'Save As' using Encoding as 'UTF-8'
2. The input can have a maximum of 512 words (Sagemaker restriction)
3. Input should have atleast 3 sentences (Model limitation)
4. Supported content types: text/plain



### Output:



Content type: text/plain



### Invoking endpoint



AWS CLI Command
If you are using real time inferencing, please create the endpoint first and then use the following command to invoke it:



`aws sagemaker-runtime invoke-endpoint --endpoint-name "endpoint-name" --body fileb://input.txt --content-type text/plain --accept text/plain result.txt`



**Substitute the following parameters:**



* "endpoint-name" - name of the inference endpoint where the model is deployed
* input.txt - input file
* text/plain - MIME type of the given input file (above)
* result.txt - filename where the inference results are written to.



## Resources



1. [Sample Notebook](text_summary_marketplace.ipynb) 
2. [Sample Input](SampleInput)
3. [Sample Output](SampleOutput) 
