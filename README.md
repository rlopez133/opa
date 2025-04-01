# Open Policy Agent Install Collection 

## What This Collection Does
This Ansible collection installs and configures an Open Policy Agent (OPA) server on OpenShift ready to receive policies and evaluate data for policy decisions.


## How to Run this Collection

Within AAP, create a Job Template with the following content. Notice that you will need to get a OpenShift Bearer Token as your Credential. This Bearer Token can be captured from the top right corner of your OpenShift Console selecting 'admin' and then selecting 'Copy login command' which will give you the server and token that you will need to create the credential. 

![image](https://github.com/user-attachments/assets/4d6d4203-be5d-4630-a293-14e4850dbb19)
