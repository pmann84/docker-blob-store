# docker-blob-store
## Overview
This is simply a docker compose file so that you can launch multiple ready made blob stores in a single to test your cloud storage applications.

## Build and Run
Simply change directory to the checkout root and run
```docker-compose up -d```
this will download and spin up a container with each container running an instance of Azurite blob store

## Accessing the container 
You can access a bash shell of the container by running 
```docker run -it kafka-zookeeper /bin/bash```

## Using the Blob Stores
The blob stores are exposed on the ports listed in the compose file, in this case blobstore1 is exposed on port 11000, with queue and table ports ending in 1 and 2. These can be viewed in the [Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/) by connecting to Azure Storage and selecting `local storage emulator`. Then pass in the ports and you should be able to administer your blob store through that.
