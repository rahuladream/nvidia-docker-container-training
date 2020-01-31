## Installing Nvidia ngc container 

### Setup using the repository

1. Update the apt package index
``` sudo apt-get update```

2. Install packages to allow apt to use a repository over HTTPS
```sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common```
    
 3. Add Docker's official GPG Key:
 ```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```

 Verify that you now have the key with the fingerprint 9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88, by searching for the last 8 characters of the fingerprint.
 
 
 4. According to ubuntu distribution `lst_release -cd` use the command
    1.(amd64) ```sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"```
   2. (armhf) ```sudo add-apt-repository \
   "deb [arch=armhf] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"```
   
