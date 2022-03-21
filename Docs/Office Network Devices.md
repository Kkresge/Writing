# Office Network Devices

When you're troubleshooting a network-related issue in an office, it's helpful to know about the types of devices that live inside the office network room and what purposes they serve. This article contains general information about these common office network devices. Keep in mind that not every office network will have all of these. You can find more specific documentation about a particular organization's network equipment in the Client Files folder on our SharePoint site.

If you look at the diagram below, you'll see one example of an office network setup (AKA, “topology”). It is divided into two halves: the network closet, and the office. This article mainly covers the type of equipment that would be in the network closet.

![Office network diagram](Office%20Network%20Devices.assets/diagram.png)

## Internet

Internet service is provided by an ISP (Internet Service Provider) such as Comcast, Fios, or Spectrum.

## Modems and Routers

### Modems

The modem is the box that brings the internet into the building. If the internet appears to be down in an office, this is probably the first device you'll want to look at.

It usually only has two ports: one coax port (which brings the internet connection from outside the building, and into the modem), and one Ethernet port (which brings the internet connection out of the modem, and into the next device). So unless your office building only has one computer, you're probably not going to be plugging it directly into the modem!

It will have LED lights on it that give you information about its power status, internet (WAN) connection status, and more. Specific colors can show which aspects of the device or internet service are working, if there’s an error, or if something is broken or offline. The meaning of modem light colors is determined by the modem’s manufacturer. For a basic overview that applies to most modems, check out this article: [What Do the Lights on My Modem Mean?](https://www.lifewire.com/modem-lights-explained-5180332)

![Comcast business modem](Office%20Network%20Devices.assets/comcast%20business%20modem.png)

(Image: a Comcast business modem)

### Routers

The router brings the internet (WAN) from the modem to other devices. Not every office will have one of these—you might have noticed that there is no router in the diagram at the top of this article. A router will typically have around five Ethernet ports that carry the internet connection to whatever devices are plugged into them. Some common router manufacturers are Linksys, 3Com, Belkin, D-Link, Motorola, TRENDnet, and Cisco.

A router can create a Wi-Fi network in the office, but this is more common in small home networks. Most office networks are in bigger buildings and need to place wireless access points around the building for Wi-Fi instead.

A router can usually do much more than carry over the internet connection from the modem. It can be configured as a DHCP server (which assigns IP addresses to all the devices on the network) and a firewall (which controls access to the internet to make the network more secure), and more (depending on the router’s brand and model). But many offices don't use the router for these capabilities. Instead they can use a separate hardware device called the "firewall", which you can read more about in the next section.

![NETGEAR router, front](Office%20Network%20Devices.assets/netgear%20router%20front.png)

(Image: the front of a NETGEAR router)

![NETGEAR router, back](Office%20Network%20Devices.assets/netgear%20router%20back.png)

(Image: the back of a NETGEAR router)

Some offices also have a special router called an Edgewater. An Edgewater is a router that is used specifically to create a separate network to connect VoIP phones, which are phones that work through the internet. You would only need to access an Edgewater if you were troubleshooting something involving VoIP phones.

![Edgewater router, front](Office%20Network%20Devices.assets/edgewater%20router%20front.png)

(Image: the front of an Edgewater router)

![Edgewater router, back](Office%20Network%20Devices.assets/edgewater%20router%20back.png)

(Image: the back of an Edgewater router)

### Additional Notes on Modems and Routers

- Sometimes, the modem and the router are combined into one hardware device.
- Many offices don't have a router at all. Instead, they have a hardware device called a "firewall" that handles things like DHCP and network security, and they have wireless access points that handle bringing Wi-Fi into the office.

## Firewalls

A firewall is a network security device. A firewall can be a virtual feature built into a router, or it can be a physical hardware device. In this section we will be discussing physical hardware firewalls.

Some common hardware firewall manufacturers are SonicWall and WatchGuard.

A firewall typically does the following things:

- Acts as the gatekeeper of the internet by blocking incoming internet traffic that is malicious or unauthorized to access the office network, and blocks outgoing traffic from accessing things on the internet that shouldn't be accessed (such as inappropriate websites).
- Acts as a DHCP server, which assigns IP addresses to devices on the office network.
- Creates and manages a VPN that allows users to have secure access to the office network when working remotely.

![SonicWall TZ300 firewall](Office%20Network%20Devices.assets/sonicwall%20firewall.png)

(Image: the front and back of a SonicWall TZ300 firewall)

## Switches

Simply put, a switch is a box that has many Ethernet ports. It will be connected to a central device on the network (such as the router, modem, or firewall) so that more devices can be connected. Think of it like a USB hub, but for Ethernet connections!

Routers and firewalls typically only have a few Ethernet ports, which is usually not enough to connect all the devices that are in a network closet to them. That's where a switch comes in.

Switches can have as few as 5 ethernet ports, or more than 50 Ethernet ports! Each port on the switch will be labeled with a number to help you keep track of what device is plugged into what Ethernet port. When you're troubleshooting a device's network connection, you should take note of what port number in the switch it is connected to.

Some common manufacturers are D-Link, Netgear, TP-Link, and TrendNet.

There are two types of switches: unmanaged switches, and managed switches.

![NETGEAR switch](Office%20Network%20Devices.assets/netgear%20switch.png)

(Image: a NETGEAR switch with 16 Ethernet ports)

### Unmanaged Switches

Unmanaged switches do not have any extra settings or special features. All an unmanaged
switch does is add more Ethernet ports to the network.

### Managed Switches

Managed switches offer more functionality and features for IT professionals and are the type most likely seen in business settings. With a managed switch, an IT admin can manage, configure, and monitor settings of the LAN (Local Area Network). These settings can be accessed from the command line, or a web interface (sort of like an "admin center" for the switch).

### PoE (Power over Ethernet) Ports

Some devices need to be connected to a Power over Ethernet port in order to work. One example of this is a UniFi Cloud Key. Another example of this is any Polycom VoIP phone that doesn't have a separate power cable. Instead of using a power outlet, it gets its power from the Ethernet cable. But you can't just plug it into any old Ethernet port—it must be plugged into a *PoE* port. To handle situations like this, many switches have at least a few ports that are PoE ports. These are usually labeled so you know which ports on the switch are PoE (and which are just plain old Ethernet ports).

## Patch Panels

A patch panel is the device in a network closet that all the Ethernet wall ports in a building connect to. Much like a switch, it is a box with a ton of Ethernet ports. It usually mounted on a wall rack. For each Ethernet port that is built into the wall in the office, an Ethernet cable is running through the walls behind it to connect it to the patch panel. The patch panel can then connect it to the switch in the network closet, which connects that port to the LAN (Local Area Network) and the WAN (internet).

![Patch panel](Office%20Network%20Devices.assets/patch%20panel.png)

(Image: a patch panel mounted to a rack)

![Ethernet port](Office%20Network%20Devices.assets/ethernet%20port.png)

(Image: an Ethernet port wall mount)

Each port of the patch panel will have a label on it. This label tells you which Ethernet wall port in the office that particular port runs back to. If an Ethernet wall port isn't working, it might be because:

- It was never hooked up to the patch panel (and a cable wiring technician will need to be hired to run an Ethernet cable through the walls to connect it), or...
- It was hooked up to the patch panel, but its corresponding patch panel port is not connected to anything that would give it network connectivity. (Normally each patch panel port will be connected to the switch, which connects to the rest of the devices in the network closet).

## Other Devices

You can read about other common devices that haven't been mentioned yet below.

### UniFi Cloud Key and Wireless Access Points

A Wireless Access Point (WAP) is used to allow devices to connect to a network wirelessly (Wi-Fi). In small home networks, these are usually not needed because this functionality is typically built into the router provided by your Internet Service Provider. This is sufficient to provide Wi-Fi coverage within a small home, but in larger buildings, you may lose the Wi-Fi connection if you go too far from the router. WAPs can be used in office networks where Wi-Fi access is needed throughout a large building. A WAP can be placed in each room or floor of an office to extend the range of a Wi-Fi network throughout the building.

![UniFi wireless access point](Office%20Network%20Devices.assets/unifi%20wap.png)

(Image: a UniFi wireless access point)

One manufacturer of WAPs is UniFi. UniFi also manufactures a device called a Cloud Key. This is a small device which allows you to monitor the status and change the settings of UniFi WAPs from a web portal. The Cloud Key would typically be connected to a switch or router in the network closet of an office building.

![UniFi Cloud Key](Office%20Network%20Devices.assets/UniFi%20cloud%20key.png)

(Image: a UniFi Cloud Key)

### Servers

A server is a computer that is used to share resources, such as files or programs, over a network. For example, a file server can be used to store and share files that multiple employees need access to. Some server manufacturers are Dell, HP, and Lenovo.

![](Office%20Network%20Devices.assets/dell%20server.png)

(Image: a Dell server)