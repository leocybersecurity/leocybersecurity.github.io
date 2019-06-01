---
layout: page
title: Minimum Requirements
permalink: /virtual-appliance/minimum-requirements.html
exclude: True
---

# About this document

This document describes the hardware requirements for your Virtual Appliance.

# Recommended Configurations
* Physical machine
    * 1 CPU core + 1 for each 250 Mbps of inspected traffic
    * 8 GB RAM + 4 GB per core
    * 2 network interfaces
    * Disks:
        * 20 GB root mount
        * 20 GB opt mount + 10 GB per core
        * 20 GB var mount
        * 4 GB swap mount
* Virtual Machine
    * 1 CPU core + 1 for each 250 Mbps of inspected traffic
    * 8 GB RAM + 4 GB per core 
    * 2 network interfaces
    * Disks:
        * 60 GB root mount + 10 GB per core
        * 0 GB swap mount
* Minimum Configuration
    * 2 CPU core
    * 4 GB RAM
    * 50 GB root mount
    * 1 network interface

# More about CPU configurations
* One CPU can manage about 250Mbps of traffic inspection
* We recommend at least on CPU allocated just for the OS
* Minimum recommended configuration, therefore, should be at least 2 CPUs

# More About Network Interface Configurations
Whether running on a physical or virtual machine, we recommend two interfaces with 1 GB capability.  There should be:
* One dedicated to managing the appliance (management interface)
* One dedicated to recieving mirrored traffic from you network (monitoring interface)
The monitoring interface will recieve a large volume of traffic.  We recommend physically isolating this interface as much as possible from other hosts, vi
rtual machines, etc. to prevent those machines from suffering network latency.
