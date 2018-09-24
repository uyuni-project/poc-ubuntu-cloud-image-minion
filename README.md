# ubuntu-cloud-image-minion

Following the UNIX Design, doing only 1 thing, doing it well, the goal of this project is:

* deploy with terraform-libvirt-provider
* use Ubuntu upstream Cloud Image.
* use cloudinit for installing openSUSE saltstack packages, and other minimal configurations.

Once the VM is created, you can boostrap this VM instance against your Uyuni-Server. (this is outside the scope of this project)


# Requirements:
This project need at **least** terraform-provider-libvirt >= 0.5 version (https://github.com/dmacvicar/terraform-provider-libvirt/releases)


# Developer Documentation:

Have a look [Here](CONTRIBUTING.md) if you want to extend/develop this project.

# USER Documentation

## Howto:

If you have terraform and terraform-libvirt-plugin already installed, after cloning this project do:

```bash
terraform init
terraform apply
```

# Installation:

If you don't have `terraform` and `terraform-provider-libvirt` installed:


* terraform
https://www.terraform.io/downloads.html

* libvirt
https://github.com/dmacvicar/terraform-provider-libvirt#installing

## Design of this project.
![arch](design_doc/architecture.jpg)

### Additional steps: boostrapping ubuntu image against SUSE-Manager.

With the VM and the ip of your Ubuntu Server, you can then boostrap the minion against uyuni server ( via gui or CLI). 
This is out of scope of this project.

![boostrap](design_doc/boostrap.jpg)


## installing a uyuni server.

You can use sumaform for installing Uyuni server and client automatically.
https://github.com/moio/sumaform
