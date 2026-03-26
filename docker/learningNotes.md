# DataEngineeringZoomCamp2026
Workshop Codespaces

"Docker is a containerization software that allows us to isolate software in a similar way to virtual machines but in a much leaner way.
A Docker image is a snapshot of a container that can define to run a software, or in this case our data pipelines. By exporting docker images to cloud providers where the containers can run."

A docker image is a stateless meaning, once the user quits the docker container ran using the docker image with any additional installations in it post running the container, all the applications installed (not defaultly came with the image) will be gone.

Example:
docker run -it ubuntu (no python installed)
"If we install python and quit the container and run the image again, no python can be invoked defaultly"
Python has to be installed again if needed.

## Why Docker?
Docker provides the following advantages:

Reproducibility: Same environment everywhere
Isolation: Applications run independently
Portability: Run anywhere Docker is installed
They are used in many situations:

Integration tests: CI/CD pipelines
Running pipelines on the cloud: AWS Batch, Kubernetes jobs
Spark: Analytics engine for large-scale data processing
Serverless: AWS Lambda, Google Functions

We can restart the stopped docker containers but it is not a good practice
command to start the stopped containers "docker start "containerID or image name"

To view the list of stopped containers
docker ps -a
To display only docker container IDs
docker ps -aq

To save space, we can delete the stopped containers using the below command
docker rm $(docker ps -aq)
Note: Any running containers cannot be deleted unless those are stopped

To run base image
"docker run -it --rm python:3.9.16-slim"
To start with bash
"docker run -it --entrypoint=bash --rm python:3.9.16-slim"
In the above two commands, slim indicates to get a smaller version, --rm is to destroy it after quitting

## Volumes
As the docker containers are stateless, we cannot store/save data in it.
So, a common way to store data is attaching volumes





