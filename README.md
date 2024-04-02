# Cloud GPU Handbook 

* Author: [Ndamulelo Nemakhavhani](https://linkedin.com/in/ndamulelonemakhavhani)

**Motivation** - I find the information about running GPUs in the public clouds to be very fragmented and presented in an unfriendly way. I want to create a catalog of cloud GPU offerings that is easy to read and compare. The objective is for users to get up and running with a GPU for training their models as quickly as possible. This repository aims to provide an easy-to-understand catalog of common cloud GPU instances, their specifications, pricing, and essential setup information.
Whether you are a Data Scientist, Machine Learning Engineer, or a Curious Learner, this handbook aims to save you time and effort so you get started with your GPU workloads as quickly as possible.

> **Updates:** I will try to keep this catalog up to date with the latest information. If you find any errors or have any suggestions, please feel free to create an issue or a pull request. Contributions are welcome.

## Key features:

- Comparative tables of GPU instances from major players: [AWS](https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html), [Google Cloud](https://cloud.google.com/compute/docs/gpus), [Microsoft Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes-gpu), and other providers
- Installation tips for NVIDIA drivers and CUDA on different operating systems
- Overview of specialized GPU offerings and notebook-based GPU platforms

## Public Cloud GPU Offerings

* Note that we only list the most popular options for experimentation and training. For production, you should probably consider the full range of options available from each provider on their respective websites.

```yaml
table:
  - headers
    - Cloud Provider
    - GPU Type
    - GPU Memory
    - vCPU
    - RAM
    - Price
    - Technical Name
    - Link
  - rows
    - Cloud Provider: AWS
      GPU Type: NVIDIA Tesla V100
      GPU Memory: 16GB
      vCPU: 8
      RAM: 61GB
      Price: $3.06/hr
      Technical Name: p3.2xlarge
      Link: https://aws.amazon.com/ec2/instance-types/p3/
    - Cloud Provider: GCP
      GPU Type: NVIDIA Tesla V100
      GPU Memory: 16GB
      vCPU: 8
      RAM: 61GB
      Price: $2.48/hr
      Technical Name: n1-highmem-8
      Link: https://cloud.google.com/compute/docs/gpus
    - Cloud Provider: Azure
      GPU Type: NVIDIA Tesla V100
      GPU Memory: 16GB
      vCPU: 6
      RAM: 112GB
      Price: $3.06/hr
      Technical Name: Standard_NC6s_v3
      Link: https://docs.microsoft.com/en-us/azure/virtual-machines/ncv3-series
```

### NVIDIA Drivers & CUDA Installation

* NVIDIA drivers and CUDA installation are required to run GPU workloads on the cloud. The following commands can be used to install the drivers and CUDA on Ubuntu.

```yaml
table:
  - headers
    - GPU Type
    - Minimum NVIDIA Driver Version
    - Maximum NVIDIA Driver Version 
    - Minimum CUDA Version
    - Maximum CUDA Version
    - Comments
  - rows
    - GPU Type: NVIDIA Tesla V100
      Minimum NVIDIA Driver Version: 418.87
      Maximum NVIDIA Driver Version: 460.32
      Minimum CUDA Version: 10.0 
      Maximum CUDA Version: 11.0
      Comments: The NVIDIA driver and CUDA version requirements are subject to change. Please check the NVIDIA website for the latest information.
```

## Specialized GPU Offerings

* [Paperspace](https://www.paperspace.com/)
* [RunPod](https://www.runpod.io/) 
* [Jarvis Labs](https://jarvislabs.ai/)
* [Lambda GPU Cloud](https://lambdalabs.com/service/gpu-cloud)
* [Coreweave](https://www.coreweave.com/)

## Notebook GPU Offerings

* Note that we only list the most suitable options for experimentation and training. For production, you should consider the full range of options available from each provider on their respective websites.
* Most of these providers provide generous free tiers for experimentation and learning for a limited time.

* [Google Colaboratory](https://colab.research.google.com/)
* [Kaggle](https://www.kaggle.com/code)
* [AWS SageMaker Studio Lab](https://studiolab.sagemaker.aws/) 
* [Deepnote](https://deepnote.com/)
* [Gradient](https://gradient.run/)

# Tips

* Always stop your instances when not in use to avoid unnecessary charges.
* Use spot instances for experimentation and training to save costs.
* Monitor your usage and set up billing alerts to avoid unexpected charges.
* Use version control to track your experiments and share your work with others.

# Contributing

- Contributions, suggestions, and issue reports are welcome from the community to make Cloud **GPU Handbook** a valuable resource for everyone interested in leveraging the power of GPUs in the cloud.

# Related Links

* [NVIDIA GPU Cloud](https://www.nvidia.com/en-us/gpu-cloud/)
* [NVIDIA NGC Catalog](https://ngc.nvidia.com/catalog)
* [TensorFlow GPU Support](https://www.tensorflow.org/install/gpu)
* [PyTorch GPU Support](https://pytorch.org/get-started/locally/)
