#### Installing tensorflow basically pull the container

got to the link https://ngc.nvidia.com/catalog/containers/nvidia:tensorflow


pull the container according to your use 
  Note: this will take around 1-2h or more according to the system setup
  
#### Procedure

Select the Tags tab and locate the container image release that you want to run.

In the Pull Tag column, click the icon to copy the docker pull command.

Open a command prompt and paste the pull command. The pulling of the container image begins. Ensure the pull completes successfully before proceeding to the next step.

Run the container image.

If you have Docker 19.03 or later, a typical command to launch the container is:

```docker run --gpus all -it --rm -v local_dir:container_dir nvcr.io/nvidia/tensorflow:xx.xx-tfx-py3```

  -> local_dir => is the directory or file from your host system (absolute path) that you want to access from inside your container. /media/model_data
  -> container_idr =>  is the target directory when you are inside your container. For example, /data/model_data
  -> xx.xx is the container version. For example, 20.01. , tfx is the version of TensorFlow. For example, tf1 or tf2.
  
At this point of command, your docker is already running into the machine, to verify the tensorflow
open python terminal

>> import tensorflow as tf
>> print(tf.__version__)
>> tf.test.is_gpu_available(
    cuda_only=False,
    min_cuda_compute_capability=None
)
