Creating Virtual Machines
================================

Most of the work we will be doing involves running running software on virtual machines.

Virtual machines (VM) are digital versions of a physical computers. They can run programs and operating systems, store data, connect to networks, and do other computing functions.

VM's are created using Compute Engine, Googles Infrastructure as a Service (IaaS) offering. This offers a high degree of customisability and allows users to scale VMs to their needs.

Creating VM's from Instance Templates
---------------------------------------

An instance template is a resource that you can use as a 'recipe' to create virtual machine (VM) instances. Instance templates define the VM configuration, including machine type, boot disk image or container image, labels, startup script, and other instance properties, including pre-installed software that is available.

Two instance templates have been created for users, who have a choice of what to use depending on their workflow requirements.
 
- **mhra-ngs-tools:** VM template with conda, singularity, cloud SDK and installed

- **mhra-ngs-nextflow-dsub:** VM template with nextflow, dsub and cloud SDK installed

These two images should give you all the flexibility to execute your workflows.
 
The mhra-ngs-tools template generates a larger VM with more disk space. This VM is a more suitable environment for interactive sessions.
 
The mhra-ngs-nextflow-dsub template generates a smaller VM suitable for launching batch jobs using either dsub or Nextflow. Both of these tools use the Google Life Science API (https://cloud.google.com/life-sciences/docs/reference/rest) to orchestrate these workflows.
 

VM Creation: Walkthrough
----------------------------

- Log in to GCP using your account credentials
 
- Select your project
 
- Search for 'Compute Engine' in the GCP console search bar -> select 'Create Instance' -> 'New VM instance from template'. Select the image that best fits your workflow and hit continue:

.. image:: ../images/gcp-vmfromtemplate.png
  :width: 800
  :alt: Creating VM from Instance Template


- Name your VM, select europe-west2 (London) as region (any zone is fine), scroll down and click 'Create'.

.. note::
    The instance template configurations should be fine for majority of workflows. Aside from naming and setting VM location, please only modify as required

.. note::
    VMs can be created via CLI using cloud shell or a terminal with cloud SDK installed, such as your hpc-scratch or your personal machine -check out the 'Equivalent Command Line' option below and try it!

- You have now created a fully-functioning VM! To view your VM, return to the VM instances screen. You will see a green tick beside your VM if it is operational. 

.. image:: ../images/gcp-vminstances.png
  :width: 800
  :alt: Running VMs

- To pause/stop/restart your VM, select the three dots in the right-hand side of the screen and choose an option

.. image:: ../images/gcp-vminstancesstop.png
  :width: 800
  :alt: Stop VMs

.. note::
    *Please remember to stop your VM* when not in use and delete once your work is finished to avoid incurring excessive costs!
 
- To connect to your VM select the 'ssh' button beside it's name, this will create a new pop-up window and provide access to the VM terminal:

.. image:: ../images/gcp-vmstartup.png
  :width: 800
  :alt: VM terminal

- You are now ready to start you analysis! Check out the next section for some standard workflows

.. note::
    Some further resources: `Creating VMs from Image Templates <https://cloud.google.com/compute/docs/instances/create-vm-from-instance-template>`_., `Connecting to VM instances <https://cloud.google.com/compute/docs/instances/connecting-to-instance>`_. and `Gcloud CLI cheatsheet <https://cloud.google.com/sdk/docs/cheatsheet>`_.