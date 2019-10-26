# devops-demo
devops-demo - CI/CD setup

# How to give static ip to VM

1) Select File -> Host Network Manager. 

    1) Select Configure Manually option
    2) IPV4 address :- 192.168.99.1
    3) Network Mask :- 255.255.255.0
    4) Don't select DHCP server option

2) Select the VM and click properties
    1) Go to Network tab
    2) Select Adapter 2 and then Select Host only adapter and select the one created above

3) Power on the VM
    1) sudo nano /etc/network/interfaces
    2) #configure enp0s8
        auto enp0s8
        iface enp0s8 inet static
          address 192.168.99.2
	         network 255.255.255.0
