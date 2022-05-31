Data Sharing
================

Using Signed URLs
--------------------

To share data with external collaborator, please follow the approach outlined below for sharing signed URLs.

Signed URLS provide time-limited access to a cloud storage resource. This method is more secure than enabling public access for a storage bucket and was recommended by the service providers.

.. note::
    Further information on sharing data using signed URLs can be found `here <https://cloud.google.com/storage/docs/access-control/signing-urls-with-helpers>`_.

- Create a service account with ‘Storage Object Viewer’ role. Go to IAM & Admin -> Service Accounts -> Create. 

.. image:: ../images/gcp-createserviceaccount.png
  :width: 800
  :alt: Creating service account using GCP console

- Give the SA and give the ‘storage object viewer role’

.. image:: ../images/gcp-saobjectviewer.png
  :width: 800
  :alt: Object viewer permissions
 
- Create a json key from the service account. Go to IAM & Admin -> Service Accounts -> select the service account you created above -> keys tab -> add key (json format)

.. image:: ../images/gcp-sajsonkey.png
  :width: 800
  :alt: Creating service account JSON key

.. note::
    This will download the key locally. **Don’t store this key anywhere publicly visible as this could allow someone to access your service account!**
 
- Move json key to cloud shell. Upload key to cloud shell to your home directory (start cloud shell from the GCP console, select the 3 dots in top right of cloud shell header and upload the file)

.. image:: ../images/gcp-sajsonupload.png
  :width: 800
  :alt: Uploading json key via cloud shell

- Generate the signedURL with following commands:

.. code-block:: text


    # install python lib dependency
    pip3 install pyopenssl

    # example command: gsutil signurl -d duration path-to-json object-to-share 
    gsutil signurl -d 2d ~/PATH/TO/signedurl.json gs://mhra-ngs-singurl-test/bio-resources.zip
 

- You can copy and send this link to your collaborators to download the data. The link will work for duration set above

 .. note::
    Ensure a dedicated service account is used (no other IAM role apart from Object Viewer) and remember to delete the key when download is completed