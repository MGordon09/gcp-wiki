Welcome to the NIBSC GCP Wiki!
==========================================

What is Google Cloud
----------------------

Google Cloud Platform (GCP) is a public cloud platform that offers an extensive suite of computing services running on the same infrastructure that Google uses for its own products.

The GCP infrastructure as a service (IaaS) model offers on-demand, highly customizable and easily scalable compute resources. This flexibility allows users to build the compute infrastructure needed for their workflows.

Caveats on the Cloud
----------------------

While Google Cloud offers great flexibility, working in this environment also comes with some important caveats for users familiar with our on-premise HPC clusters.

Most importantly, as GCP resources are provided on demand, this means **you pay for the compute, storage and networking resources used**. This places an onus on the scientists to manage our budget use these resources sensibly!

Interacting with GCP
----------------------

We will touch on three different approaches for interacting with GCP in later sections. Basic instructions are generally provided with examples on the GCP console, as this is the most beginner-friendly interface for interacting with GCP services. 

For more experienced CLI users, we recommend using Cloud SKD due to its potential for scripting and automation.

Cloud SDK is pre-installed in cloud shell. It is also available on hpc-scratch and can be installed on your personal machine. For more information on Cloud SDK, check out the `gcloud SDK documentation <https://cloud.google.com/sdk/docs/install>`_


.. toctree::
   :maxdepth: 2
   :caption: Contents:

   connecting
   storage
   uploading
   creating-vms
   workflows
   signedurl
   qwiklabs

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. note::

   This wiki is under active development. If you would like to contribute, please contact martin.gordon@nibsc.org, khushwant.sidhu@nttdata.com or a member of the NGS core facility