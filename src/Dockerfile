# The base image
FROM alpine:latest

# Install Python and pip
RUN apk update && apk add python3 py3-pip

# Install Python modules needed by the Python app
COPY requirements.txt /usr/src/app/
RUN pip3 install --no-cache-dir -r /usr/src/app/requirements.txt

# Copy files for the app required to run
COPY app.py /usr/src/app/

# Declare the port number the container should expose
EXPOSE 5000

# Run the application
CMD [ "python3", "/usr/src/app/app.py" ]
