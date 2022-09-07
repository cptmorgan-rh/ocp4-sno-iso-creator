Single Node OpenShift Bootable ISO with Static IPs
===========================================

## Description
------------

This is a simple Ansible Playbook that creates an ISO to install Single Node OpenShift with a static IP Address.

## Quickstart
This is a concise summary of everything you need to do to use the repo. Rest of the document goes into details of every step.
1. Edit `group_vars/all.yml`, the following must be changed while the rest can remain the same
   * ip and host/domain names
2. If you wish to run a specific Channel and Version modify the following in `group_vars/all.yml`:
   * download.channel
   * download.version

 ## Installation Steps

 ### Set Global Variables
 > Pre-populated entries in **group_vars/all.yml** are ready to be used unless you need to customize further. Any updates described below refer to [group_vars/all.yml](group_vars/all.yml) unless otherwise specified.
 1. Get the ***pull secret*** from [here](https://console.redhat.com/OpenShift/install/vsphere/user-provisioned). Update the file on the line with location of your `pull_secret`. ex. `~/openshift/pull-secret.json`
 2. OpenShift cluster
    1. base domain *(pre-populated with **example.com**)*
    2. cluster name *(pre-populated with **ocp4**)*
    3. network type *(pre-populated with **KubernetesOVN**)


USAGE
------------

### Run Deploy Playbook
```sh
# Deploy the Lab and all components
ansible-playbook create-sno-iso.yml
```
### create-sno-iso.yml Extra Variables

`specific_version=4.10.z` - Deploys a specific version of OpenShift. Must be in 4.x.z format.


AUTHOR
------
Morgan Peterman
