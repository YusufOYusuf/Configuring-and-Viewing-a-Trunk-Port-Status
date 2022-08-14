<h1>Configuring and Viewing a Trunk Port Status</h1>


<h2>Description</h2>
In this lab, I learned to configure and view a trunk port status. A trunk is a single physical or logical connection that simultaneously carries traffic for multiple VLANs.
<br />



<h2>Environments Used </h2>

- <b>Ubuntu 20.04.2 LTS</b> 
- <b>PuTTY SSH Client</b>

<h2>Program walk-through:</h2>

<p align="center">
From the left sidebar click PuTTY SSH Client and proceed to put in the IP address, port number, click Telnet and then click open: <br/>
<img src="https://i.postimg.cc/vZjWNVVK/Screen-Shot-2022-08-13-at-10-13-39-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the IOU1 terminal window type the following commands <br/>
1. configure terminal <br/>
2. interface range e1/0-3 <br/>
3. switchport trunk encapsulation dot1q <br/>
4. switchport mode trunk <br/>
5. exit <br/>
6. interface e1/3 <br/>
7. switchport trunk allowed vlan 1,99 <br/>
8. switchport mode trunk <br/>
9. end <br/>
<img src="https://i.postimg.cc/XY8PB3pL/Screen-Shot-2022-08-13-at-10-20-09-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />
  
  
  
<br />
In the IOU1 terminal window type "show run interface e1/3" command to display the status of the particular interface of the network device<br/>
The type the "show interface trunk" command to display information on the swtich
<img src="https://i.postimg.cc/xdmbFjMy/Screen-Shot-2022-08-13-at-10-21-49-PM.png" height="80%" width="80%" alt="Configuring Advanced Ethernet Options Steps"/>
<br />






  
  
 

  
  
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
