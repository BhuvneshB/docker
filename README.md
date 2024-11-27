# DOCKER INSTALLATION

Learnt from [**https://ska-telescope.gitlab.io/src/ska-src-training-containers/**](https://ska-telescope.gitlab.io/src/ska-src-training-containers/)

## For Ubuntu/Debian
Open terminal and run following commands to install Docker:
1. Uninstall older versions of Docker. Older versions of Docker were called docker, docker.io, or docker-engine.
   
   ```bash
   sudo apt-get remove docker docker-engine docker.io containerd runc
   ```
   
3. Update the apt package index and install packages to allow apt to use a repository over HTTPS:

    ```bash
   sudo apt-get update
    ```

    ```bash
   sudo apt-get install  ca-certificates curl  gnupg lsb-release
    ```
    
5. Add Docker’s official GPG key:

    ```bash
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg  | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    ```
    
 7. Use the following command to set up the stable repository:

    ```bash
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```
    
9. Update the apt package index, and install the latest version of Docker Engine and containerd:

    ```bash
   sudo apt-get update
    ```
      
    ```bash
   sudo apt-get install docker-ce docker-ce-cli containerd.io
    ```
    
8. Run a test image to check installation:
      
     ```bash
   sudo docker run hello-world
     ```

## Use docker
Example docker file ```pyglow``` : [IRI pyglow](https://github.com/timduly4/pyglow)
1. Install the image in docker/making a container of the image
   
   ```bash
   docker build -t <image_name> .
   ```
   [Note=> Image name should be in lower case]
   
3. Run the unit tests within the container via:

   ```bash
   docker run <image_name>
   ```
      
5. To enter in Docker container (bash):
   
   ```bash
   docker run -it <image_name> bash
   ```
   
Ex. 
```bash
docker run -it pyglow bash
```

