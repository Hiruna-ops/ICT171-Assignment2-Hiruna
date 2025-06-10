ICT171 Assignment 2 - OpenVPN Server Project

Student Name: Hiruna Randika Perera  
Student ID: 35536505  
Public IP: 3.107.28.187  

Overview

This project demonstrates the deployment of a secure OpenVPN server hosted on an AWS EC2 instance. It includes server configuration, client VPN setup, automation via Bash scripting, and accessible documentation for reproducibility.

Server Setup Steps

1. Launched a new Ubuntu EC2 instance on AWS.
2. Connected using PEM key with SSH:  
   ssh -i ict171-key.pem ubuntu@3.107.28.187
3. Downloaded and ran the OpenVPN script:  
   bash
   wget https://git.io/vpn -O openvpn-install.sh
   chmod +x openvpn-install.sh
   sudo ./openvpn-install.sh
   
4. Followed prompts to generate client1.ovpn.
5. Downloaded the config using SCP:
   bash
   scp -i ict171-key.pem ubuntu@3.107.28.187:/home/ubuntu/client1.ovpn .
   

Script Purpose

The vpn-install.sh script automates:
- OpenVPN installation
- Key and certificate generation
- Firewall rules
- TLS setup
- Client configuration generation

File Structure

- client1.ovpn – Client config for OpenVPN GUI
- vpn-install.sh – Script used to install and configure OpenVPN
- README.md – This documentation
- screenshots/ – Screenshots for proof of setup
- demo_script.txt – Script for final video walkthrough

Video Link


References

- https://github.com/angristan/openvpn-install  
- https://openvpn.net/community-resources/how-to/  
