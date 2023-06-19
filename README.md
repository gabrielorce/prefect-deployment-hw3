# prefect-deployment-hw3
mlops-zoomcamp's homework 3 - orchestration

homework 3 of the mlops zoomcamp



To be able to work with Prefect:
1) create conda environment
```
conda create --name prefect-mlops python==3.11
conda activate prefect-mlops
```
2) get requirements.txt from https://github.com/gabrielorce/mlops-zoomcamp/tree/main/03-orchestration
```
pip install -r requirements.txt
```
4) Open separate window, activate prefect server
```
prefect server start
```
5) be sure to configure PREFECT_API_URL  
Configure Prefect to communicate with the server with:
```
    prefect config set PREFECT_API_URL=http://127.0.0.1:4200/api
```
6) Check out the dashboard at http://127.0.0.1:4200  
View the API reference documentation at http://127.0.0.1:4200/docs


for creating prefect deployments:
```
prefect project init
```
this creates new files in the directory.  

Start a worker that polls your work pool:
```
prefect worker start -p <my-pool> -t process
```  

(we can create the work pool from the UI)  




In your virtual environment, install the prefect-email integration with 
```
pip install prefect-email
```
