# DockerImageClassificationWebService

## Note: For a larger project. This is a containerized version of an API exposed like Clarifai's. 

# Quick Summary
## A user can upload a photo and get a json list of category confidences either through the web gui or through REST-ful queries. The latter is meant to give clients an endpoint.

# Reassembly
`cat x* > itdex_service.tar.gz`

# Load image
`docker load itdex_service.tar.gz`

# Change directory to web service
`cd nexgensearch/ItDex/ItDexWebService/`

# Create Container from Image
`docker run -v $PWD:/tmp/working -w=/tmp/working -p 8888:8888 --rm -it itdex_service`

# Run web service
`python3 itdex_service.py`

# Example usage (GUI)

![alt text](https://raw.githubusercontent.com/Cpruce/ItDexWebService/master/itdex_pic2.png)

![alt text](https://raw.githubusercontent.com/Cpruce/ItDexWebService/master/itdex_pic1.png)

# Example usage (HTTP)

0.0.0.0:8888/image?={{ base_64(image_content) }}
