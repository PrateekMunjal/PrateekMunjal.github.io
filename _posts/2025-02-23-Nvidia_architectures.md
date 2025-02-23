---
layout: post
title: "Nvidia's New GPU Architectures: GB200"
date: 2025-02-24
categories: [Nvidia, AI, GPUs]
tags: [Blackwell, Hopper]
---

This post examines Nvidia’s new GPU architecture: GB200.

## Parallelism in AI Training

In AI model training, particularly with large language models (LLMs) and diffusion models, parallelism refers to the ability to perform multiple operations simultaneously to enhance computational efficiency. Achieving effective parallelism is essential, as it allows workers to tackle numerous problems at once. It is important to note that the speed of processing becomes irrelevant without sufficient workload, therefore thw workers should have enough work always inorder to optimize the performance. Nvidia's latest GPU architectures: GB200, are designed to maximize operational throughput by performing as many computations as possible at high speeds. These architectures incorporate high bandwidth capabilities, enabling them to efficiently work with distributed methods like GEMM.

### Overview of Nvidia GPU Architectures

#### GB200: The Blackwell Architecture

To meet the growing demands for large scale training and inference of AI models such as LLMs, Nvidia has recently launched a new GPU architecture. This architecture is among the largest GPUs globally and claims to be energy efficient compared to Nvidia’s Hopper based GPUs. The Blackwell architecture is named after David Blackwell, a renowned mathematician and statistician, especially known for the Rao Blackwell theorem.

### Key Features
1. The Blackwell architecture is built with 208 billion transistors which is 2.5x amount of transistors in NVIDIA Hopper GPUs

2. This was achieved by Nvidia working with TSMC’s 4NP process, performance optimized process for chip design (4nm) for Blackwell, compared to the 4N(without P) process used in Hopper architecture. 

3. With 4NPs of TSMC, Nvidia enables the Blackwell gpu to achieve the highest compute ever on a single chip i.e 20 petaFLOPs (for FP4 where as it is only 4 Petaflops approximately with Nvidia H100 and NVIDIA H200[1,2]). With more flops, one can expect both training and inference to run faster as GPUs can handle more computations per second.

4. As most large scale models are trained on substantial amounts of data, they require large models loaded in VRAM, along with sizable optimizer states. Typically, distributed strategies such as FSDP, Zero3-DeepSpeed, or simple tensor parallelism are employed to facilitate their training.

5. These strategies vary in how they shard the model parameters, optimizer, and gradients. However, since all of them shard in one way or another, it's crucial to consider how quickly the processors communicate and transfer data—such as model gradients, optimizer states, and other information—between each other. This is where Blackwell leverages HBM3e, which provides higher bandwidth (8 TB/s compared to 4.8 TB/s[2]) and increased VRAM (192 GB vs. 141 GB[2]).

### Practical Takeaways

- **Faster Training**: High bandwidth, High Memory, More FLOPs per second, and 5th gen NVLink

- **More Efficient Inference**: Same as Above

- **Optimized Resource Utilization**: Leveraging the energy efficiency of the Blackwell architecture can lead to reduced operational costs and a smaller carbon footprint, which is increasingly important in the field of AI.

References
- [1] H100: https://www.nvidia.com/en-us/data-center/h100
- [2] H200: https://www.nvidia.com/en-us/data-center/h200
