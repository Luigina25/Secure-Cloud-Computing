# Secure-Cloud-Computing
Secure Cloud Computing Project, a.a. 2022/2023

With the help of Arrikto, using Kubeflow and Kubernetes, the aim of the project was to train a time series glucose prediction model for 6 patients affected by Type 1 Diabetes.
Hyperparamter tuning was performed using Kale, and the best models saved as a Bundle (name/version) to later support serving using TensorFlow Serving.

The models have each been served with the help of Docker, and the images corresponding to the served models have been uploaded on Docker Hub.
The images have been used for the deployment of the models in Kubernetes, where later NodePort services were defined to expose each pod outside of the cluster.
Lastly, a Nginx Ingress checks and forwards the traffic to each service to infere the models.

The web app was designed using Streamlit, where one of the 6 patients can add their own data (csv files) to get a prediction from the respective model.
A graph displays the results.

The web app has been deployed using Docker as well.
