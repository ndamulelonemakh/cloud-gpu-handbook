# Cloud GPU Handbook [WIP]

**Motivation** - I want to create an easy-to-read catalog of common cloud GPU offerings for users to quickly get started with training models or conduct their research. This repository will attempt to provide relevant specifications, pricing, and setup information to save time and effort for Data Scientists, Machine Learning Engineers, Platform Engineers etc.

> **Updates:** I will try to keep this catalog up to date with the latest information. If you find any errors or have any suggestions, please feel free to create an issue or a pull request.

## Key features:

- Comparative tables of GPU instances from major players: [AWS](https://docs.aws.amazon.com/dlami/latest/devguide/gpu.html), [Google Cloud](https://cloud.google.com/compute/docs/gpus), [Microsoft Azure](https://learn.microsoft.com/en-us/azure/virtual-machines/sizes-gpu), and other providers
- Installation tips for NVIDIA drivers and CUDA on different operating systems
- Overview of specialized GPU offerings and notebook-based GPU platforms

## Public Cloud GPU Offerings

* Note that we only list the most popular options for experimentation and training. For production, you should probably consider the full range of options available from each provider on their respective websites.

| Cloud Provider | GPU Model             | GPU Memory | vCPUs | RAM   | Price (USD/hr) | Instance Type         | Link                                                                                      |
|----------------|-----------------------|------------|-------|-------|----------------|-----------------------|-------------------------------------------------------------------------------------------|
| AWS            | NVIDIA Tesla V100     | 16 GB      | 8     | 61 GB | $3.06          | p3.2xlarge            | [AWS p3 Instances](https://aws.amazon.com/ec2/instance-types/p3/)                         |
| AWS            | NVIDIA T4             | 16 GB      | 4     | 16 GB | $0.526         | g4dn.xlarge           | [AWS g4 Instances](https://aws.amazon.com/ec2/instance-types/g4/)                         |
| AWS            | NVIDIA A10G           | 24 GB      | 4     | 16 GB | $1.006         | g5.xlarge             | [AWS g5 Instances](https://aws.amazon.com/ec2/instance-types/g5/)                         |
| AWS            | NVIDIA H100           | 80 GB      | 192   | 2048 GB| $13.46         | p5.48xlarge           | [AWS p5 Instances](https://aws.amazon.com/ec2/instance-types/p5/)                         |
| GCP            | NVIDIA Tesla V100     | 16 GB      | 8     | 52 GB | $2.48          | n1-highmem-8          | [GCP GPU Instances](https://cloud.google.com/compute/docs/gpus)                           |
| GCP            | NVIDIA T4             | 16 GB      | 4     | 15 GB | $0.95          | n1-standard-4         | [GCP GPU Instances](https://cloud.google.com/compute/docs/gpus)                           |
| GCP            | NVIDIA A100           | 40 GB      | 12    | 85 GB | $4.10          | a2-highgpu-1g         | [GCP GPU Instances](https://cloud.google.com/compute/docs/gpus)                           |
| GCP            | NVIDIA H100           | 80 GB      | 96    | 768 GB| $6.98          | a3-highgpu-1g         | [GCP A3 Instances](https://cloud.google.com/compute/docs/gpus/a3)                         |
| Azure          | NVIDIA Tesla V100     | 16 GB      | 6     | 112 GB| $3.06          | Standard_NC6s_v3      | [Azure NCv3 Series](https://learn.microsoft.com/en-us/azure/virtual-machines/ncv3-series) |
| Azure          | NVIDIA T4             | 16 GB      | 4     | 28 GB | $0.90          | Standard_NC4as_T4_v3  | [Azure NC T4 v3 Series](https://learn.microsoft.com/en-us/azure/virtual-machines/nct4-v3-series) |
| Azure          | NVIDIA A100           | 40 GB      | 8     | 56 GB | $3.80          | Standard_NC8as_A100_v4| [Azure NC A100 v4 Series](https://learn.microsoft.com/en-us/azure/virtual-machines/nca100-v4-series) |
| Azure          | NVIDIA H100           | 80 GB      | 120   | 960 GB| $6.98          | Standard_NC96ads_H100_v5| [Azure NC H100 v5 Series](https://learn.microsoft.com/en-us/azure/virtual-machines/nc-h100-v5-series) |

Table 1: Compare popular NVIDIA GPUs from AWS, GCP, and Azure for training Deep Learning & AI models. (**Note:** The prices are subject to change, check the provided links for the latest prices)

> **Note**: Prices are subject to change and may vary by region. Always refer to the official pricing pages for the most current information.

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
| NVIDIA H100               | 515.43                        |                               | 12.0                 |                      |


## Specialized GPU Offerings

* [Paperspace](https://www.paperspace.com/)
* [RunPod](https://www.runpod.io/) 
* [Jarvis Labs](https://jarvislabs.ai/)
* [Lambda GPU Cloud](https://lambdalabs.com/service/gpu-cloud)
* [Coreweave](https://www.coreweave.com/)
* [Vast.ai](https://vast.ai/)
* [Genesis Cloud](https://www.genesiscloud.com/)

## Notebook GPU Offerings

* Note that we only list the most suitable options for experimentation and training. For production, you should consider the full range of options available from each provider on their respective websites.
* Most of these providers provide generous free tiers for experimentation and learning for a limited time.

* [Google Colaboratory](https://colab.research.google.com/)
* [Kaggle Kernels](https://www.kaggle.com/code)
* [AWS SageMaker Studio Lab](https://studiolab.sagemaker.aws/)
- [Gradient by Paperspace](https://www.paperspace.com/gradient)
- [Lightning AI Studio](https://lightning.ai/studios)

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


## Tips

- **Instance Management:** Stop or terminate instances when not in use to avoid unnecessary charges.
- **Spot Instances:** Utilize spot instances for cost savings, but be aware of potential interruptions; they are best suited for fault-tolerant workloads.
- **Billing Alerts:** Set up billing alerts and budgets to monitor and control spending effectively.
- **Version Control:** Use platforms like GitHub or GitLab for version control to facilitate collaboration and track experiments.
