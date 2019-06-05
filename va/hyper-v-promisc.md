---
layout: page
title: Enabling Promiscuous Mode for Hyper-V
permalink: /virtual-appliance/hyper-v-promisc.html
exclude: True
---

# About this document
This document provides information for network administrators about how to enable promiscuous mode for Microsoft Hyper-V virtual environments.  **Please note:** LEO does not officially support running the LEO Virtual Appliance in a Hyper-V environment at this time.

# How to Enable Promiscuous Mode in Hyper-V
1. If running the Virtual Appliance on Hyper-V R2 2012, please ensure [this hotfix is installed](https://support.microsoft.com/en-us/help/2885541/packet-sniffing-tool-does-not-sniff-all-network-traffic-through-port-m)
2. Open the **Hyper-V Manager** and right-click the machine that you want to use to capture mirrored traffic
3. Select **Settings**
4. Expand the associated network adapter and select **Advanced Features**
5. Scroll to the **Port mirroring** section and set the **Mirroring mode** to "Destination"
6. Click **Apply** and **OK**
7. Open a Windows PowerShell console
8. Enter the following commands:
   1. `$a = Get-VMSystemSwitchExtensionPortFeature -FeatureId 776e0ba7-94a1-41c8-8f28-951f524251b5`
   2. `$a.SettingData.MonitorMode = 2`
   3. `add-VMSwitchExtensionPortFeature -ExternalPort -SwitchName <virtual_switch_name> -MSwitchExtensionFeature $a`
