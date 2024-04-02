# Cloud GPU Handbook [WIP]

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

| Cloud Provider | GPU Type                  | GPU Memory | vCPU | RAM    | Price*    | Technical Name      | Link                                                                                      |
|----------------|---------------------------|------------|------|--------|-----------|---------------------|-------------------------------------------------------------------------------------------|
| AWS            | NVIDIA Tesla V100         | 16GB       | 8    | 61GB   | $3.06/hr  | p3.2xlarge          | https://aws.amazon.com/ec2/instance-types/p3/                                             |
| AWS            | NVIDIA Tesla T4           | 16GB       | 4    | 16GB   | $0.82/hr  | g4dn.xlarge         | https://aws.amazon.com/ec2/instance-types/g4/                                             |
| AWS            | NVIDIA Tesla A10G         | 24GB       | 4    | 16GB   | $1.35/hr  | g5.xlarge           | https://aws.amazon.com/ec2/instance-types/g5/                                             |
| GCP            | NVIDIA Tesla V100         | 16GB       | 8    | 61GB   | $2.48/hr  | n1-highmem-8        | https://cloud.google.com/compute/docs/gpus                                                |
| GCP            | NVIDIA Tesla T4           | 16GB       | 4    | 16GB   | $0.95/hr  | n1-standard-4       | https://cloud.google.com/compute/docs/gpus                                                |
| GCP            | NVIDIA Tesla A100         | 40GB       | 12   | 85GB   | $4.10/hr  | a2-highgpu-1g       | https://cloud.google.com/compute/docs/gpus                                                |
| Azure          | NVIDIA Tesla V100         | 16GB       | 6    | 112GB  | $3.06/hr  | Standard_NC6s_v3    | https://docs.microsoft.com/en-us/azure/virtual-machines/ncv3-series                       |
| Azure          | NVIDIA Tesla T4           | 16GB       | 4    | 28GB   | $0.90/hr  | Standard_NC4as_T4_v3| https://docs.microsoft.com/en-us/azure/virtual-machines/nct4-v3-series                    |
| Azure          | NVIDIA Tesla A100         | 40GB       | 8    | 56GB   | $3.80/hr  | Standard_NC8as_A100_v4 | https://docs.microsoft.com/en-us/azure/virtual-machines/nca100-v4-series               |

Table 1: Compare popular NVIDIA GPUs from AWS, GCP, and Azure for training Deep Learning & AI models. (**Note:** The prices are subject to change, check the provided links for the latest prices)

### NVIDIA Drivers & CUDA Installation

* NVIDIA drivers and CUDA installation are required to run GPU workloads on the cloud. The following commands can be used to install the drivers and CUDA on Ubuntu.
* Most cloud providers already offer managed services that come pre-installed with all the necessary dependencies - If these meet your needs, consider using them instead

| GPU Type                  | Minimum NVIDIA Driver Version | Maximum NVIDIA Driver Version | Minimum CUDA Version | Maximum CUDA Version |
|---------------------------|-------------------------------|-------------------------------|----------------------|----------------------|
| NVIDIA Tesla V100         | 418.87                        |                               | 10.0                 |                      |
| NVIDIA Tesla T4           | 410.79                        |                               | 10.0                 |                      |
| NVIDIA Tesla A10G         | 418.87                        |                               | 10.0                 |                      |
| NVIDIA Tesla A100 40GB    | 450.36                        |                               | 11.0                 |                      |
| NVIDIA Tesla A100 80GB    | 450.36                        |                               | 11.0                 |                      |
| NVIDIA Tesla P100         | 410.48                        |                               | 9.0                  |                      |
| NVIDIA Tesla K80          | 375.26                        |                               | 8.0                  |                      |
| NVIDIA GeForce RTX 2080 Ti| 411.31                        |                               | 10.0                 |                      |
| NVIDIA GeForce RTX 3090   | 452.39                        |                               | 11.0                 |                      |


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

# Disclaimer

> Please note that the information about the GPU offerings, such as GPU type, GPU memory, vCPU, RAM, price, and technical name, varies across different cloud providers and may change over time. Therefore, it's always a good idea to check the official websites for the most up-to-date and detailed information. Also, the prices listed are subject to change and may vary based on the region and other factors. Always check the provider's pricing page for the most accurate and current pricing information. 

# Related Links

* [PyTorch GPU Support](https://pytorch.org/get-started/locally/)
* [TensorFlow GPU Support](https://www.tensorflow.org/install/gpu)
* [NVIDIA GPU Cloud](https://www.nvidia.com/en-us/gpu-cloud/)
