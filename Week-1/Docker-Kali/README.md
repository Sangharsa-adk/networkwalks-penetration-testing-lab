# Kali Linux Docker Environment

## Objective

Deploy a Kali Linux penetration testing environment inside Docker
using Arch Linux as the host operating system.

## Base Image

The environment uses:

```text
kalilinux/kali-rolling

## Container

The Kali service is configured through the project's Docker Compose file.

Current container name:
networkwalks_internship

##Docker Network
The Kali container is attached to the shared Docker network:
pentest-lab

This network allows communication with the Windows target container.

## Workspace
The host project workspace is mounted into Kali:

Host:
./workspace

Container:
/workspace

This allows lab scripts and project files to persist outside the
container filesystem.

## Display Support
The container is configured with the host X11 socket:
/tmp/.X11-unix
and receives the host DISPLAY environment variable.

## Security Tools
Additional security and development packages were installed inside
the Kali environment during Week 1.

These include tools for:

Network reconnaissance
Network connectivity testing
SMB testing
Python network automation
Security testing
Android security experimentation

Detailed package information is documented under:

Optional Kali Tools
