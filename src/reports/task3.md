# Task 3 — Network Configuration

Configured hostname, timezone, network interfaces, and static IP settings.

## Hostname Setup

![Hostname](../image_for_md/hostnamectl.png)

Setting machine name with `hostnamectl set-hostname`

## Timezone Configuration

![Timezone](../image_for_md/timedatectl.png)

Setting timezone with `timedatectl set-timezone`

## Network Interfaces

![Network Interfaces](../image_for_md/iplink.png)

Listing all network interfaces with `ip link`

> **lo (loopback)** — virtual network interface used for local testing and services.

## DHCP IP Address

![DHCP](../image_for_md/ipa_and_dhclient.png)

Obtaining IP from DHCP server using `dhclient` and verifying with `ip a`

## Gateway IPs

![Gateway](../image_for_md/iproute.png)

Displaying internal and external gateway IPs with `ip route`, `hostname -I`, and `curl ifconfig.me`

## Static Network Configuration

![Netplan](../image_for_md/netplan.png)

Configuring static IP, gateway, and DNS via `/etc/netplan/` YAML file.

## Verification After Reboot

![Network Result](../image_for_md/result_network_setting.png)

Confirming static settings persist after reboot.

## Connectivity Test

![Ping](../image_for_md/ping.png)

Successfully pinging remote hosts with 0% packet loss.
