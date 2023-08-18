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

FROM python:3.8-slim-buster
WORKDIR /app

COPY requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

COPY . .

CMD ["python3", "manage.py", "runserver"]


FROM python:3.8-slim-buster           //base image
WORKDIR /app                              // change Work Directory
COPY requirements.txt requirements.txt          // copy the requirement.txt file to install the dependencies 
RUN pip3 install -r requirements.txt               // run the requirement.txt to install the dependencies
COPY . .                                            // copy all files to the working directory
CMD ["python3", "manage.py", "runserver"]            //command to run when the container is started


# Step4:
Created Docker Image sucesfully 

![image](https://github.com/mwaqaskh/waqas_docker-assignment/assets/39801941/96c963a1-9ac5-4e0e-9c35-1c6d27100412)


 => [internal] load build definition from Dockerfile                                                                                                                                                        0.0s
 => => transferring dockerfile: 210B                                                                                                                                                                        0.0s
 => [internal] load .dockerignore                                                                                                                                                                           0.0s
 => => transferring context: 2B                                                                                                                                                                             0.0s
 => [internal] load metadata for docker.io/library/python:3.8-slim-buster                                                                                                                                   4.6s
 => [1/5] FROM docker.io/library/python:3.8-slim-buster@sha256:8799b0564103a9f36cfb8a8e1c562e11a9a6f2e3bb214e2adc23982b36a04511                                                                             9.7s
 => => resolve docker.io/library/python:3.8-slim-buster@sha256:8799b0564103a9f36cfb8a8e1c562e11a9a6f2e3bb214e2adc23982b36a04511                                                                             0.0s
 => => sha256:8799b0564103a9f36cfb8a8e1c562e11a9a6f2e3bb214e2adc23982b36a04511 988B / 988B                                                                                                                  0.0s
 => => sha256:23d7a8ad83a5dc0487d65a89ab61aa618e5b5d6379b6e429e0459be999b5b8fd 1.37kB / 1.37kB                                                                                                              0.0s
 => => sha256:ebe69edfe405db3fc5cb36968a6f0359602992d8083c6674d9cf21af5362ca7e 6.88kB / 6.88kB                                                                                                              0.0s
 => => sha256:d191be7a3c9fa95847a482db8211b6f85b45096c7817fdad4d7661ee7ff1a421 25.92MB / 25.92MB                                                                                                            8.1s
 => => sha256:14aea17807c4c653827ca820a0526d96552bda685bf29293e8be90d1b05662f6 2.65MB / 2.65MB                                                                                                              2.6s
 => => sha256:3fe349e029970270c77c6cc4e8c8159d6390de76a4c30666e585e9ac57e54212 12.98MB / 12.98MB                                                                                                            5.2s
 => => sha256:7399277d91f4520aebebe70097c48af726818282fbbc79c1fb34b53f088eb090 243B / 243B                                                                                                                  3.1s
 => => sha256:35f10c4cf03d43a7afd688184e68c55cc3adc2049e78dffcc419a28f8ee8ac68 3.14MB / 3.14MB                                                                                                              4.6s
 => => extracting sha256:d191be7a3c9fa95847a482db8211b6f85b45096c7817fdad4d7661ee7ff1a421                                                                                                                   0.9s
 => => extracting sha256:14aea17807c4c653827ca820a0526d96552bda685bf29293e8be90d1b05662f6                                                                                                                   0.1s
 => => extracting sha256:3fe349e029970270c77c6cc4e8c8159d6390de76a4c30666e585e9ac57e54212                                                                                                                   0.3s
 => => extracting sha256:7399277d91f4520aebebe70097c48af726818282fbbc79c1fb34b53f088eb090                                                                                                                   0.0s
 => => extracting sha256:35f10c4cf03d43a7afd688184e68c55cc3adc2049e78dffcc419a28f8ee8ac68                                                                                                                   0.2s
 => [internal] load build context                                                                                                                                                                           0.0s
 => => transferring context: 7.99kB                                                                                                                                                                         0.0s
 => [2/5] WORKDIR /app                                                                                                                                                                                      0.1s
 => [3/5] COPY requirements.txt requirements.txt                                                                                                                                                            0.0s
 => [4/5] RUN pip3 install -r requirements.txt                                                                                                                                                              7.3s
 => [5/5] COPY . .                                                                                                                                                                                          0.0s
 => exporting to image                                                                                                                                                                                      0.4s
 => => exporting layers                                                                                                                                                                                     0.4s
 => => writing image sha256:612a1b75c831b30c6cdfb1ddf1091a46c58d709bc43f6e96dab42c71f4058d60                                                                                                                0.0s 
 => => naming to docker.io/library/python-django      

# Step 5
Have published the image succesfully 
 ![image](https://github.com/mwaqaskh/waqas_docker-assignment/assets/39801941/fd36e670-b0ab-479e-a879-7876ebb04403)

# Step 6
I have created repo name "waqas_docker-assignment"
![image](https://github.com/mwaqaskh/waqas_docker-assignment/assets/39801941/1d8670e6-a957-418a-bc13-6c49c2fd2536)


# Step 7 
I have succfully created the README.ms file and have logged the details of each step in this file

# Step 8
