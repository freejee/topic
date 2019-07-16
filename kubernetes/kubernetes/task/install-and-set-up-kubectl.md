## Install and Set Up kubectl

+ [Before you begin](#before-you-begin)
+ [Install kubectl on Linux](#install-kubectl-on-linux)
    + [Install kubectl binary with curl on Linux](#install-kubectl-binary-with-curl-on-linux)
    + [Install using native package management](#install-using-native-package-management)
        + [Ubuntu, Debian or HypriotOS](#ubuntu-debian-or-hypriotos)
        + [CentOS, RHEL or Fedora](#centos-rhel-or-fedora)
    + [Install with snap](#install-with-snap)
+ [Install kubectl on macOS](#install-kubectl-on-macos)
    + [Install kubectl binary with curl on macOS](#install-kubectl-binary-with-curl-on-macos)
    + [Install with Homebrew on macOS](#install-with-homebrew-on-macos)
    + [Install with Macports on macOS](#install-with-macports-on-macos)
+ [Install kubectl on Windows](#install-kubectl-on-windows)
    + [Install kubectl binary with curl on Windows](#install-kubectl-binary-with-curl-on-windows)
    + [Install with Powershell from PSGallery](#install-with-powershell-from-psgallery)
    + [Install on Windows using Chocolatey or Scoop](#install-on-windows-using-chocolatey-or-scoop)
+ [Download as part of the Google Cloud SDK](#download-as-part-of-the-google-cloud-sdk)
+ [Verifying kubectl configuration](#verifying-kubectl-configuration)
+ [Optional kubectl configurations](#optional-kubectl-configurations)
    + [Enabling shell autocompletion](#enabling-shell-autocompletion)
        + [Bash on Linux](#bash-on-linux)
            + [Introduction](#introduction)
            + [Install bash-completion](#install-bash-completion)
            + [Enable kubectl autocompletion](#enable-kubectl-autocompletion)
        + [Bash on macOS](#bash-on-macos)
            + [Introduction](#introduction-1)
            + [Install bash-completion](#install-bash-completion-1)
            + [Enable kubectl autocompletion](#enable-kubectl-autocompletion-1)
        + [Zsh](#zsh)
+ [What's next](#whats-next)

----------------------------------------------------------------------------------------------------

The Kubernetes command-line tool, [kubectl](https://kubernetes.io/docs/user-guide/kubectl/), allows you to run commands against Kubernetes clusters.

You can use kubectl to deploy applications, inspect and manage cluster resources, and view logs.

For a complete list of kubectl operations, see [Overview of kubectl](https://kubernetes.io/docs/reference/kubectl/overview/).

## Before you begin

You must use a kubectl version that is within one minor version difference of your cluster.

For example, a v1.2 client should work with v1.1, v1.2, and v1.3 master.

Using the latest version of kubectl helps avoid unforeseen issues.

## Install kubectl on Linux

### Install kubectl binary with curl on Linux

1. Download the latest release with the command:
   ```shell
   curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
   ```

   To download a specific version, replace the **`$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)`** portion of the command with the specific version.

   For example, to download version v1.15.0 on Linux, type:
   ```shell
   curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.0/bin/linux/amd64/kubectl
   ```

2. Make the kubectl binary executable.
   ```shell
   chmod +x ./kubectl
   ```

3. Move the binary in to your PATH.
   ```shell
   sudo mv ./kubectl /usr/local/bin/kubectl
   ```

4. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

### Install using native package management

#### Ubuntu, Debian or HypriotOS

```shell
sudo apt-get update && sudo apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
```

#### CentOS, RHEL or Fedora

```shell
cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF
yum install -y kubectl
```

### Install with snap

If you are on Ubuntu or another Linux distribution that support [snap](https://snapcraft.io/docs/core/install) package manager, kubectl is available as a [snap](https://snapcraft.io/) application.

1. Switch to the snap user and run the installation command:
   ```shell
   sudo snap install kubectl --classic
   ```

2. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

## Install kubectl on macOS

### Install kubectl binary with curl on macOS

1. Download the latest release:
   ```shell
   curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/darwin/amd64/kubectl
   ```

   To download a specific version, replace the **`$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)`** portion of the command with the specific version.

   For example, to download version v1.15.0 on macOS, type:
   ```shell
   curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.0/bin/darwin/amd64/kubectl
   ```

2. Make the kubectl binary executable.
   ```shell
   chmod +x ./kubectl
   ```

3. Move the binary in to your PATH.
   ```shell
   sudo mv ./kubectl /usr/local/bin/kubectl
   ```

4. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

### Install with Homebrew on macOS

If you are on macOS and using [Homebrew](https://brew.sh/) package manager, you can install kubectl with Homebrew.

1. Run the installation command:
   ```shell
   brew install kubernetes-cli
   ```

2. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

### Install with Macports on macOS

If you are on macOS and using [Macports](https://macports.org/) package manager, you can install kubectl with Macports.

1. Run the installation command:
   ```shell
   sudo port selfupdate
   sudo port install kubectl
   ```
    
2. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

## Install kubectl on Windows

### Install kubectl binary with curl on Windows

1. Download the latest release v1.15.0 from [this link](https://storage.googleapis.com/kubernetes-release/release/v1.15.0/bin/windows/amd64/kubectl.exe).
   Or if you have **`curl`** installed, use this command:
   ```shell
   curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.15.0/bin/windows/amd64/kubectl.exe
   ```

   To find out the latest stable version (for example, for scripting), take a look at [https://storage.googleapis.com/kubernetes-release/release/stable.txt](https://storage.googleapis.com/kubernetes-release/release/stable.txt).

2. Add the binary in to your PATH.

3. Test to ensure the version of **`kubectl`** is the same as downloaded:
   ```shell
   kubectl version
   ```

> **`Note`**: [Docker for Windows](https://docs.docker.com/docker-for-windows/#kubernetes) adds its own version of **`kubectl`** to PATH.
  If you have installed Docker before, you may need to place your PATH entry before the one added by Docker installer or remove the Docker's **`kubectl`**.

### Install with Powershell from PSGallery

If you are on Windows and using [Powershell Gallery](https://www.powershellgallery.com/) package manager, you can install and update kubectl with Powershell.

1. Run the installation commands (making sure to specify a **`DownloadLocation`**):
   ```shell
   Install-Script -Name install-kubectl -Scope CurrentUser -Force
   install-kubectl.ps1 [-DownloadLocation <path>]
   ```

   > **`Note`**: If you do not specify a **`DownloadLocation`**, **`kubectl`** will be installed in the user's temp Directory.
    
   The installer creates **`$HOME/.kube`** and instructs it to create a config file

2. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

   > **`Note`**: Updating the installation is performed by rerunning the two commands listed in step 1.

### Install on Windows using Chocolatey or Scoop

To install kubectl on Windows you can use either [Chocolatey](https://chocolatey.org/) package manager or [Scoop](https://scoop.sh/) command-line installer.

1. choco
   ```shell
   choco install kubernetes-cli
   ```

   scoop
   ```shell
   scoop install kubectl
   ```

2. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

3. Navigate to your home directory:
   ```shell
   cd %USERPROFILE%
   ```

4. Create the **`.kube`** directory:
   ```shell
   mkdir .kube
   ```

5. Change to the **`.kube`** directory you just created:
   ```shell
   cd .kube
   ```

6. Configure kubectl to use a remote Kubernetes cluster:
   ```shell
   New-Item config -type file
   ```
    
   > **`Note`**: Edit the config file with a text editor of your choice, such as Notepad.

## Download as part of the Google Cloud SDK

You can install kubectl as part of the Google Cloud SDK.

1. Install the [Google Cloud SDK](https://cloud.google.com/sdk/).

2. Run the **`kubectl`** installation command:
   ```shell
   gcloud components install kubectl
   ```
    
3. Test to ensure the version you installed is up-to-date:
   ```shell
   kubectl version
   ```

## Verifying kubectl configuration 

In order for kubectl to find and access a Kubernetes cluster, it needs a [kubeconfig file](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/), which is created automatically when you create a cluster using **`kube-up.sh`** or successfully deploy a Minikube cluster.

By default, kubectl configuration is located at **`~/.kube/config`**.

Check that kubectl is properly configured by getting the cluster state:

```shell
kubectl cluster-info
```
If you see a URL response, kubectl is correctly configured to access your cluster.

If you see a message similar to the following, kubectl is not configured correctly or is not able to connect to a Kubernetes cluster.

```shell
The connection to the server <server-name:port> was refused - did you specify the right host or port?
```

For example, if you are intending to run a Kubernetes cluster on your laptop (locally), you will need a tool like Minikube to be installed first and then re-run the commands stated above.

If kubectl cluster-info returns the url response but you can't access your cluster, to check whether it is configured properly, use:

```shell
kubectl cluster-info dump
```

## Optional kubectl configurations

### Enabling shell autocompletion

kubectl provides autocompletion support for Bash and Zsh, which can save you a lot of typing.

Below are the procedures to set up autocompletion for Bash (including the difference between Linux and macOS) and Zsh.

#### Bash on Linux

##### Introduction

The kubectl completion script for Bash can be generated with the command **`kubectl completion bash`**.

Sourcing the completion script in your shell enables kubectl autocompletion.

However, the completion script depends on [**`bash-completion`**](https://github.com/scop/bash-completion), which means that you have to install this software first (you can test if you have bash-completion already installed by running **`type _init_completion`**).

##### Install bash-completion

bash-completion is provided by many package managers (see [here](https://github.com/scop/bash-completion#installation)).

You can install it with **`apt-get install bash-completion`** or **`yum install bash-completion`**, etc.

The above commands create **`/usr/share/bash-completion/bash_completion`**, which is the main script of bash-completion.

Depending on your package manager, you have to manually source this file in your **`~/.bashrc`** file.

To find out, reload your shell and run **`type _init_completion`**.

If the command succeeds, you're already set, otherwise add the following to your **`~/.bashrc`** file:

```shell
source /usr/share/bash-completion/bash_completion
```

Reload your shell and verify that bash-completion is correctly installed by typing **`type _init_completion`**.

##### Enable kubectl autocompletion

You now need to ensure that the kubectl completion script gets sourced in all your shell sessions.

There are two ways in which you can do this:

+ Source the completion script in your **`~/.bashrc`** file:
  ```shell
  echo 'source <(kubectl completion bash)' >>~/.bashrc
  ```

+ Add the completion script to the **`/etc/bash_completion.d`** directory:
  ```shell
  kubectl completion bash >/etc/bash_completion.d/kubectl
  ```

> **`Note`**: bash-completion sources all completion scripts in **`/etc/bash_completion.d`**.

Both approaches are equivalent.

After reloading your shell, kubectl autocompletion should be working.

#### Bash on macOS

##### Introduction

The kubectl completion script for Bash can be generated with **`kubectl completion bash`**.

Sourcing this script in your shell enables kubectl completion.

However, the kubectl completion script depends on [**`bash-completion`**](https://github.com/scop/bash-completion) which you thus have to previously install.

> **`Warning`**: there are two versions of bash-completion, v1 and v2.
  V1 is for Bash 3.2 (which is the default on macOS), and v2 is for Bash 4.1+.
  The kubectl completion script **`doesn't work`** correctly with bash-completion v1 and Bash 3.2.
  It requires **`bash-completion v2`** and **`Bash 4.1+`**.
  Thus, to be able to correctly use kubectl completion on macOS, you have to install and use Bash 4.1+ ([*instructions*](https://itnext.io/upgrading-bash-on-macos-7138bd1066ba)).
  The following instructions assume that you use Bash 4.1+ (that is, any Bash version of 4.1 or newer).

##### Install bash-completion

> **`Note`**: As mentioned, these instructions assume you use Bash 4.1+, which means you will install bash-completion v2 (in contrast to Bash 3.2 and bash-completion v1, in which case kubectl completion won't work).

You can test if you have bash-completion v2 already installed with **`type _init_completion`**.

If not, you can install it with Homebrew:
```shell
brew install bash-completion@2
```

As stated in the output of this command, add the following to your **`~/.bashrc`** file:
```shell
export BASH_COMPLETION_COMPAT_DIR="/usr/local/etc/bash_completion.d"
[[ -r "/usr/local/etc/profile.d/bash_completion.sh" ]] && . "/usr/local/etc/profile.d/bash_completion.sh"
```

Reload your shell and verify that bash-completion v2 is correctly installed with **`type _init_completion`**.

##### Enable kubectl autocompletion

You now have to ensure that the kubectl completion script gets sourced in all your shell sessions.

There are multiple ways to achieve this:

+ Source the completion script in your **`~/.bashrc`** file:
  ```shell
  echo 'source <(kubectl completion bash)' >>~/.bashrc
   ```

+ Add the completion script to the **`/usr/local/etc/bash_completion.d`** directory:
  ```shell
  kubectl completion bash >/usr/local/etc/bash_completion.d/kubectl
  ```

+ If you installed kubectl with Homebrew (as explained [above](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-with-homebrew-on-macos)), then the kubectl completion script should already be in **`/usr/local/etc/bash_completion.d/kubectl`**.
  In that case, you don't need to do anything.

> **`Note`**: the Homebrew installation of bash-completion v2 sources all the files in the **`BASH_COMPLETION_COMPAT_DIR`** directory, that's why the latter two methods work.

In any case, after reloading your shell, kubectl completion should be working.

#### Zsh

The kubectl completion script for Zsh can be generated with the command **`kubectl completion zsh`**.

Sourcing the completion script in your shell enables kubectl autocompletion.

To do so in all your shell sessions, add the following to your **`~/.zshrc`** file:

```shell
source <(kubectl completion zsh)
```

After reloading your shell, kubectl autocompletion should be working.

If you get an error like **`complete:13: command not found: compdef`**, then add the following to the beginning of your **`~/.zshrc`** file:

```shell
autoload -Uz compinit
compinit
```

## What's next

+ [Install Minikube](https://kubernetes.io/docs/tasks/tools/install-minikube/).
+ See the [getting started guides](https://kubernetes.io/docs/setup/) for more about creating clusters.
+ [Learn how to launch and expose your application](https://kubernetes.io/docs/tasks/access-application-cluster/service-access-application-cluster/).
+ If you need access to a cluster you didn't create, see the [Sharing Cluster Access document](https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/).
+ Read the [kubectl reference docs](https://kubernetes.io/docs/reference/kubectl/kubectl/).


