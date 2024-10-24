# Use an official Python runtime as a parent image
FROM python:3.10-slim

RUN apt-get update
RUN apt install tcpdump libpcap0.8-dev

# Set the working directory in the container
WORKDIR /root

# Install any needed packages specified in requirements.txt
RUN pip install scapy

ENTRYPOINT ["tail", "-f", "/dev/null"]