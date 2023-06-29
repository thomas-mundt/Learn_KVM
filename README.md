# Learn KVM

## Setup

```
egrep -c '(vmx|svm)' /proc/cpuinfo

sudo apt install bridge-utils libvirt-clients libvirt-daemon-system qemu-system-x86

systemctl status libvirtd

sudo systemctl stop libvirtd

sudo groupadd kvm
sudo groupadd libvirt

sudo usermod -aG kvm $USER
sudo usermod -aG libvirt $USER

sudo chown :kvm /var/lib/libvirt/images

sudo chmod g+rw /var/lib/libvirt/images

sudo systemctl start libvirtd

sudo systemctl status libvirtd

sudo apt install ssh-askpass virt-manager

virt-manager
```
