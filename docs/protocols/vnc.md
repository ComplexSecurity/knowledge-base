Virtual Network Computing (VNC) is a graphical desktop-sharing system that uses the Remote Frame Buffer protocol (RFB) to remotely control another computer. It transmits the keyboard and mouse events from one computer to another, relaying the graphical-screen updates back in the other direction, over a network.

VNC works on a [[client]]/[[server]] model. A server component is installed on the remote computer (the one you want to control), and a VNC viewer, or client, is installed on the device you want to control from. This can include another computer, a tablet, or a mobile phone. When the server and viewer are connected, the server transmits a copy of the remote computer’s screen to the viewer.

Not only can the remote user see everything on the remote computer’s screen, but the program also allows for keyboard and mouse commands to work on the remote computer from afar, so the connected user has full control (after being granted permission from the remote compute)r.

The VNC protocol and [[Remote Desktop Protocol|RDP]], developed by Microsoft, share several similarities:

- These protocols both provide access to remote desktops for quick and easy troubleshooting and remote working.
- They both require both client and server-side software to support communication.
- They use direct peer-to-peer communication, which just means that the local user computer can connect directly to the remote computer or device.
- Both support software to manage users and enable secure access.

Both VNC and RDP connect devices through a network, either via server or peer-to-peer. But even though their goals are the same – to provide graphical remote desktop capabilities to a device – they also differ in how they achieve that goal.

- RDP has limited platform capabilities, whereas VNC works across multiple operating systems.
- RDP can be faster than VNC.
- Security levels can vastly differ between the two protocols.
- VNC connects directly to the computer, but RDP connects to a shared server.
- RDP is not very compatible if you need to implement a remote desktop solution across a wide range of devices.
- Because of this, RDP can limit the ability to provide IT help.
