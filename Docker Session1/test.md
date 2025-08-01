# **Session 1 Tasks**

## **Task 1: Host Volume Mapping**

> Map a folder from your host system to a folder inside a Docker container.  
Create a file inside the container and verify its presence from the host.

- Make new directory at the home directory

``` bash
mkdir ~/myVolume
```

- Run new container with host volume mapping

``` bash
docker run -it -v ~/myVolume:/home/test --name test ubuntu /bin/bash
```

<br>



## **Task 2: Anonymous Volume**  

>Use Docker’s default anonymous volume location to create a container.  
Create a file inside the container and verify its existence.

- Run new container with Anonymous volume mapping
``` bash
docker run -it -v /home/test --name test ubuntu /bin/bash
```

<br>


## **Task 3: Named Volume**  

>Create a named volume (e.g., sprints-volume), map it to a container,  
and create a file inside the container. Verify the file exists.

 
- Run new container with Named volume mapping
``` bash
docker run -it -v testVolume:/home/test --name test ubuntu /bin/bash
```