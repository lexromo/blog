---
title: "SSH authorized_keys file"
date: 2024-04-04T23:15:00+07:00
slug: 
category: 
summary:
description: 
cover:
  image: "ssh.png"
  alt:
  caption: 
  relative: true
showtoc: true
draft: false
---

# Hello everyone!


I'm back again. Right now, I'm diving into learning how to use Ansible. And guess what? While I was learning some new stuff, I realized something important—I didn't have an authorized_keys file. So, it's time to figure out how to deal with that!

## What is an Authorized_keys file in SSH?

The SSH authorized_keys file is a critical component of SSH (Secure Shell) authentication. It's a file located on the server that contains a list of public keys that are authorized to access the server. When a client attempts to connect to the server via SSH, the server checks the authorized_keys file to see if the client's public key matches any of the keys listed within it. If a match is found, the client is granted access without needing to enter a password. This mechanism provides a secure and convenient way to manage access to the server, particularly in environments where multiple users or automated processes need to connect remotely.

    ~/.ssh/authorized_keys file

## Lets understand SSH Authentication Keys


1. **Key Generation:** Users create a pair of keys: a private key and a public key. The private key remains on the user's local machine and serves as their authentication credential. Meanwhile, the public key is distributed to remote servers to confirm the user's identity.

2. **Public Key Installation:** Users upload their public key onto the remote server(s) they intend to access by appending it to the server's authorized_keys file. Typically, this file resides in the user's home directory on the remote server.

3. **Initiating Connection:** Users commence an SSH connection with the remote server by specifying the server's IP address or hostname and providing the path to their private key.

4. **Authentication:** Upon receiving the connection request, the remote server presents a challenge to the user. This challenge gets encrypted using the user's public key. Subsequently, the user decrypts the challenge using their private key and returns the decrypted response to the server.

5. **Access Granted:** If the decrypted response aligns with the anticipated value, the remote server authorizes access for the user, allowing them to log in securely.

The SSH protocol operates with two integral components: the client and the server. SSH key-based authentication leverages cryptographic keys to validate the user's authorization.

When the correct SSH key is provided, it enables users to log in seamlessly without requiring manual input of a username or password.

Let's delve deeper into the mechanics.

The SSH authorized_keys file resides within the user's home directory on the remote server. Its purpose is to catalog the public keys authorized for accessing the user's account.

During an SSH key-based login attempt, the server cross-references the user's public key with entries in the authorized_keys file to confirm the user's legitimacy.

While it's feasible to manually modify authorized_keys to manage keys, best practice advocates for utilizing the ssh-copy-id command. This command streamlines the process by appending the user's public key to the remote server's authorized_keys file, preserving existing keys, and adjusting file permissions to facilitate SSH key-based authentication.

The authorized_keys file assumes a pivotal role in this authentication flow by housing the public keys sanctioned for server access.

Administrators wield control over server access by administering the authorized_keys file. They possess the capability to grant or revoke access by adding or removing a user's public key from the file, thereby regulating server entry.

## Inspect the contents of the authorized_keys file:

To inspect the contents of the authorized_keys file, there are several methods available, including using a text editor or command-line tools such as cat or less.

Here's a step-by-step guide using the cat command:

Open a terminal window on your system.

Navigate to the .ssh directory by entering the following command:
    cd ~/.ssh

Once you're in the .ssh directory, use the cat command to display the contents of the authorized_keys file. Type the following command:
    cat authorized_keys


Executing this command will render the content of the file directly within the terminal interface.

## Create the .ssh directory and the authorized_keys file the first time.

You might not have a .ssh directory and the authorized_keys file, so lets fix that!

Create the .ssh directory: 

    mkdir ~/.ssh

Set the right permissions:

    chmod 700 ~/.ssh

Create the authorized_keys file:

    touch ~/.ssh/authorized_keys

Set the right permissions:

    chmod 600 ~/.ssh/authorized_keys


The permissions are very very important! It won't work without the right permissions!

Now you can add the public key to the authorized_keys file:

    cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys




##

MORE COMMING UP!
