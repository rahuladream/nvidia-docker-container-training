### Verifying –gpus option under docker run
Also if ndivia-docker-container toolkit missing

docker run --help | grep -i gpus
      --gpus gpu-request               GPU devices to add to the container ('all' to pass all GPUs)
      
#### How to fix this?

#### Install nvidia-container-toolkit

#### Add the package repositories
$ distribution=$(. /etc/os-release;echo $ID$VERSION_ID)
$ curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | sudo apt-key add -
$ curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | sudo tee /etc/apt/sources.list.d/nvidia-docker.list

# Install and reload Docker
$ sudo apt-get update && sudo apt-get install -y nvidia-container-toolkit
$ sudo systemctl restart docker
