---
layout: page
title: How to Install the Virtual Appliance
permalink: /virtual-appliance/install.html
exclude: True
---

# About this document
This document helps LEO customers install the VA from scratch on a brand new virtual machine or dedicated appliance.  Customers should make certain to review the [minimum requirements](minimum-requirements) before proceeding.

# Before You Begin
1. Retrieve your device ID and license key from [ETS](https://ets.leocybersecurity.com/)
2. Install a secure shell client on your desktop machine
3. Setup your host VM according to the [minimum requirements](minimum-requirements)
4. Setup your network devices to use promiscuous mode.  Please see your network equipment manufacturer's documentation for more information
5. Setup your management interface for Internet access.  Your management interface will need to reach the following end-points:
    * https://mvpn.leocybersecurity.com
    * https://lvpn.leocybersecurity.com
    * https://hfystmmgp5.execute-api.us-east-2.amazonaws.com (configuration only)
    * https://s3.us-east-2.amazonaws.com (configuration only)

# Step 1: Download and mount the ISO from LEO Cybser Security
1. Visit [https://iso.leocybersecurity.com/latest/](https://iso.leocybersecurity.com/latest/)
2. Download the ISO (the file is about 760 MB)
3. Place the ISO in a storage location accessible to your virtualization environment
4. Mount the ISO to a virtual optical device attached to your virtual machine
5. Power on the virtual machine

# Step 2: Install the virtual appliance
1. Press `enter` to select **Install Virtual Appliance**
2. Wait for the unattended installation to complete
3. The machine will reboot.  Once reboot is complete, log into the console using the following credentials:
    * `user: customer`
    * `pass: customer`

# Step 3: Configure the virtual appliance
1. **Important**: Change your default password immediately and record it in a secure location
    1. Select **User Settings**
    2. In the **Old Password** field, type `customer`
    3. Update your password according to the following requirements:
        * 10 characters
        * at least one number
        * at least one special character
        * not a palindrome (example: *tacocat, borroworrob*)

       Once you update the password, the interface will log out automatically
2. Configure the interfaces

    > **Note**: Please see [more about interfaces](more-about-interfaces) for further information. 

    1. Select **Interface Configuration**
    2. Select **turn monitoring mode on** for your promiscuous interface
    3. Continue to configure other interfaces as required
3. Input your device ID and license key

    > **Note**: Please see [more about devices](more-about-devices) for further information. 
      
    1. Login to the virtual appliance using your management interface and a secure shell client
    2. Select **Input license key**
    3. Input your `Device Name` and `License Key` from [ETS](https://ets.leocybersecurity.com/).  Your virtual appliance will reach out
       and download a custom configuration for your device from LEO at this step

At this point, your virtual appliance will reach out to the LEO management VPN and being deploying our technology stack.  Depending on your Internet connection, this can take between 10 and 30 minutes.

# Post configuration tasks

You can follow along with the deployment by tracking the **status** page.

