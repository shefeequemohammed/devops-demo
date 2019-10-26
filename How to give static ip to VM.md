# devops-demo
devops-demo - CI/CD setup

# How to give static ip to VM

1) In VirtualBox, select File -> Host Network Manager. 

Select Configure Manually option
IPV4 address :- 192.168.99.1
Network Mask :- 255.255.255.0
Don't select DHCP server option

2) Select the VM and click properties, go to Network tab
Select Adapter 2 and then Select Host only adapter and select the one created above
