# OMARCHY VM for UTM

A pre-configured Arch Linux virtual machine for UTM, ready to use with minimal setup.

## 🚀 Quick Start

### Prerequisites

#### Installing UTM

UTM is a powerful virtualization application for macOS and iOS that uses QEMU under the hood.

**For macOS:**
- **Download from App Store:** [UTM on Mac App Store](https://apps.apple.com/us/app/utm-virtual-machines/id1538878817) (Paid, supports development)
- **Download from GitHub:** [UTM Releases](https://github.com/utmapp/UTM/releases) (Free)
  1. Download the latest `.dmg` file
  2. Open the DMG and drag UTM to Applications
  3. On first launch, you may need to right-click and select "Open" due to Gatekeeper

**For iOS/iPadOS:**
- Available on the [App Store](https://apps.apple.com/us/app/utm-se-retro-pc-emulator/id1564628856)

**System Requirements:**
- macOS 11 Big Sur or later (Apple Silicon or Intel)
- At least 8GB RAM recommended
- 20GB free disk space for the VM

### Installation

1. **Download the VM:**
   - Go to the [Releases](https://github.com/hjanuschka/OMARCHY-VM-UTM/releases) page
   - Download the latest `.utm` file from the assets

2. **Import into UTM:**
   - Double-click the downloaded `.utm` file, OR
   - Open UTM and drag the `.utm` file into the UTM window, OR
   - In UTM, go to File → Import Virtual Machine

3. **Start the VM:**
   - Select the OMARCHY VM in UTM
   - Click the Play button to start

## 🔑 Login Credentials

The VM includes two user accounts:

| Username | Password | Access Level |
|----------|----------|--------------|
| `root`   | `arch`   | Administrator |
| `arch`   | `arch`   | Standard User |

**⚠️ Security Note:** Please change these default passwords after first login using the `passwd` command.

## 📦 What's Included

This OMARCHY VM comes pre-configured with:

- **Base System:** Arch Linux (latest)
- **Desktop Environment:** [Specify if any - e.g., GNOME, KDE, XFCE, or minimal]
- **Development Tools:** 
  - Git
  - Base development packages
  - [List other pre-installed tools]
- **Network:** Configured with DHCP
- **Storage:** [Specify disk size]

## 🛠️ Configuration

### VM Specifications
- **RAM:** [Specify allocated RAM]
- **CPU Cores:** [Specify number of cores]
- **Display:** [Specify display settings]
- **Architecture:** [x86_64 or ARM64]

### Network Configuration
The VM is configured to use NAT networking by default. To access the VM via SSH from your host:
```bash
ssh arch@localhost -p [port]  # Port will be shown in UTM network settings
```

### Shared Folders
To set up shared folders between host and VM:
1. In UTM, select the VM and click Settings
2. Go to Sharing section
3. Add directories you want to share
4. Mount in the VM using the appropriate commands

## 📝 First Steps After Installation

1. **Update the system:**
   ```bash
   sudo pacman -Syu
   ```

2. **Change default passwords:**
   ```bash
   passwd  # For current user
   sudo passwd root  # For root user
   ```

3. **Configure timezone:**
   ```bash
   sudo timedatectl set-timezone Your/Timezone
   ```

4. **Install additional packages as needed:**
   ```bash
   sudo pacman -S package-name
   ```

## 🤝 Contributing

Feel free to open issues or submit pull requests if you have suggestions for improvements or encounter any problems.

### Building Your Own Version

If you want to customize this VM:
1. Import the base VM into UTM
2. Make your modifications
3. Export the VM: Right-click → Share → Save
4. Create a pull request with your changes documented

## 📄 License

This VM image is provided as-is for educational and development purposes. Arch Linux and all included software retain their respective licenses.

## 🔗 Resources

- [UTM Documentation](https://docs.getutm.app/)
- [Arch Linux Wiki](https://wiki.archlinux.org/)
- [UTM GitHub Repository](https://github.com/utmapp/UTM)
- [OMARCHY Project](https://github.com/hjanuschka/OMARCHY-VM-UTM)

## ⚠️ Disclaimer

This is an unofficial Arch Linux distribution. For official Arch Linux downloads, please visit [archlinux.org](https://archlinux.org/).

---

**Need Help?** Open an [issue](https://github.com/hjanuschka/OMARCHY-VM-UTM/issues) on GitHub.