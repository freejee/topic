# Installing on Kubernetes

Instructions for installing the Istio control plane on Kubernetes and adding virtual machines into the mesh.

> Istio 1.2 has been tested with these Kubernetes releases: 1.12, 1.13, 1.14.

Visit our [getting started guide](https://istio.io/docs/setup/kubernetes/getting-started/) to learn how to evaluate and try Istio's basic features quickly.

Istio offers [multiple installation flows](https://istio.io/docs/setup/kubernetes/getting-started/) depending on your platform and whether or not you intend to use Istio in production.

At a high level, the basic flow is the same regardless of platform:

1. [Review the pod requirements](https://istio.io/docs/setup/kubernetes/additional-setup/requirements/)

2. [Prepare your platform for Istio](https://istio.io/docs/setup/kubernetes/platform-setup/)

3. [Download the Istio release](https://istio.io/docs/setup/kubernetes/#downloading-the-release)

4. [Install Istio on your platform](https://istio.io/docs/setup/kubernetes/install)

## Installing Istio

Choose one of the following installation options, depending on your intended use:

+ [Demo installation](https://istio.io/docs/setup/kubernetes/install/kubernetes/):
  This option is ideal if you're new to Istio and just want to try it out.
  It allows you to experiment with many Istio features with modest resource requirements.

+ [Custom installation with Helm](https://istio.io/docs/setup/kubernetes/install/helm/):
  This option is ideal to install Istio for production use or for performance evaluation.

+ [Supported platform installation](https://istio.io/docs/setup/kubernetes/install/platform/):
  This option is ideal if your platform provides native support for Istio-enabled clusters with a [configuration profile](https://istio.io/docs/setup/kubernetes/additional-setup/config-profiles/) corresponding to your intended use.

After choosing an option and installing Istio on your cluster, you can deploy your own applications or experiment with some of our [tasks](https://istio.io/docs/tasks/) and [examples](https://istio.io/docs/examples/).

> If you're running your own applications, make sure to check the [requirements for pods and services](https://istio.io/docs/setup/kubernetes/additional-setup/requirements/).

When you're ready to consider more advanced Istio use cases, check out the following resources:

+ To install using Istio's Container Network Interface (CNI) plugin, visit our [CNI guide](https://istio.io/docs/setup/kubernetes/additional-setup/cni/).

+ To perform a multicluster setup, visit our [multicluster installation documents](https://istio.io/docs/setup/kubernetes/install/multicluster/).

+ To expand your existing mesh with additional containers or VMs not running on your mesh's Kubernetes cluster, follow our [mesh expansion guide](https://istio.io/docs/setup/kubernetes/additional-setup/mesh-expansion/).

+ To add services requires a detailed understanding of sidecar injection.
  Visit our [sidecar injection guide](https://istio.io/docs/setup/kubernetes/additional-setup/sidecar-injection/) to learn more.

## Downloading the release

Istio is installed in its own **`istio-system`** namespace and can manage services from all other namespaces.

1. Go to the [Istio release](https://github.com/istio/istio/releases) page to download the installation file corresponding to your OS.
   On a macOS or Linux system, you can run the following command to download and extract the latest release automatically:
   ```
   $ curl -L https://git.io/getLatestIstio | ISTIO_VERSION=1.2.2 sh -
   ```

2. Move to the Istio package directory.
   For example, if the package is **`istio-1.2.2`**:
   ```
   $ cd istio-1.2.2
   ```
   The installation directory contains:
   + Installation YAML files for Kubernetes in **`install/kubernetes`**
   + Sample applications in **`samples/`**
   + The **`istioctl`** client binary in the **`bin/`** directory.
     **`istioctl`** is used when manually injecting Envoy as a sidecar proxy.

3. Add the **`istioctl`** client to your **`PATH`** environment variable, on a macOS or Linux system:
   ```
   $ export PATH=$PWD/bin:$PATH
   ```

4. You can enable the [auto-completion option](https://istio.io/docs/ops/setup/istioctl) when working with a bash or ZSH console.


