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

###

