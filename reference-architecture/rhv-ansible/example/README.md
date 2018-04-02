# OCP on RHV Examples
The files in this directory are used in development of the reference architecture
and reflect the development environment used to test at RedHat.

## Common files
  - nsupdate-clean.txt  Contains nsupdate commands to remove any DNS entires
    created by the env, including reverse pointers in the 192.168.155 space
## OCP 3.9 on RHV 4.2 Environment
  - inventory.yaml Static inventory for 3.9 on RHV 4.2 beta
  - node_preparation.yaml Playbook to do minimal setup before handing off to OpenShift prerequisites pb
  - ocp-vars.yaml.39 Base set of variables needed to establish VMs and DNS setup
  - ovirt-37-infra.yaml Set up VMs for refarch (39 is a symlink to this one)
  - vars/ovirt-37-vars.yaml
  - ovirt-39-infra.yaml
  - vars/ovirt-39-vars.yaml
  - redeploy-39.sh Script to (re) deploy OCP 3.9 on RHV 4.2 beta environment

## Older Versions OCP on RHV
  - ocp-vars.yaml
  - ocp-vars.yaml.35
  - ocp-vars.yaml.36
  - ocp-vars.yaml.37
  - ocp-vars.yaml.atomic
  - ocp-vars.yaml.beta
  - ocp-vars.yaml.cen39
  - ocp-vars.yaml.centos

## Miscellaneous playbooks
  - onevm-uninstall.yaml  An example of destroying one ill-fated VM to avoid
    forcing a reinstall of the entire environment.
  - test-docker-storage.yaml Playbook to test docker-storage-setup role during development
  - test-instance-groups.yaml Playbook to debug effect of instance-groups role

## Ovirt installation playbooks and vars
  - ovirt-atomic-infra.yaml Deploy Atomic in place of RHEL
  - vars/ovirt-atomic-vars.yaml

  - ovirt-cen39-infra.yaml CentOS deployed for OCP 3.9 effort
  - vars/ovirt-cen39-vars.yaml

  - ovirt-centos-infra.yaml CentOS in place of RHEL (includes cloud-init to handle guest agent)
  - vars/ovirt-centos-vars.yaml

  - ovirt-image-only.yaml Playbook to just handle template image without deploying infra

  - redeploy.sh Script to clean existing environment, and redeploy

  - uninstall.yaml Playbook to unsubscribe nodes from RHSM, erase in ovirt, and run nsupdate-clean
