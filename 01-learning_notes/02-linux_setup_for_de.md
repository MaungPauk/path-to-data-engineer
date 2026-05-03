<h1 align="center">
    <strong>Linux for Data Engineering</strong>
</h1>
<h3 align="center">
    <i>____by Maung Pauk</i>
</h3>

---
Linux is the backbone of most data engineering environments—from local development to cloud infrastructure. Many production systems, including servers and containers, run on Linux, so knowing it gives you a practical edge.

### Why Linux matters:

- **Command-line efficiency**  
  The shell (e.g., Bash) lets you automate workflows, manipulate files, and process data quickly using tools like `grep`, `awk`, and `sed`.

- **Automation & scripting**  
  You can write shell scripts to automate ETL tasks, schedule jobs (via `cron`), and manage pipelines.

- **Environment consistency**  
  Most cloud platforms and data tools run on Linux, so developing in Linux reduces “it works on my machine” issues.

- **Tool compatibility**  
  Technologies like Docker, Apache Airflow, and Apache Spark are designed with Linux environments in mind.

- **Resource efficiency & control**  
  Linux gives better control over system resources, permissions, and networking—important when handling large-scale data workloads.

---

## Advantages of Using WSL (Linux on Windows)

WSL (Windows Subsystem for Linux) allows you to run a real Linux environment directly inside Windows without a virtual machine.

### Key advantages:

- **Native Linux experience without dual boot**  
  You can use Ubuntu or other distros alongside Windows—no need to switch operating systems.

- **Seamless integration with Windows tools**  
  Access Windows files from Linux and use editors like Visual Studio Code across both environments.

- **Lightweight compared to virtual machines**  
  WSL uses fewer resources than traditional VMs, making it faster to start and easier to manage.

- **Perfect for learning and development**  
  Practice Linux commands, run Python scripts, and build pipelines in a real Linux-like environment.

- **Great for containerization**  
  Works smoothly with Docker Desktop, enabling you to build and run containers just like in production.

---

## WSL Linux Setup in Windows 11

I am a Windows user and this is a step-by-step notes to install and configure Windows Subsystem for Linux (WSL 2) on Windows 11 for Data Engineering workflows.

---

## 1. Requirements

Before starting, ensure:

* Windows 11 (Build 22000 or later)
* Virtualization enabled in BIOS (usually enabled by default)

---

## 2. Install WSL

Open **PowerShell as Administrator** and run:

```bash
wsl --install
```

### What this does:

* Enables required Windows features
* Installs WSL 2
* Installs Ubuntu (default Linux distribution)
* Sets WSL 2 as default version

---

## 3. Restart Your Computer

After installation completes, restart your system to apply changes.

---

## 4. Initial Linux Setup

After reboot, Ubuntu (or your chosen Linux distro) will launch.

You will be prompted to:

* Create a Linux username
* Set a Linux password

> Note: This is separate from your Windows login.

---

## 5. Verify Installation

Run the following command in PowerShell or Windows Terminal:

```bash
wsl -l -v
```

You should see output similar to:

```
NAME      STATE           VERSION
Ubuntu    Running         2
```

---

## 6. Update Linux Packages

Inside your WSL terminal, run:

```bash
sudo apt update && sudo apt upgrade -y
```

---

## 7. Install Essential Data Engineering Tools

Install commonly used tools:

```bash
sudo apt install -y python3 python3-pip git curl wget unzip
```

Optional build tools:

```bash
sudo apt install -y build-essential
```

---

## 8. Install VS Code Integration

Install Visual Studio Code and the **Remote - WSL** extension.

See more details about [*Visual Studio Code (VSCode) installation](03-vscode_setup.md)

Then open WSL projects directly in VS Code:

```bash
code .
```

---

## 9. Docker Integration (Optional but Recommended)

Install Docker Desktop on Windows and enable WSL integration.

This allows running containers directly inside Linux environment.

---

## 10. Set WSL 2 as Default (If Needed)

```bash
wsl --set-default-version 2
```

---

## Best Practices for Data Engineering

* Store projects inside Linux filesystem:

  ```
  /home/your-username/projects
  ```

  (Faster than Windows-mounted drives)

* Use Git inside WSL for production-like workflows

* Keep environment reproducible using requirements files or Docker

---

## Basic linux commands
```bash
ls #

```

---

**[↑ Up](/README.md)** | **[← Previous](01-de_core_concepts_and_theories.md)** | **[Next →](03-vscode_setup.md)**
