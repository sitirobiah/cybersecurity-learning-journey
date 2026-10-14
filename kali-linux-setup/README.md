# Kali Linux Setup on a Virtual Machine

## `1. Objective`

> The objective of this setup is to install and run Kali Linux in a virtual machine for cybersecurity learning, networking practice, and penetration testing labs.
>
> Running Kali Linux in a virtual machine provides an isolated environment where I can explore Linux commands, configure network settings, and practice security tools without installing Kali Linux directly on my main operating system.

## `2. Tools and Requirements`

> The following tools are required to set up the virtual environment.

- **Virtualization Software:** [Oracle VM VirtualBox](https://www.virtualbox.org/) or [VMware Workstation](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
- **Kali Linux Download:** [Official Kali Linux Downloads](https://www.kali.org/get-kali/)
- **Host Operating System:** Windows, Linux, or another supported operating system
- **Internet Connection:** Required to download installation files and system updates

## `3. Virtual Machine Configuration`

> The following settings are a practical starting point for a Kali Linux learning environment. Actual performance depends on the host computer's available resources and the workload.

| Component | Recommended Starting Point |
|---|---|
| RAM | 4 GB |
| Virtual CPUs | 2 cores |
| Virtual Disk | 40–80 GB |
| Network Adapter | NAT |
| System Architecture | Match the downloaded image to the host and virtualization platform |

> Allocate resources according to your computer's capabilities. The virtual machine shares hardware resources with the host operating system, so avoid allocating too much RAM or CPU capacity.

## `4. Installation Methods`

> Kali Linux can be set up using either an ISO installer or an official prebuilt virtual machine image.

### `Method A: Install from an ISO Image`

> This method provides an opportunity to learn the operating system installation process.

1. Download the appropriate Kali Linux ISO from the [official website](https://www.kali.org/get-kali/).
2. Download and install VirtualBox or VMware Workstation.
3. Open the virtualization software and create a new virtual machine.
4. Select the downloaded Kali Linux ISO as the installation media.
5. Configure the RAM, CPU cores, and virtual disk.
6. Start the virtual machine and follow the on-screen installation instructions.
7. Complete the installation and reboot the virtual machine.
8. Remove or disconnect the ISO installer if prompted, then boot into the installed system.

### `Method B: Import a Prebuilt Virtual Machine`

> Kali Linux also provides prebuilt virtual machine images. This method is generally faster because the operating system is already installed and configured for the supported virtualization platform.

1. Visit the [official Kali Linux download page](https://www.kali.org/get-kali/).
2. Download the VirtualBox or VMware image that matches your virtualization software.
3. Extract the downloaded archive if required.
4. Import or open the virtual machine using the appropriate configuration file.
5. Review the virtual machine's hardware settings.
6. Start Kali Linux and verify that the system boots correctly.

> Always use official Kali Linux downloads and verify file checksums when applicable. For detailed instructions, refer to the [official VirtualBox installation guide](https://www.kali.org/docs/virtualization/install-virtualbox-guest-vm/) and [prebuilt VM import guide](https://www.kali.org/docs/virtualization/import-premade-virtualbox-vm/).

## `5. Initial Setup and Verification`

> After starting Kali Linux for the first time, I verify that the system is working properly before beginning cybersecurity exercises.

- Confirm that Kali Linux boots successfully.
- Check that the mouse, keyboard, and display work correctly.
- Verify network connectivity.
- Check the installed Kali Linux version.
- Update the system packages when appropriate.
- Create an initial snapshot before making significant changes.

> To check the Kali Linux version, open a terminal and run:

```bash
cat /etc/os-release
```

> To update the package list and upgrade installed packages:

```bash
sudo apt update
sudo apt full-upgrade
```

> System upgrades may take time and require additional disk space. I make sure the VM has sufficient resources and a recovery point before performing major updates.

## `6. Network Configuration`

> I use NAT as the initial network configuration because it generally allows Kali Linux to access the internet through the host computer without exposing the VM directly as a separate device on the local network.
>
> For specific cybersecurity labs, other network modes may be appropriate. Host-only or internal networking can help isolate lab machines, while bridged networking connects the VM more directly to the physical network.
>
> Network settings should be selected according to the lab requirements and the intended level of isolation.

## `7. Important Considerations`

> - Use official Kali Linux images.
> - Check hardware compatibility and enable hardware virtualization if required.
> - Allocate sufficient RAM, CPU cores, and storage.
> - Create snapshots before installing unfamiliar tools or changing system configurations.
> -
