# My_Learning_Docker
My Notes on DOCKER

## Installation
* #### Docker for Windows - 

  **NOTE**: Turn the Hyper-V (already built-in into Win 10) on using `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All`. [SOURCE](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v)
  
  Follow the steps:
  * Download from here - https://store.docker.com/editions/community/docker-ce-desktop-windows
  * Then follow the installation steps
  * PATH added - "C:\Program Files\Docker\Docker\Resources\bin" in the environment variables
  * To start, click on the docker icon (start-menu/desktop). 
  * Login to the docker engine and create images, containers
  * use the commands - `docker run hello-world`(run hello-world from the docker hub) , `docker ps`(list of containers) , `docker images`(list of images)

* #### Docker for Linux (Ubuntu) - 
  Follow the steps:
  * Uninstall old versions (if any) - `$ sudo apt-get remove docker docker-engine docker.io` 
  * Set up the docker repository:
    * Update the apt package index: `$ sudo apt-get update`
    * Install packages to allow apt to use a repository over HTTPS:
      ```
      $ sudo apt-get install \
        apt-transport-https \
        ca-certificates \
        curl \
        software-properties-common
      ```
    * Add Docker’s official GPG key:<br/>
      `$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
      
      Verify using `$ sudo apt-key fingerprint 0EBFCD88`
    * Download the stable repository
      ```
      $ sudo add-apt-repository \
         "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
         $(lsb_release -cs) \
         stable"
      ```
      
   * Install DOCKER CE:
      `$ sudo apt-get update`
      
      `$ sudo apt-get install docker-ce` (latest version)
      
      `$ sudo docker run hello-world`
      
   * Uninstall DOCKER CE:
      * Remove all the images, containers using `$ sudo rm -rf /var/lib/docker`
      * Uninstall the docker-ce using `$ sudo apt-get purge docker-ce`
      * Remove the packages not required anymore using `$ sudo apt autoremove`
      
  [**SOURCE**](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
  
* 
  
  
