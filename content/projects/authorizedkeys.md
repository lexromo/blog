---
title: "SSH authorized_keys file"
date: 2024-04-04T23:15:00+07:00
slug: 
category: 
summary:
description: 
cover:
  image:  
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

