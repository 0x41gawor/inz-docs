# inz-docs

At first 5G Core VM was created. In this step we created a Ubuntu-Server VM, which can used as a skeleton for other VMs.

Second step is to create UERANSIM VM.



## Launch it

- Go to VirtualBox and start both `free5gc` and `ueransim` VMs

- Connect to them via SSH ( e.g. MobaXterm)

- (Optional) Ping them from each other

- Copy and paste it into `free5gc` line by line...

  ```bash
  sudo sysctl -w net.ipv4.ip_forward=1
  sudo iptables -t nat -A POSTROUTING -o enp0s3 -j MASQUERADE
  sudo systemctl stop ufw
  ```

  ... to enable IP forwarding

  - in 5G terms enable Core to forward UERAN flows to the Data Network (Internet in our case)

- Next steps are described in [here](Create UERANSIM VM.md) under **"Step 5 Testing UERANSIM against free5gc"**

