LVM Partition
=============

[![Actions Status](https://github.com/ome/ansible-role-lvm-partition/workflows/Molecule/badge.svg)](https://github.com/ome/ansible-role-lvm-partition/actions)
[![Ansible Role](https://img.shields.io/ansible/role/41255.svg)](https://galaxy.ansible.com/ome/lvm_partition/)

Additional LVM logical volumes to be created and mounted.

Existing LVs will be resized.

Role Variables
--------------

These variables must be defined (defaults aren't provided):

- `lvm_vgname`: LVM volume group for the logical volume
- `lvm_lvname`: Logical volume name, use `[A-Aa-z0-9]+` to avoid problems
- `lvm_lvmount`: Where the partition should be mounted
- `lvm_lvsize`: Size of the partition
- `lvm_lvfilesystem`: filesystem for partitions which need to be formatted

Optional variables:

- `lvm_shrink`: Shrink if current size is higher than size requested (default: True)
- `lvm_lvopts`: Logical volume creation options (default: None)
- `lvm_lvmount_dump`: Mount option (dump) for the filesystem mount point (default: 1)
- `lvm_lvmount_passno`: Mount option (passno) for the filesystem mount point (default: 2)


Author Information
------------------

ome-devel@lists.openmicroscopy.org.uk
