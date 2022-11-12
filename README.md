# awx-patching
For patching Linux servers via AWX

# Prerequisites 
To get started with this repo, you'll need the following:
 - An AWX instance -> [Ansible AWX Repo](https://github.com/ansible/awx)
 - A git repo (fork of this)

# Getting Started
## In AWX
1) Create source control, make sure to use their respective credential types too
2) Create a project and point to your fork and branch in Github, GitLab, etc. Make sure to check the box to update on launch. This is pull the latest commit into AWX
3) Create an inventory with the servers you would like to target
4) Create a Template and choose **Job Type** of `run` then select for inventory and project from the dropdowns. Set your playbook as well. You can set your execution environment if you want, but it shouldn't be required. 
5) In the template, set your credentials to log on to the servers (SSH keys recommended).
6) Save the template and **Launch** the job