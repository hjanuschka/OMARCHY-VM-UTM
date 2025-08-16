# OMARCHY VM for UTM

A pre-configured OMARCHY virtual machine for UTM - a beautiful and productive Linux distribution designed for software developers, featuring Hyprland tiling window manager and a curated set of development tools.

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
   - Download the latest `OMARCHY-VM.utm.tar.gz` file from the assets

2. **Extract the archive:**
   ```bash
   tar -xzf OMARCHY-VM.utm.tar.gz
   ```

3. **Import into UTM:**
   - Double-click the extracted `.utm` bundle, OR
   - Open UTM and drag the `.utm` bundle into the UTM window, OR
   - In UTM, go to File → Import Virtual Machine

4. **Start the VM:**
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

- **Base System:** OMARCHY (based on Arch Linux)
- **Window Manager:** Hyprland - A dynamic tiling Wayland compositor
- **Development Tools:** 
  - Neovim - Advanced text editor
  - Git - Version control
  - Alacritty - GPU-accelerated terminal emulator
  - Base development packages
- **Productivity Applications:**
  - Chromium - Web browser
  - Spotify - Music streaming
  - Typora - Markdown editor
  - LibreOffice - Office suite
  - Zoom - Video conferencing
- **Design Philosophy:** Terminal-heavy workflow with focus on aesthetics and productivity
- **Network:** Configured with DHCP
- **Storage:** Optimized for development workloads

## 🛠️ Configuration

### VM Specifications
- **RAM:** 4GB minimum (8GB recommended for optimal performance)
- **CPU Cores:** 2 cores minimum (4 cores recommended)
- **Display:** Configured for Hyprland with hardware acceleration support
- **Architecture:** x86_64

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

This VM image is provided as-is for educational and development purposes. OMARCHY, Arch Linux, and all included software retain their respective licenses.

## 🎨 About OMARCHY

OMARCHY is a customized Linux distribution that prioritizes both aesthetics and productivity. It's designed specifically for software developers who appreciate a beautiful working environment and are willing to embrace a terminal-heavy workflow. The distribution encourages users to step outside their comfort zone and experience a more hands-on approach to computing.

### Key Philosophy
- **Beauty as Motivation:** A visually appealing environment that inspires productivity
- **Developer-Focused:** Curated selection of development tools and workflows
- **Different by Design:** Intentionally distinct from Windows and macOS
- **Terminal-First:** Embraces command-line efficiency while maintaining visual appeal

## 🔗 Resources

- [OMARCHY Documentation](https://manuals.omamix.org/2/the-omarchy-manual/91/welcome-to-omarchy)
- [UTM Documentation](https://docs.getutm.app/)
- [Hyprland Wiki](https://wiki.hyprland.org/)
- [Arch Linux Wiki](https://wiki.archlinux.org/)
- [UTM GitHub Repository](https://github.com/utmapp/UTM)
- [OMARCHY VM Project](https://github.com/hjanuschka/OMARCHY-VM-UTM)

## ⚠️ Disclaimer

OMARCHY is a customized distribution based on Arch Linux, designed with aesthetics and developer productivity in mind. For official Arch Linux downloads, please visit [archlinux.org](https://archlinux.org/).

---

**Need Help?** Open an [issue](https://github.com/hjanuschka/OMARCHY-VM-UTM/issues) on GitHub.