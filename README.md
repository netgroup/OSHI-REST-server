# OSHI REST Server

## Introduction

Server for common OSHI REST endpoints, currently offering:
- generation of .png for traffic statistics from .rrd database files

## Setup
You can use the OSHI-REST-server.sh script to setup and run this project.

The available options are:
- --mode (or -m) to choose the running mode: setup, run

1. Download the VirtualBox VM from [Uniroma2 Netgroup](http://netgroup.uniroma2.it/twiki/bin/view/Oshi/WebHome#AnchorSoftDown)
2. After starting the VM, run the following command as user `user`:
    ```
    cd /home/user/workspace
    
    git clone https://github.com/netgroup/OSHI-REST-server.git
    ```
3. Setup the environment:
    ```
    cd /home/user/workspace/OSHI-REST-server
    
    sudo ./OSHI-REST-server.sh --mode setup
    ```
    
## Run instructions

1. Run the server:
    ```
    cd /home/user/workspace/OSHI-REST-server
    
    ./OSHI-REST-server.sh --mode run
    ```

## Access the server
You can find an instance of Swagger UI running @ [localhost:8000](http://localhost:8000/docs/) where localhost is the host running this server, on the 8000 port.

For the .png generation service, the OSHI-monitoring tool should be up and running, see https://github.com/netgroup/OSHI-monitoring

## Available settings
### OSHI-REST-server/oshi_rest_server/rrdgraph_server/config.py
- RRD_FILE_PATH: set the path where the RRD files are stored. This can be set to where OSHI-monitoring stores RDD files.