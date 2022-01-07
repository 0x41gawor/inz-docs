# Free5GC on Virtual Machines

[free5gc](https://www.free5gc.org)

## Launch it

- Go to VirtualBox and start both `free5gc` and `ueransim` VMs

- Connect to them via SSH ( e.g. MobaXterm)

- (Optional) Ping them from each other, to test communication.

- Copy and paste it into `free5gc` line by line...

  ```bash
  sudo sysctl -w net.ipv4.ip_forward=1
  sudo iptables -t nat -A POSTROUTING -o enp0s3 -j MASQUERADE
  sudo systemctl stop ufw
  ```

  ... to enable IP forwarding

  - in 5G terms enable Core to forward UERAN flows to the Data Network (Internet in our case)

- Next steps are described in [here](on_VMs/Create UERANSIM VM.md) under **"Step 5 Testing UERANSIM against free5gc"**

# Free5GC on Kubernetes Clusters

[towards5gs-helm](https://github.com/Orange-OpenSource/towards5gs-helm)

## Introduction to clusters

[Introduction to clusters](on_Clusters/Clusters_intro.md)

