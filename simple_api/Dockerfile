#Us:ing official python runtime base image
FROM python:2.7-stretch

# The person who write the Dockerfile
MAINTAINER Gerold (geroldsiewe@gmail.com)

# ADD source code of API in the container at the root "/" path
COPY student_age.py /

# install of package
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv

#Mount Volumes
VOLUME /data

# Make port 5000 available to interact with this API
EXPOSE 5000

# Define our command to be run when launching the container
CMD [ "python", "./student_age.py" ]

