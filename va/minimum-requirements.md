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
    * 8 GB RAM
    * Disks:
        * 20 GB root mount
        * 20 GB opt mount
        * 20 GB var mount
        * 4 GB swap mount
* Virtual Machine
    * 1 CPU core + 1 for each 250 Mbps of inspected traffic
    * 8 GB RAM
    * Disks:
        * 60 GB root mount
        * 0 GB swap mount
* Minimum Configuration
    * 2 CPU core
    * 4 GB RAM
    * 50 GB root mount

# Important Notes
* One CPU can manage about 250Mbps of traffic inspection
* We recommend at least on CPU allocated just for the OS
* Minimum recommended configuration, therefore, should be at least 2 CPUs
