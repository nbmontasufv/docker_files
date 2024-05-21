# Use an official Python runtime as a parent image
FROM nvidia/cuda:11.8.0-cudnn8-devel-ubuntu22.04 
FROM continuumio/anaconda3:latest

# Set the working directory in the container to /app
WORKDIR /home/ceiec/app

# Install any needed packages specified in requirements.txt
RUN apt-get update && apt-get install -y \
    python3-pip \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install --upgrade pip

RUN apt-get update

# Create the environment:
#COPY environment.yml .
#RUN conda env create -f environment.yml

#Make RUN commands use the new environment:
#RUN echo "conda activate gaussian_splatting" >> ~/.bashrc
#SHELL ["conda", "run", "-n", "gaussian_splatting", "/bin/bash", "-c"]
### OR FOR WINDOWS: #####
#CMD ["conda", "run", "-n", "gaussian_splatting", "cmd", "/S", "/C"]

#COPY requirements.txt ./ 

# Install any needed packages specified in requirements.txt
#RUN pip install -r requirements.txt

# Make port 2222 available to the world outside this container
#EXPOSE 8000