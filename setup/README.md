# Lab 0: Workshop Setup


Before you begin learning, you will need to install the required CLIs to create and manage your Kubernetes clusters in IBM Cloud Container Service, and to deploy containerized apps to your cluster.

This lab includes the information for installing these CLIs and plug-ins:

``` txt
IBM Cloud CLI version 0.5.0 or later
IBM Cloud Container Service plug-in
Kubernetes CLI version 1.5.6 or later
Optional: IBM Cloud Container Registry plug-in
Optional: Docker version 1.9 or later
```

If you have already installed these CLIs and plug-ins, you can skip this lab and proceed to [Exercise 1 - Setting up a Kubernetes cluster](exercise-1/README.md).


## Install the IBM Cloud CLI

As a prerequisite for the IBM Cloud Container Service plug-in, install the IBM Cloud command line interface, located at https://clis.ng.bluemix.net/ui/home.html. Once installed, you can access IBM Cloud from your command line with the prefix `bx`.

Log in to the IBM Cloud CLI with `bx login`. Enter your IBM Cloud credentials when prompted.
    * Note: If you have a federated ID, use `bx login --sso` to log in to the IBM Cloud CLI. Enter your user name and use the provided URL in your CLI output to retrieve your one-time passcode. You know you have a federated ID when the login fails without the `--sso` and succeeds with the `--sso` option.

## Install the IBM Cloud Containers Service Plug-in

To create Kubernetes clusters and manage worker nodes, install the IBM Cloud Container Service plug-in with `bx plugin install container-service -r Bluemix`. The prefix for running commands by using the IBM Cloud Container Service plug-in is `bx cs`.

To verify that the plug-in is installed properly, run `bx plugin list`. The IBM Cloud Container Service plug-in is displayed in the results as `container-service`.

Once the IBM Cloud CLI and the Containers Service plug-in are installed, you can move on to the next phase of the lab.

## Install the Kubernetes CLI

To view a local version of the Kubernetes dashboard and to deploy apps into your clusters, you will need to install the Kubernetes CLI. The following links will install the CLI. Simply click the link corresponding to your operating system:

OS X: https://storage.googleapis.com/kubernetes-release/release/v1.5.6/bin/darwin/amd64/kubectl
Linux: https://storage.googleapis.com/kubernetes-release/release/v1.5.6/bin/linux/amd64/kubectl
Windows: https://storage.googleapis.com/kubernetes-release/release/v1.5.6/bin/windows/amd64/kubectl.exe

If you are using Windows, install the Kubernetes CLI in the same directory as the IBM Cloud CLI. This setup saves you some filepath changes when you run commands later.

If you are using OSX or Linux, complete the following steps.

Move the executable file to the `/usr/local/bin` directory with `mv /<path_to_file>/kubectl/usr/local/bin/kubectl`.

Make sure that `/usr/local/bin` is listed in your PATH system variable.

```txt
echo $PATH
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```
Convert the binary file to an executable with `chmod +x /usr/local/bin/kubectl`.

## Optional: Install the IBM Cloud Container Registry plug-in and Docker

To manage a private image repository, install the IBM Cloud Container Registry plug-in. Use this plug-in to set up your own namespace in a multi-tenant, highly available, and scalable private image registry that is hosted by IBM, and to store and share Docker images with other users. Docker images are required to deploy containers into a cluster. The prefix for running registry commands is `bx cr`.

To install the plug-in, run `bx plugin install container-registry -r Bluemix`.

To verify that the plug-in is installed properly, run `bx plugin list`. The plug-in is displayed in the results as `container-registry`.

To build images locally and push them to your registry namespace, install [Docker](https://www.docker.com/community-edition#/download). If you are using Windows 8 or earlier, you can install the [Docker Toolbox](https://www.docker.com/products/docker-toolbox) instead. The Docker CLI is used to build apps into images. The prefix for running commands by using the Docker CLI is `docker`.
