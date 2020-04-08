# Building ETL Pipelines with Apache Spark

## Infrastructure

This lecture series requires a full installation of Pyspark. The easiest way to do this is via Docker. 

Launch a Jupyter Notebook server using Docker and the `jupyter/pyspark-notebook` image on your local machine.

Copy and paste the below into your terminal.

```
docker pull jupyter/pyspark-notebook
docker run -d -v `pwd`:/home/jovyan -p 80:8888 jupyter/pyspark-notebook
```

This will launch a Jupyter Notebook server available at http://localhost/. By default this server has authentication and requires a token.

### Accessing Jupyter

1. Retrieve the container id of the Jupyter Notebook Server

   ```
   docker ps
   ```
   
   This command displays currently running Docker containers. Look for the container using the image `jupyter/pyspark-notebook`. 
   
   Copy the `CONTAINER ID`.
   
2. Retrieve the token. Run the following command, replace `CONTAINERID` with the value copied in the previous step.

   ```
   docker exec CONTAINERID jupyter notebook list
   ```
   
   You should see an output like the following:
   
   ```
   Currently running servers:
   http://0.0.0.0:8888/?token=b362ef9ea151f45b29cdcf9e9c39e9c914ef2d93478bce17 :: /home/jovyan
   ```
   
   Copy the value after `token=`. This is the authentication token. 
   
3. Access the server at http://localhost/ and use the authentication token to sign in.


## March 25, 2020

[Building ETL Pipelines with Apache Spark (slides)](https://docs.google.com/presentation/d/1X2WHETOErrkfz1bEUoS2saQlX07N3ACedgTSnE4RYto/edit?usp=sharing)

[Proof-of-concept (notebook)](nb/Proof-of-concept.ipynb) **notebook**  
Demonstrates that Jupyter Server is running with full Python Scipy Stack installed.

[Lesson 1 (Google Doc)](https://docs.google.com/presentation/d/1X2WHETOErrkfz1bEUoS2saQlX07N3ACedgTSnE4RYto/edit?usp=sharing)

[Lesson 1 (notebook)](/nb/Lesson-01.ipynb)
