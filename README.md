# DOCKER INSTALLATION

Learnt from [**https://ska-telescope.gitlab.io/src/ska-src-training-containers/**](https://ska-telescope.gitlab.io/src/ska-src-training-containers/)

## For Ubuntu/Debian
Open terminal and run following commands to install Docker:
1. Uninstall older versions of Docker. Older versions of Docker were called docker, docker.io, or docker-engine.
   
   ```sudo apt-get remove docker docker-engine docker.io containerd runc```
   
2. Update the apt package index and install packages to allow apt to use a repository over HTTPS:

    ```sudo apt-get update```

    ```sudo apt-get install  ca-certificates curl  gnupg lsb-release```
    
3. Add Docker’s official GPG key:

    ```curl -fsSL https://download.docker.com/linux/ubuntu/gpg  | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg```
    
 4. Use the following command to set up the stable repository:

    ```echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null```
    
5. Update the apt package index, and install the latest version of Docker Engine and containerd:

    ```sudo apt-get update```
      
    ```sudo apt-get install docker-ce docker-ce-cli containerd.io```
    
6. Run test image to check installetion:
      
     ```sudo docker run hello-world```


