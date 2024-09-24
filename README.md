# Pentbox 1.8 Setup and Usage Guide

Pentbox is a simple and powerful network security testing toolkit written in Ruby. This guide will walk you through the installation, setup, and usage of Pentbox 1.8, focusing on the honeypot functionality for network monitoring and security.

## Overview

Pentbox provides a collection of security and network tools that can be used for testing and monitoring purposes. One of its main features is the honeypot, which can be easily configured to monitor traffic and potential intrusions on your network.

## Installation

### Prerequisites

- Ruby installed on your server (ensure Ruby is installed before proceeding).

### Steps to Install and Run Pentbox 1.8

1. **Download Pentbox 1.8**

   Download the Pentbox 1.8 tarball from SourceForge using the following command:

   ```bash
   wget http://downloads.sourceforge.net/project/pentbox18realised/pentbox-1.8.tar.gz
   ```

2. **Extract the Downloaded File**

   Extract the contents of the tarball using the tar command:

   ```bash
   tar xvfz pentbox-1.8.tar.gz
   ```

3. **Navigate to the Pentbox Directory**

   Change into the extracted directory:

   ```bash
   cd pentbox-1.8
   ```

4. **Run Pentbox**

   Start Pentbox using the Ruby interpreter:

   ```bash
   ./pentbox.rb
   ```

## Using Pentbox as a Honeypot

### Server-Side Configuration

1. **Start Pentbox**

   Run the Pentbox executable:

   ```bash
   ./pentbox
   ```

2. **Navigate Through the Menu**

   - Select **Network Tools**.
   - Choose **Honeypot**.
   - Select **Fast Auto Configuration**.

   The system will automatically configure the honeypot, and a port number will be displayed on the screen. This port is where the honeypot will be active and listening for incoming connections.

### Client-Side Testing

1. **Find Your IP Address**

   On the client machine, use the following command to find the IP address (look for the `inet` field):

   ```bash
   ifconfig
   ```

2. **Access the Honeypot**

   Open a web browser on the client machine and type the following in the address bar:

   ```
   http://<server-ip-address>:<port-number>
   ```

   Replace `<server-ip-address>` with the server's IP address and `<port-number>` with the port number displayed during the honeypot configuration.

3. **Monitor Activity**

   On the server terminal, you should see logs and details of any activity happening through the honeypot, including connections made by the client.

## Conclusion

Pentbox's honeypot feature allows you to monitor and analyze potential threats by setting up a simple trap on your network. This guide covers the basic setup and testing procedure. For more advanced configurations and options, refer to the Pentbox documentation.


## Made By
  - Tejas Shivaprasad
  - Moulya A S
  
