# waqas_docker-assignment
# Step1. Selected App: Django Blog App

# Step2: Dependencies
              asgiref==3.3.1
              Django==3.1.7
              pytz==2021.1
              sqlparse==0.4.1
# Step3:
First I created requirement.txt file
Added below dependencies in requirement.txt 
      asgiref==3.3.1
      Django==3.1.7
      pytz==2021.1
      sqlparse==0.4.1


Below is Dockerfile
FROM python:3.8-slim-buster           //base image
WORKDIR /app                              // change Work Directory
COPY requirements.txt requirements.txt          // copy the requirement.txt file to install the dependencies 
RUN pip3 install -r requirements.txt               // run the requirement.txt to install the dependencies
COPY . .                                            // copy all files to the working directory
CMD ["python3", "manage.py", "runserver"]            //command to run when the container is started


# Step4:
Created Docker File
