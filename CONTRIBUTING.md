# How to contribute:

Developer documentation.





# terraform
For deploying the VM we use the a terraform file.

You can have a look at the libvirt-provider documentation: https://github.com/dmacvicar/terraform-provider-libvirt#website-docs and examples:  https://github.com/dmacvicar/terraform-provider-libvirt/tree/master/examples

For how works terraform just search terraform doc upstream

# cloudinit

When we create the VM we use cloudinit which will create the standard password, add the right repo for saltstack.

If you want to add your ssh-key, just make a pr  with and add your pub key to dir `pub_ssh`.

If you want to dev further the cloudinit part take a look on upstream doc:

https://cloudinit.readthedocs.io/en/latest/

and also on libvirt-plugin https://github.com/dmacvicar/terraform-provider-libvirt/blob/master/website/docs/r/cloudinit.html.markdown.

The libvirt-plugin support all 3 input files. (`user_data`, `meta_data` and `network_config`).
