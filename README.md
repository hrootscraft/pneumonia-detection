# Pneumonia Detection API

<br>

### Deploy a Production Machine Learning Model REST API with AWS 

Here are the main steps of the code:
* Import necessary libraries and set up the SageMaker session.
* Retrieve the Docker image for the image classifier from Amazon's Elastic Container Registry (ECR) and set up the estimator.
* Set up the hyperparameters for the model and define a range of values for some of the hyperparameters to be tuned using SageMaker's Hyperparameter Tuning feature.
* Define the training data and validation data and set up the hyperparameter tuning job.
* Once the best hyperparameters are found, create a model from the best training job and deploy it to an endpoint.
* Use the endpoint to make predictions on new chest X-ray images
<br>

<hr>

This code trains an image classifier model to classify chest X-ray images into two categories: normal and pneumonia. 
All the data for training, testing and validating the model as well as the trained classifiers are stored in S3 buckets.
The model is trained using a pre-trained convolutional neural network (CNN) and transfer learning. 
The hyperparameters of the model are tuned using Amazon SageMaker's Hyperparameter Tuning feature, which finds the best set of hyperparameters for the model by searching over a defined range of values with it's default Bayesian Search Optimization Technique. The training of the classifier is then logged and tracked from CloudWatch and CloudWatch Logs.
Once the model is trained, it is deployed to an endpoint using Amazon SageMaker's deployment feature with API Gateway + Lambda Functions, and then used to make predictions on new chest X-ray images. 

<br>

<sub>[Quick video walk-through](https://youtu.be/8EjjyvhszoA)</sub>
