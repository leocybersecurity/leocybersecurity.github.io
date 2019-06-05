---
layout: page
title: Available Features
permalink: /virtual-appliance/available-features-1.0.html
exclude: True
---

# About this document
This document describes the features available for the LEO Virtual Appliance version 1.0 product.

# IDS
This is a typical intrusion detection framework that utilizes standard and custom rules to identify normal, abnormal, and malicious network traffic. We use the IDS to add context to network telemetry and to supplement the data we receive directly from endpoint agents.

# Flow Monitoring
Flow monitoring records all network connections metadata. E.g. source and destination IP and ports, port independent protocol identification, amount of data sent and received, TCP and UDP specific data, and more. This is used to analyze endpoint and application behavior.

# HTTPS fingerprinting
Fingerprinting HTTPS connections is essentially capturing the metadata surrounding the secure connection.  This meta-data of can be used to infer what clients generated the encrypted traffic.

# File fingerprinting
The metadata of unencrypted files sent over the monitored network can be used to identify malicious, unwanted, and other files and their types.
