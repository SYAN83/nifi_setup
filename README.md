# How To Set Up NiFi

A guide to set up NiFi on an AWS ec2 instance

## Installation

1. Install java and set the **JAVA_HOME** environment varialbe.

2. Create an empty directory `nifi` and cd into it. 

3. Download **nifi**, **nifi toolkit** and **nifi registry** tarballs and unzip them inside the directory:
    ```
    echo "Download nifi"
    wget http://mirror.cc.columbia.edu/pub/software/apache/nifi/1.6.0/nifi-1.6.0-bin.tar.gz && tar xvzf nifi-1.6.0-bin.tar.gz
    echo "Download nifi toolkit"
    wget http://apache.mirrors.tds.net/nifi/1.6.0/nifi-toolkit-1.6.0-bin.tar.gz && tar xvzf nifi-toolkit-1.6.0-bin.tar.gz
    echo "Download nifi registry"
    wget http://mirror.metrocast.net/apache/nifi/nifi-registry/nifi-registry-0.1.0/nifi-registry-0.1.0-bin.tar.gz && tar xvzf nifi-registry-0.1.0-bin.tar.gz
    ```
    
## Starting services

1. To start **nifi** as a service:
  - run `nifi-1.6.0/bin/nifi.sh start` to start the service
  - open inbound port `8080` in the security group of the instance
  - open a web browser and navigate to http://localhost:8080/nifi

2. To start **nifi registry** as a service:
  - run `nifi-registry-0.1.0/bin/nifi-registry.sh start` to start the service
  - open inbound port `18080` in the security group of the instance
  - open a web browser and navigate to http://localhost:18080/nifi-registry


## Setting Up a Secure Apache NiFi Registry

## Setting Up a Secure NiFi to Integrate with a Secure NiFi Registry
