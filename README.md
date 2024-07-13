# KVM VM Migration host to host

to migrate the virtual machine to onther host

to list all vm's in the host

```virsh list --all```

shutdown the vm

```virsh shutdown vm_name```

export the vm configuration

```virsh dumpxml vm_name > /root/vm_name.xml ```

Copy the configuration file to the destination host

``` scp /root/vm_name.xml destination_host_ip://etc/libvirt/qemu ```

Copy the hard disk to destination host

``` scp vm_disk.qcow2 destination_host_ip://var/libvirt/qemu/ ```

define migrated vm using config file

```virsh define guest_name.xml```

start the vm 

``` virsh start ```
