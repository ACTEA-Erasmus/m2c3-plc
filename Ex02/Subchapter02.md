# Study materials
_____________________________________
## Equipment
>   **1** Engineering station
>   **2** SIMATIC S7-1200 controller, e.g. CPU 1215C DC/DC/DC – firmware V4.2 or higher
>   **3** SIMATIC STEP 7 software in TIA Portal – V15 SP1 or higher
>   **4** Ethernet connection between engineering station and controller

<center>

![Equipment](../Ex02/Images/Equipment.jpg "Equipment")
</center>

## Setting the engineering station IP address
You need a TCP/IP connection to program a SIMATIC S7-1200 controller from the PC, the programming device or a laptop.

It is important that the IP addresses of both devices match for the PC and
SIMATIC S7-1200 to communicate with each other via TCP/IP.

* Locate the network icon ![](../Ex02/Images/Network_icon.jpg) in the taskbar at the bottom and click on "Network settings".

![](../Ex02/Images/Network_settings.jpg)

* In the network settings window that opens, click on "Ethernet" and then on "Change adapter options".


![](../Ex02/Images/Select_ethernet.jpg)

* Select the desired "Local Area Connection" that you want to use to connect to the controller and click "Properties".

![](../Ex02/Images/Network_connections.jpg)

* Next, select "Properties" for "Internet Protocol Version 4 (TCP/IP)".

![](../Ex02/Images/Ethernet_properties.jpg)

* You can now use the following IP address : 192.168.0.99 with Subnet mask 255.255.255.0. Accept the settings by pushing the "OK" button.
