# DNS/DHCP Playbook

Configure Bind9 and ISC DHCP Server with support for multiple subnets, zonefiles,
and dynamic DNS of DHCP clients.

## Server

This playbook is designed for an Ubuntu 14.04 LTS server. The server should be
the only host listed in the [`hosts`](hosts.example) file.

## Configuration

In the [`vars/main.yml`](vars/main.yml.example) file, set up one subnet that is
marked as authoritative (DHCP is enabled), and any additional subnets if you
would like to configure additional DNS zones for the systems listed in it.

Each subnet may have a list of systems that receive statically allocated IPs,
and may have additional DNS records configured in the `additional_records`
section.
