# Windows 11 Docker Target

## Objective

Deploy a Windows 11 environment inside Docker to act as a controlled
target for authorized penetration testing and security laboratory
exercises.

## Base Image

The environment uses:

```text
dockurr/windows

## Container
Current container name:
win-target

## Windows Configuration
The Docker Compose configuration specifies:

Version: Windows 11
RAM:     4 GB
CPU:     2 cores

## Virtualization
The Windows container is configured with:
/dev/kvm
to provide hardware-assisted virtualization.

## Network
The Windows target is connected to:
pentest-lab
the same Docker network used by the Kali container.

## Network Access
The following ports are configured:

Port	Protocol	Purpose
3389	TCP	RDP
3389	UDP	RDP
8006	TCP	Web management interface

## Persistent Storage
Windows storage is mounted through:
./win_data:/storage
The win_data directory contains the Windows environment data and
is intentionally excluded from Git version control.

## Purpose of use
The Windows environment will be used as a controlled target for
authorized security testing and future laboratory exercises.
