---
layout: page
title: Software
permalink: /software/
description: Open-source software and platforms developed by Madduri Lab for privacy-preserving federated learning, genomics analysis, and scientific workflows.
nav: true
nav_order: 4
---

Our lab develops open-source software and platforms that advance privacy-preserving machine learning, large-scale genomics analysis, and scientific workflow automation. Below are our major software projects.

---

## APPFL - Argonne Privacy Preserving Federated Learning

<div class="row">
<div class="col-sm-12">

An open-source framework for privacy-preserving federated learning that enables collaborative AI model development without centralizing sensitive data.

**Key Features:**
- Differential privacy and secure aggregation
- Support for heterogeneous computing environments (cloud, HPC, edge)
- Flexible communication backends (MPI, gRPC)
- Policy-driven governance and access control
- Integration with PyTorch and other ML frameworks

**Applications:** Healthcare AI, genomics, smart grid optimization, COVID prediction models

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% include repository/repo.liquid repository="APPFL/APPFL" %}
</div>

</div>
</div>

---

## APPFLx - Federated Learning as a Service

A production-ready platform that provides privacy-preserving federated learning capabilities as a managed service.

**Highlights:**
- Deployed on AWS with enterprise-grade security
- Used by NIH-funded Bridge2AI program
- Supports cross-institutional collaborations
- Web-based interface for non-expert users
- End-to-end encryption and secure enclaves

**Access:** [appflx.link](https://appflx.link)

---

## MapperTrac

A massively parallel, portable, and reproducible tractography pipeline for neuroimaging analysis.

**Features:**
- Scalable across HPC clusters
- Reproducible containerized workflows
- Published in Neuroinformatics (2024)

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% include repository/repo.liquid repository="LLNL/mappertrac" %}
</div>

---

## Globus Genomics

A next-generation sequencing analysis service built on Galaxy, Globus, and Amazon Web Services that democratized large-scale genomics analysis.

**Impact:**
- Used by thousands of researchers worldwide
- Analyzed millions of genomes
- Led to successful commercial spinoff (funded by UChicago Polsky Center, NIH, NSF SBIR)
- Established patterns for Science-as-a-Service platforms

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
{% include repository/repo.liquid repository="globusgenomics/genomics-galaxy" %}
</div>

---

## Historical Projects

### caGrid - Cancer Biomedical Informatics Grid

Grid infrastructure for secure data sharing and high-performance workflows in cancer research, adopted by multiple NCI-designated cancer centers.

[View on GitHub](https://github.com/NCIP/cagrid)

### Reliable File Transfer (RFT)

The first "grid service" created for Wide Area Networks, part of Globus Toolkit versions 3 and 4. Integral component for data staging in/out of HPC resources, adopted by thousands of institutions worldwide.

---

## Getting Started

Interested in using our software? Here are some resources:

- **APPFL Documentation:** [appfl.ai](https://appfl.ai)
- **APPFLx Access:** [appflx.link](https://appflx.link)
- **Questions?** Contact us at [rkmadduri@anl.gov](mailto:rkmadduri@anl.gov)

We welcome contributions and collaborations. See individual repositories for contribution guidelines.
