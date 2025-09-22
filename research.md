---
layout: page
title: Research
# subtitle: 
---

### Cacheflow: Cross-layer KV Cache Parallelism for LLM Serving at Scale
August 2024 - present; Supervisor: [Fan Lai](https://www.fanlai.me/) @ GAEA Lab
-	Identified KV cache as a growing memory and latency bottleneck in large-scale LLM serving systems.
-	Developed novel cross-layer parallelism framework combining token-wise, layer-wise, and multi-GPU parallelism for hybrid KV cache restoration. 
-	Implemented SLO-aware scheduling to manage I/O contention across requests, batches, and models while maintaining performance guarantees. 
-	Addressed limitations of existing systems in long-context scenarios and concurrent restoration workloads.
-	Designed cross-layer management system that optimally balances computation and communication for KV cache restoration at cluster scale.

### Tempo: Application-aware LLM Serving with Mixed SLO Requirements
August 2024 - present; Supervisor: [Fan Lai](https://www.fanlai.me/) @ GAEA Lab
-	Identified diverse SLO requirements across three LLM request patterns: latency-sensitive, throughput-intensive, and collective requests with varying performance needs.
-	Developed SLO-aware scheduler that maximizes service gain by allocating just enough bandwidth to meet individual SLOs while preserving residual capacity for other requests.
-	Implemented hybrid approach using quantile regression forests for response length estimation and dependency-graph matching for collective request coordination.
-	Created service density-based prioritization algorithm that balances requests across different SLO constraints without starving low-priority workloads.
-	Achieved 1.3×-8.3× improvement in service gain and 4.0×-10.3× improvement in SLO goodput compared to existing systems across diverse workloads and models.


### Andes: Defining and Enhancing Quality-of-Experience in LLM Serving
May 2023 – April 2024; Supervisor: [Mosharaf Chowdhury](https://www.mosharaf.com/) @ Symbiotic Lab
Here’s a more concise version:
- Identified that in LLM text-streaming services, generating text faster than user reading speed is crucial for enhancing user experience, addressing gaps in prior metrics.
- Defined Quality of Experience (QoE) in LLM serving by tracking each step of text generation and monitoring the overall user experience throughout the entire streaming process.
- Formulated QoE optimization as a knapsack problem and developed a scheduling algorithm to maximize QoE by efficiently allocating resources.
- Built Andes, an LLM serving system on top of vLLM, integrating the scheduling algorithm to enhance QoE in real-time LLM services.
- Co-authored the paper “Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services” as second author.


# Publications
- [Andes: Defining and Enhancing Quality-of-Experience in LLM-Based Text Streaming Services](https://arxiv.org/abs/2404.16283); Preprint, 2024; Jiachen Liu, **Zhiyu Wu**, Jae-Won Chung, Fan Lai, Myungjin Lee, Mosharaf Chowdhury
-	[Tempo: Application-aware LLM Serving with Mixed SLO Requirements](https://arxiv.org/abs/2504.20068); Preprint, 2025; submit to SOSP 25; Wei Zhang*, **Zhiyu Wu***, Yi Mu, Banruo Liu, Myungjin Lee, Fan Lai 
-	[The ML.ENERGY Benchmark: Toward Automated Inference Energy Measurement and Optimization](https://arxiv.org/abs/2505.06371); NeurIPS spotlight, 2025; Jae-Won Chung, Jiachen Liu, Jeff J Ma, Ruofan Wu, Oh Jun Kweon, Yuxuan Xia, **Zhiyu Wu**, Mosharaf Chowdhury