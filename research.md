---
layout: page
title: Research
# subtitle: 
---

### Improving Service Level Objective (SLO) of Large Language Model Serving
July 2024 - present; Supervisor: [Fan Lai](https://www.fanlai.me/) @ GAEA Lab
- Classify LLM serving requests into three categories based on unique system objectives:
  - Latency-Intensive: For streaming use case, ensuring fluent reading experience.
  - Throughput-Intensive: Only focus on the job completion time (JCT).
  - Bulk Requests: Large groups of requests submitted together, with collective completion time as the priority.
- Define Service Level Objectives (SLO) for each request type:
  - Latency-Intensive: SLO based on Quality of Experience (QoE).
  - Throughput-Intensive: Extended deadlines, calculated as the time it runs alone on the machine multiplied by a scaling ratio.
  - Bulk Requests: SLO based on the deadline of the last request in the group.
- Develop an SLO-aware scheduling policy using length prediction to optimize job completion time (JCT) and improve user experience in LLM inference.
  - The policy combines DAG scheduling and two-dimensional knapsack scheduling, ensuring efficient resource allocation to meet SLOs across different request types.


### Defining and Enhancing Quality-of-Experience in LLM Serving
May 2023 – April 2024; Supervisor: [Mosharaf Chowdhury](https://www.mosharaf.com/) @ Symbiotic Lab
Here’s a more concise version:
- Identified that in LLM text-streaming services, generating text faster than user reading speed is crucial for enhancing user experience, addressing gaps in prior metrics.
- Defined Quality of Experience (QoE) in LLM serving by tracking each step of text generation and monitoring the overall user experience throughout the entire streaming process.
- Formulated QoE optimization as a knapsack problem and developed a scheduling algorithm to maximize QoE by efficiently allocating resources.
- Built Andes, an LLM serving system on top of vLLM, integrating the scheduling algorithm to enhance QoE in real-time LLM services.
- Co-authored the paper “Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services” as second author.


# Publications
- [Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services](https://arxiv.org/abs/2404.16283); Preprint, 2024; Jiachen Liu, **Zhiyu Wu**, Jae-Won Chung, Fan Lai, Myungjin Lee, Mosharaf Chowdhury