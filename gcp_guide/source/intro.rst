
Google Cloud Overview
=======================

What is GCP?
---------------

Google Cloud Platform (GCP) is a public cloud platform that offers a suite of extensive suite of computing services that runs on the same infrastructure that Google uses for its own products.

The GCP infrastructure as a service (IaaS) model offers on-demand, highly customisable and easily scalable suite of compute resources applicable for various (computing, data storage, analytics, ML etc.). This flexibility allows users to build the compute infrastructure to meet their business needs.

While GCP offers great flexibility, working in this environment also comes with some important caveats for users more familiar with on-premise HPC clusters. Most importantly, as GCP resources are provided on demand, this means **you pay for the compute, storage and networking resources used**. This places the onus on the scientists to manage our budget and pay close attention to our resource use!

Basic instructions on interacting with GCP via the console are provided in this document. For users more experienced with the CLI, we recommend using Cloud SKD for its potential for scripting and automation. Cloud SDK is pre-installed on gcloud and can also be downloaded to your personal machine. For more information on Cloud SDK, check out the `gcloud SDK documentation`_.
.. _gcloud SDK documentation: https://cloud.google.com/sdk/docs/install