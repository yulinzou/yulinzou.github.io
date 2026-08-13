---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Education
* Ph.D. in Computer Science, Nanyang Technological University, Jan 2024 - expected 2028
  * Supervisors: Asst. Prof. Dmitrii Ustiugov (NTU) and Dr. Luo Tao (A*STAR)
* B.Eng. (Honours, Highest Distinction) in Computer Engineering, Nanyang Technological University, Aug 2018 - May 2022
  * Elective focus on Artificial Intelligence, CGPA 4.51/5.00

## Research Interests
* Efficient multimodal LLM and video diffusion model serving
* Streaming video analytics
* Long video generation

## Technical Skills
* Languages & systems: Python, Go, C; Linux, Git, Docker, Kubernetes
* LLM & VDM infrastructure: PyTorch, vLLM, SGLang Diffusion; LMCache, KV cache management, paged memory allocation, distributed serving
* Performance & profiling: CUDA, GPU benchmarking, FlashAttention, paged/radix attention

## Publications & Preprints
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

## Research Experience
**Ph.D. Researcher**, NTU College of Computing and Data Science, Jan 2024 - Present

*Memory management for autoregressive long video generation*, 2026 - Present
* Ongoing work on KV cache memory management for autoregressive video diffusion transformers, where cache growth over long rollouts bounds both achievable video length and the number of concurrent sessions a GPU can host.
* Prototyping on Wan2.1-based causal video models and evaluating serving-throughput metrics against recent long-video memory baselines.

*CodecSight: codec-guided token pruning and KV cache reuse for streaming VLM serving*, 2025 - Present
* First-authored a training-free, model-agnostic serving layer that wraps unmodified VLMs and reuses codec metadata (motion vectors, frame types, residuals) already produced during decode to prune visual patches before ViT encoding and to reuse KV cache across sliding-window prefill.
* Cut visual tokens by 85% and prefill FLOPs by 87% at matched accuracy, for 3&times; end-to-end throughput on InternVL3-14B and Qwen3-VL-32B; evaluated on UCF-Crime streaming workloads including multistream scaling.
* Built on vLLM and LMCache with single-pass decode and metadata extraction via PyNvVideoCodec/NVDEC; filed a technology disclosure with NTUitive for commercialisation.

## Industry Experience
**Research Engineer**, Continental-NTU Corporate Lab, Jun 2022 - Dec 2023
* Built a real-time bus driver safety monitoring system fusing trajectory, speed profiling, and multi-sensor streams; deployed across several local bus lines.
* Designed the ML and data pipelines for incident detection and driver risk prediction, from ingestion and temporal fusion through inference deployment.

**Algorithm Engineer Intern**, Didi Global Inc., Jun 2021 - Aug 2021
* Improved pricing algorithms for South American markets using causal inference and uplift modelling.
* Built budget control and cost prediction models using neural networks and domain adaptation.

**Software Engineer Intern**, Shopee TechOps, May 2020 - Dec 2020
* Developed internal engineering resource management tools and backend components to optimise CI/CD workflows.

## Awards
* A*STAR Graduate Scholarship, Jan 2024 - Jan 2028
* NTU Science & Engineering Scholarship, Aug 2018 - May 2022

## Teaching
* AY26/27 S1: SC2005 Operating Systems, Teaching Assistant (tutorials)
* AY25/26 S1: SC2005 Operating Systems, Teaching Assistant (lab supervision)
* AY24/25 S2: SC1006 Computer Organisation & Architecture, Teaching Assistant (lab supervision)
* AY24/25 S1: SC2001 Algorithms, Teaching Assistant (lab supervision)
