# upgrade-kernel-6.8
A step-by-step guide to upgrading the Ubuntu kernel to 6.8.0-52-generic (HWE) on Ubuntu 22.04 LTS. Includes installation via standard updates, manual installation, GRUB update, and kernel verification.

# Upgrade to Kernel 6.8.0-52-generic (HWE) in Ubuntu

## Step-by-Step Guide

### 1. Check Current Kernel Version

```bash
uname -r
```

### 2. Update the Package List

```bash
sudo apt update
```

### 3. Install the Kernel via Standard System Update (For Ubuntu 22.04 Users)

```bash
sudo apt update && sudo apt upgrade -y
```

### 4. (Optional) Manually Install the Target Kernel Version

*Use this step only if the kernel was not installed after running the update and upgrade commands in Step 3.*

#### Install Specific Kernel Version

```bash
sudo apt install linux-image-6.8.0-52-generic linux-headers-6.8.0-52-generic linux-modules-6.8.0-52-generic
```

#### Install HWE Generic Package

```bash
sudo apt install linux-generic-hwe-22.04
```

### 5. Update GRUB

```bash
sudo update-grub
```

### 6. Reboot and Select Kernel

```bash
sudo reboot
```

### 7. Verify the Kernel Version

```bash
uname -r
```
