# Optional Work — Docker Network Configuration

## Overview

The Kali Linux and Windows 11 containers were configured to operate
on the same Docker bridge network.

## Network

Network name:

```text
pentest-lab

## Driver:
bridge

## Architecture

                 Arch Linux
                     |
                   Docker
                     |
              pentest-lab
                     |
          ┌──────────┴──────────┐
          │                     │
          ▼                     ▼
       Kali Linux          Windows 11
    networkwalks_        win-target
     internship

## Purpose
The shared network provides an isolated environment where Kali can
communicate with the Windows target for authorized security testing.

## Verification
Container status can be checked using:
docker ps

The Docker network can be inspected using:
docker network inspect pentest-lab

