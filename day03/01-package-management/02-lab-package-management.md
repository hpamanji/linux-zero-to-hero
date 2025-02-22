## Session 01 : Package Management in Linux

In this session, we’ll explore how to manage software packages in Linux. Package management is a critical skill for installing, updating, and removing software on your system. By the end of this session, you’ll be comfortable using package managers like `apt` (for Debian-based systems) and `yum`/`dnf` (for Red Hat-based systems).

---

### What is a Package Manager?
A package manager is a tool that automates the process of installing, updating, configuring, and removing software packages. It resolves dependencies and ensures that software is installed correctly.

### Key Concepts
- **Package**: A compressed archive containing software files, metadata, and instructions for installation.
- **Repository**: A collection of packages hosted on a server. Package managers fetch packages from repositories.
- **Dependencies**: Other software packages required for a package to function correctly.

### Common Package Managers
- **APT (Advanced Package Tool)**: Used in Debian-based distributions like Ubuntu.
- **YUM/DNF**: Used in Red Hat-based distributions like CentOS and Fedora.
- **RPM (Red Hat Package Manager)**: A low-level package manager used in Red Hat-based systems.

---

### Hands-On Lab: Managing Packages

#### Objective
Learn how to install, update, and remove packages using package managers.

#### Step 1: Update Package Lists

1. **For Debian-based systems (e.g., Ubuntu):**
   ```bash
   sudo apt update
   ```

2. **For Red Hat-based systems (e.g., CentOS):**
   ```bash
   sudo yum check-update
   ```
   or
   ```bash
   sudo dnf check-update
   ```

---

#### Step 2: Install a Package

- **For Debian-based systems:**
  ```bash
  sudo apt install vim
  ```

- **For Red Hat-based systems:**
  ```bash
  sudo yum install vim
  ```
  or
  ```bash
  sudo dnf install vim
  ```

---

#### Step 3: Update Installed Packages

- **For Debian-based systems:**
  ```bash
  sudo apt upgrade
  ```

- **For Red Hat-based systems:**
  ```bash
  sudo yum update
  ```
  or
  ```bash
  sudo dnf upgrade
  ```

---

#### Step 4: Remove a Package

- **For Debian-based systems:**
  ```bash
  sudo apt remove vim
  ```

- **For Red Hat-based systems:**
  ```bash
  sudo yum remove vim
  ```
  or
  ```bash
  sudo dnf remove vim
  ```

---

#### Step 5: Search for a Package

- **For Debian-based systems:**
  ```bash
  apt search vim
  ```

- **For Red Hat-based systems:**
  ```bash
  yum search vim
  ```
  or
  ```bash
  dnf search vim
  ```

---

#### Step 6: Clean Up

- **For Debian-based systems:**
  ```bash
  sudo apt autoremove
  ```

- **For Red Hat-based systems:**
  ```bash
  sudo yum autoremove
  ```
  or
  ```bash
  sudo dnf autoremove
  ```

---

### Best Practices and Common Issues

#### Best Practices
- **Regularly Update Your System**: Keep your system secure and up-to-date by regularly updating packages.
- **Use Official Repositories**: Stick to official repositories to avoid installing malicious software.
- **Read Package Descriptions**: Before installing a package, read its description to ensure it’s what you need.

#### Common Issues
- **Breaking Dependencies**: Avoid manually installing packages that might conflict with system dependencies.
- **Ignoring Updates**: Failing to update your system can leave it vulnerable to security threats.
- **Using Unverified Repositories**: Adding untrusted repositories can lead to installing malicious software.
