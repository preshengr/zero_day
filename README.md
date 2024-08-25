# 0x00-vagrant

## Overview

This repository contains a directory named `0x00-vagrant` and within it, a file called `0-hello_ubuntu`. This project is intended to familiarize you with Vagrant, a tool for building and managing virtualized development environments. The `0-hello_ubuntu` file will be used to test your Vagrant setup.

## Prerequisites

Before you start, make sure you have the following software installed:

- **Vagrant:** Vagrant is used to manage virtual machines. You can download it from [Vagrant's official website](https://www.vagrantup.com/).
- **VirtualBox:** Vagrant typically works in tandem with VirtualBox to create virtual environments. Download it from [VirtualBox's official website](https://www.virtualbox.org/).

## Project Structure

Here’s the structure of the repository:

```plaintext
/
└── 0x00-vagrant
    └── 0-hello_ubuntu
```

- **0x00-vagrant/**: This directory contains the file `0-hello_ubuntu`.
- **0-hello_ubuntu**: This file will store the output of a command that you will run inside the virtual machine managed by Vagrant.

## Setup Guide

### Step 1: Install Vagrant and VirtualBox

1. **Install VirtualBox**:
   - Go to [VirtualBox's download page](https://www.virtualbox.org/wiki/Downloads) and download the installer for your operating system.
   - Run the installer and follow the instructions to complete the installation.

2. **Install Vagrant**:
   - Go to [Vagrant's download page](https://www.vagrantup.com/downloads) and download the installer for your operating system.
   - Run the installer and follow the instructions to complete the installation.

### Step 2: Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/yourusername/your-repository-name.git
cd your-repository-name/0x00-vagrant
```

### Step 3: Initialize and Start Vagrant

1. **Initialize Vagrant**:
   - Inside the `0x00-vagrant` directory, run the following command to initialize your Vagrant environment:

     ```bash
     vagrant init ubuntu/bionic64
     ```

   - This command will create a `Vagrantfile` in your directory, which Vagrant uses to configure the virtual machine.

2. **Start the Vagrant Environment**:
   - Run the following command to start the virtual machine:

     ```bash
     vagrant up
     ```

   - This command will download the specified box (if not already available) and create a virtual machine.

### Step 4: Access the Virtual Machine

1. **SSH into the Virtual Machine**:
   - Once the virtual machine is up, you can SSH into it using:

     ```bash
     vagrant ssh
     ```

2. **Check Ubuntu Version**:
   - Inside the virtual machine, run the following command to check the version of Ubuntu:

     ```bash
     lsb_release -a
     ```

   - The output of this command should include details about the Ubuntu version.

### Step 5: Create and Modify the `0-hello_ubuntu` File

1. **Create the `0-hello_ubuntu` File**:
   - Inside the virtual machine, create a file named `0-hello_ubuntu`:

     ```bash
     echo "Hello Ubuntu" > /vagrant/0-hello_ubuntu
     ```

   - The `/vagrant` directory inside the virtual machine maps to your `0x00-vagrant` directory on your host machine, so this will create the file in the appropriate location.

2. **Verify the File**:
   - On your host machine, navigate to the `0x00-vagrant` directory and check that the `0-hello_ubuntu` file has been created with the content `Hello Ubuntu`.

### Step 6: Clean Up

1. **Exit the Virtual Machine**:
   - Type `exit` to leave the SSH session.

2. **Shut Down the Virtual Machine**:
   - Run the following command to shut down the virtual machine:

     ```bash
     vagrant halt
     ```

3. **Destroy the Virtual Machine** *(Optional)*:
   - If you want to remove the virtual machine entirely, run:

     ```bash
     vagrant destroy
     ```

## Conclusion

You have successfully set up a Vagrant environment and created a file within it. This setup is a fundamental step in using Vagrant to manage virtualized development environments efficiently.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
