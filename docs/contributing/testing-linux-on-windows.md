# Linux Testing Environment on Windows

## Overview
This guide describes setting up an isolated Linux testing environment using Hyper-V for validating our development templates.

## Why Hyper-V over WSL2?
- Complete system isolation
- Snapshot support for clean testing states
- Full control over system resources
- Better multi-distro testing capabilities
- True network isolation options
- More representative of real Linux environments

## Setup Instructions
1. Enable Hyper-V feature in Windows
2. Create a new Virtual Switch (recommend both External and Internal networks)
3. Download your preferred Linux distribution ISO
4. Create a new VM with:
   - Generation 2 VM (for UEFI support)
   - Adequate resources (recommend 4GB RAM, 2 vCPUs minimum)
   - Dynamic memory enabled
   - Multiple network adapters if needed

## Testing Workflow
1. Create a base VM image with minimal setup
2. Take a snapshot as your "clean state"
3. Run your tests
4. Revert to snapshot for next test run

## Network Configuration Options
1. Isolated: Internal switch only
2. Internet-enabled: External switch
3. Multi-network: Both switches for complex testing

## Recommended Tools
- Virtual Machine Connection for direct VM access
- PowerShell for VM management
- Hyper-V Manager for GUI management
