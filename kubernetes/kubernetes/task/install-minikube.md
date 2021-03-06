# Install Minikube

+ [Before you begin](#before-you-begin)
    + [Linux](#linux)
    + [macOS](#macos)
    + [Windows](#windows)
+ [Installing minikube](#installing-minikube)
    + [Linux](#linux-1)
        + [Install kubectl](#install-kubectl)
        + [Install a Hypervisor](#install-a-hypervisor)
        + [Install Minikube using a package](#install-minikube-using-a-package)
        + [Install Minikube via direct download](#install-minikube-via-direct-download)
    + [macOS](#macos-1)
        + [Install kubectl](#install-kubectl-1)
        + [Install a Hypervisor](#install-a-hypervisor-1)
        + [Install Minikube](#install-minikube-1)
    + [Windows](#windows-1)
        + [Install kubectl](#install-kubectl-2)
        + [Install a Hypervisor](#install-a-hypervisor-2)
        + [Install Minikube using Chocolatey](#install-minikube-using-chocolatey)
        + [Install Minikube using an installer executable](#install-minikube-using-an-installer-executable)
        + [Install Minikube via direct download](#install-minikube-via-direct-download-1)
+ [Cleanup local state](#cleanup-local-state)
+ [What's next](#whats-next)

----------------------------------------------------------------------------------------------------

This page shows you how to install [Minikube](https://kubernetes.io/docs/tutorials/hello-minikube), a tool that runs a single-node Kubernetes cluster in a virtual machine on your personal computer.

## Before you begin

### Linux

To check if virtualization is supported on Linux, run the following command and verify that the output is non-empty:

```shell
egrep --color 'vmx|svm' /proc/cpuinfo
```

### macOS

To check if virtualization is supported on macOS, run the following command on your terminal.

```shell
sysctl -a | grep machdep.cpu.features
```

If you see **`VMX`** in the output, the VT-x feature is supported on your OS.

### Windows

To check if virtualization is supported on Windows 8 and above, run the following command on your Windows terminal or command prompt.

```shell
systeminfo
```

If you see the following output, virtualization is supported on Windows.

```shell
Hyper-V Requirements: VM Monitor Mode Extensions: Yes
                      Virtualization Enabled In Firmware: Yes
                      Second Level Address Translation: Yes
                      Data Execution Prevention Available: Yes
```

If you see the following output, your system already has a Hypervisor installed and you can skip the next step.

```shell
Hyper-V Requirements: A hypervisor has been detected. Features required for Hyper-V will not be displayed.
```

## Installing minikube

### Linux

#### Install kubectl

Make sure you have kubectl installed.

You can install kubectl according to the instructions in [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-linux).

#### Install a Hypervisor

If you do not already have a hypervisor installed, install one of these now:

+ [KVM](https://www.linux-kvm.org/), which also uses QEMU

+ [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

> **`Note`**: Minikube also supports a **`--vm-driver=none`** option that runs the Kubernetes components on the host and not in a VM.
  Using this driver requires [Docker](https://www.docker.com/products/docker-desktop) and a Linux environment but not a hypervisor.

#### Install Minikube using a package

There are **`experimental`** packages for Minikube available; you can find Linux (AMD64) packages from Minikube's [releases](https://github.com/kubernetes/minikube/releases) page on GitHub.

Use your Linux's distribution's package tool to install a suitable package.

#### Install Minikube via direct download

If you're not installing via a package, you can download a stand-alone binary and use that.

```shell
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube
```

Here's an easy way to add the Minikube executable to your path:

```shell
sudo install minikube /usr/local/bin
```

### macOS

#### Install kubectl

Make sure you have kubectl installed.

You can install kubectl according to the instructions in [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-macos).

#### Install a Hypervisor

If you do not already have a hypervisor installed, install one of these now:

+ [HyperKit](https://github.com/moby/hyperkit)

+ [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

+ [VMware Fusion](https://www.vmware.com/products/fusion)

#### Install Minikube

The easiest way to install Minikube on macOS is using [Homebrew](https://brew.sh/):

```shell
brew cask install minikube
```

You can also install it on macOS by downloading a stand-alone binary:

```shell
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64 && chmod +x minikube
```

Here's an easy way to add the Minikube executable to your path:

```shell
sudo mv minikube /usr/local/bin
```

### Windows

#### Install kubectl

Make sure you have kubectl installed.

You can install kubectl according to the instructions in [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl-on-windows).

#### Install a Hypervisor

If you do not already have a hypervisor installed, install one of these now:

+ [Hyper-V](https://msdn.microsoft.com/en-us/virtualization/hyperv_on_windows/quick_start/walkthrough_install)

+ [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

> **`Note`**: Hyper-V can run on three versions of Windows 10: Windows 10 Enterprise, Windows 10 Professional, and Windows 10 Education.

#### Install Minikube using Chocolatey

The easiest way to install Minikube on Windows is using [Chocolatey](https://chocolatey.org/) (run as an administrator):

```shell
choco install minikube kubernetes-cli
```

After Minikube has finished installing, close the current CLI session and restart.

Minikube should have been added to your path automatically.

#### Install Minikube using an installer executable

To install Minikube manually on Windows using [Windows Installer](https://docs.microsoft.com/en-us/windows/desktop/msi/windows-installer-portal), download [**`minikube-installer.exe`**](https://github.com/kubernetes/minikube/releases/latest/download/minikube-installer.exe) and execute the installer.

#### Install Minikube via direct download

To install Minikube manually on Windows, download [**`minikube-windows-amd64`**](https://github.com/kubernetes/minikube/releases/latest), rename it to **`minikube.exe`**, and add it to your path.

## Cleanup local state

If you have previously installed minikube, and run:

```shell
minikube start
```

And this command returns an error:

```shell
machine does not exist
```

You need to clear minikube's local state:

```shell
minikube delete
```

## What's next

+ [Running Kubernetes Locally via Minikube](https://kubernetes.io/docs/setup/learning-environment/minikube/)


