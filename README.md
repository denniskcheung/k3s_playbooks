# Ansible Playbooks for setting up Raspberry Pi K3s cluster

Wrote some Ansible scripts to set up and maintain a k3s cluster running on a [Pico 10 cluster](https://www.picocluster.com/collections/pico-10/products/copy-of-pico-10-raspberry-pi4-8gb). The cluster runs on 10 x   [Raspberry Pi 4 8gb's](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) with attached [Samsung 128gb Fit Plus](https://www.samsung.com/us/computing/memory-storage/usb-flash-drives/usb-3-1-flash-drive-fit-plus-128gb-muf-128ab-am/) flash drives for running Longhorn.

Originally ran on Raspbian; however, found some stability issues which would lock up my master nodes after a week or so.  Moved to [Ubuntu ARM server 22.04 LTS](https://ubuntu.com/download/server/arm) and has been stable since.

The script will set up K3s with the control plane and worker nodes as well as upgrade an existing cluster to the latest [stable release](https://update.k3s.io/v1-release/channels).