# One-Click-OpenVPN-for-free
 
One-Click OpenVPN for free
In today's society, security and privacy is a problem when you are at public areas like airports, coffee shops, hotels, censored countries(China,etc) in the world, or any location that offers free public WiFi. Outsiders can monitor internet traffic between your computer and the web. OpenVPN is an open source application that implements a virtual private network, which will create a secure connection between you and your remote destination (website or server). This tutorial will show you how to quickly install and setup OpenVPN .


Step 1:  Create free account in Vultr , Click here  http://www.vultr.com/?ref=6920741-3B  

 

Step 2: Login Vultr  

Click here   http://www.vultr.com/?ref=6920741-3B  


Then Click below One-Click deploy OpenVPN 

https://my.vultr.com/deploy/?app=openvpn

Important note:ALL YOU NEED TO DO IS SELECT CentOS 6 x64 operating system IN Server type, Then Click Deploy Now. This process will be completed in minutes.

Initially, you will need to access https://[SERVER_IP]:943/ in your web-browser. Substitute the [SERVER_IP] with the IP address of your VPS. Your login credentials are available in the Vultr control panel. Login and review the EULA prompt. You will also see an SSL warning when you try to connect, this is safe to accept.

Step 3: Connecting To Your VPN
Follow the steps below to connect to your VPN using the OpenVPN Connect Client. The official OpenVPN website also has useful guides:
Desktop Client Configuration
Connect With Linux Clients
OpenVPN uses system user accounts on the app VPS for authentication. An "openvpn" user is automatically added to your VPS (the password for it is in the Vultr control panel). See the notes below on how to add more users.
For Iphone /IOS users, click below
https://itunes.apple.com/us/app/openvpn-connect/id590379981?mt=8
OpenVPN Connect iOS FAQ
https://docs.openvpn.net/docs/openvpn-connect/openvpn-connect-ios-faq.html
For Android users, click below
https://play.google.com/store/apps/details?id=net.openvpn.openvpn&hl=en
OpenVPN Connect Android FAQ
https://docs.openvpn.net/docs/openvpn-connect/openvpn-connect-android-faq.html
 

Windows Client

Login to https://[SERVER_IP]:943/ as the client that you want to connect to your VPN with. The default is "openvpn".
Download the .msi installer.
Proceed through the installation wizard.
Locate the "OpenVPN Client" shortcut (desktop, start menu, or application menu), launch this application.
An OpenVPN icon will appear by the system clock.
Click the icon, then click "Connect [SERVER_IP]" from the popup menu. If you do not see your server's IP in the list, revisit thehttps://[SERVER_IP]:943/ site again and follow the steps to connect. Your web browser may block content on that page that prevents your tray icon from updating - in this case, you will need to allow content on that page to run.
Follow the login prompts. Once completed, you will be on the VPN hosted by your server.
Mac OS X Client

Login to https://[SERVER_IP]:943/ as the client that you want to connect to your VPN with. The default is "openvpn".
Download the .dmg installer.
Right click on the downloaded .dmg installer and click "Open". Allow the installation from an unidentified developer.
Proceed through the installation wizard.
Navigate to /Applications/OpenVPN.
Launch "OpenVPN Connect.app".
An OpenVPN icon will appear by the system clock.
Click the icon, then click "Connect [SERVER_IP]" from the popup menu. If you do not see your server's IP in the list, revisit the https://[SERVER_IP]:943/ site again and follow the steps to connect. Your web browser may block content on that page that prevents your tray icon from updating - in this case, you will need to allow content on that page to run.
Follow the login prompts. Once completed, you will be on the VPN hosted by your server.
 Enjoy your freedom.
Tips: Using Your VPN
Here are some important notes to keep in mind while using your OpenVPN app on Vultr.
Each OpenVPN app includes the Access Server (AS) control panel. This can be accessed with your OpenVPN login (https://[SERVER_IP]:943/ ).
The OpenVPN software used only allows 2 concurrent connections. This means that you may have up to 2 computers connected to your OpenVPN server at any given time. If you need additional connections, you may purchase a license from OpenVPN. See the license section of the AS control panel ( https://[SERVER_IP]:943/admin/license ).
The VPN default network address range is ( 172.27.224.0 - 172.27.239.255 ). Upon connecting with the OpenVPN Client software, your computer will be given an IP address in this range.
By default, OpenVPN does not allow multiple client connections to communicate with one another. For example, say you have 2 computers connected to your OpenVPN server, they are given addresses: 172.27.224.1 and 172.27.224.2. If you would like 172.27.224.1 to be able to communicate with 172.27.224.2, you have to change some routing settings on the "VPN Settings" section of the AS control panel.
Visit the VPN settings page ( https://[SERVER_IP]:943/admin/vpn_settings ).
Under the routing section, choose "Yes, using routing (advanced)" under "Should VPN clients have access to private subnets (non-public networks on the server side)?".
In the "Specify the private subnets..." box, enter 172.27.224.0/20.
Click "Save Settings". Then click "Update Running Server".
IPv6 is not supported with this app. You can enable IPv6 when launching an OpenVPN app on Vultr, but the OpenVPN software will not take advantage of it. The OpenVPN software used for this app only has partial IPv6 support. Vultr will likely add full IPv6 integration when the OpenVPN software fully supports it.
For IPv6 clients - no IPv6 traffic is routed through the OpenVPN app. If you connect to your OpenVPN network, only IPv4 traffic will be routed through it. As a workaround, you can disable your local IPv6 connection temporarily while using OpenVPN, or disable IPv6 in your web browser (some browsers have this setting).
OpenVPN controls the DNS settings of each connected client computer. By default, the DNS servers of your OpenVPN server are used. You can change this behavior in the AS control panel ( https://[SERVER_IP]:943/admin/vpn_settings ).
When connected to your OpenVPN server, all of your IPv4 internet traffic passes through it. Therefore, your internet download/upload speeds will be slower than normal.
(You can log into this system with an SSH client using the root login found on your Vultr control panel.)

About Vultr Applications
Vultr applications use modern releases of software packages. Applications are configured to be deployed with specific versions of software. Over time, the Vultr team will update the application offerings to include newer operating systems, package versions, etc. This document only provides up-to-date information about the latest version of this application. Vultr applications are updated without notice. If you plan to build a project or infrastructure based on our application templates, we recommend taking a snapshot of the application used in your initial deployment.
