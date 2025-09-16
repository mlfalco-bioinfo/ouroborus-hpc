# Introduction to the Ouroboros HPC Project

Welcome to the start of your journey in creating a personal High-Performance Computing (HPC) cluster. This project, nicknamed "Ouroboros," is designed to be a complete and practical guide, from preparing your computer to running a distributed bioinformatics pipeline and professionally monitoring your environment.

## Philosophy

The name **Ouroboros** was chosen for its representation of cycles and self-sufficiency. Our goal is to create a computing ecosystem that is:
-   **Self-Contained:** It lives entirely within your host computer, with no cloud costs.
-   **Self-Referential:** The cluster nodes know each other and work together, managed by a central mind (Slurm).
-   **Cyclical:** Communication flows from the host to the cluster (for management) and from the cluster to the host/world (to download data and software), completing a cycle.

## Who is This Guide For?

This material is intended for students, researchers, and professionals in the fields of bioinformatics, computational biology, data science, and related areas who wish to:
-   Understand in a practical way how an HPC cluster is structured.
-   Learn to install and configure a job scheduler like Slurm.
-   Gain experience in submitting jobs and using pipeline managers like Nextflow in a distributed environment.
-   Have a robust local development environment to create and test pipelines before deploying them to real supercomputers.

## Final Architecture

By the end of this guide, you will have built the following architecture:

-   **1 Master Node:** Responsible for managing the job queue (Slurm Controller), serving shared files (NFS Server), and hosting the monitoring services (Prometheus + Grafana).
-   **3 Worker Nodes:** Responsible for executing the calculations and tasks of the pipelines (Slurm Daemons).
-   **Private Virtual Network:** An internal network where all nodes communicate in an isolated and efficient manner.
-   **Shared Storage:** A central directory accessible by all nodes, ensuring that data, software, and results are consistent across the entire cluster.

Let's begin!

➡️ **Next Step: [Phase 1: Host Preparation](01_host_preparation.md)**
