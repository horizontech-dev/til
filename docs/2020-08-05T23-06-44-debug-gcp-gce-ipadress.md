---
date: 2020-08-05T23:06:44-07:00
title: Debug-Gcp-Gce-Ipadress
tags: GCP
---

# Debug-Gcp-Gce-Ipadress

- The public IP of a GCE is ephemeral. There are a couple of ways one can make it static https://cloud.google.com/compute/docs/ip-addresses/reserve-static-external-ip-address
- If the IP address changes, you likely need to change your DNS A record too
- GCE also provides console access https://cloud.google.com/compute/docs/instances/interacting-with-serial-console

