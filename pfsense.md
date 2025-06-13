<div align="center">
  <a href="index">Home</a>&nbsp;&nbsp;&nbsp;
  <a href="projects">Projects</a>&nbsp;&nbsp;&nbsp;
  <a href="scripts">Scripts</a>
</div>


# OPNsense Firewall

The overall plan for the Proxmox network is to simulate a business network, so we'll definitely need a solid firewall to control our traffic. 

<br>

## Download and Verify
After downloading the ISO, we'll verify its integrity by generating a hash of the image and comparing it to the hash on the OPNsense website. 

I'm verifying the hash from a Mac, so I used the following command:

<img width="749" alt="Screen Shot 2025-06-12 at 11 31 53 PM" src="https://github.com/user-attachments/assets/ae587e95-e8d7-462f-9096-6f01f6050db7" />

<br>
<br>
<br>

This is the result, which matches what OPNsense provided:

<img width="798" alt="Screen Shot 2025-06-12 at 11 32 08 PM" src="https://github.com/user-attachments/assets/66ed03f3-689a-4d5c-aafc-bcf8f8edf6a0" />

<br>
<br>
<br>

## Already running into problems...
On boot, we're greeted with an error "Boot failed: Could not read from CDROM" and "Boot failed: not a bootable disk".

A quick google search led me to this result on reddit, which mentioned switching from a VGA image to a DVD image. We'll give that a shot.

(source: https://www.reddit.com/r/Proxmox/comments/rxohnu/opnsense_cant_boot_for_first_time/)

<br>

## Booting successful
Now that we've uploaded the proper file to Proxmox, OPNsense is now opening up properly and greets us with this screen: 

![image](https://github.com/user-attachments/assets/80890395-d382-4e8a-a2a8-d152f00340f0)

<br>

## To Be Continued
Next, we'll begin the installation.
