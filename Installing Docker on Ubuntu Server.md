# Installing Docker on Ubuntu Server

## Description

This documentation provides step-by-step instructions for installing Docker on an Ubuntu Server. Docker is a widely-used platform for containerization, enabling developers to package applications and their dependencies into lightweight containers for efficient deployment across different environments.

## Prerequisite Check

Ensure access to an Ubuntu Server instance with administrative privileges. Additionally, verify that the server meets the minimum system requirements for running Docker and has a stable internet connection for downloading necessary packages.

## Update Package Lists

Before installing Docker, it's recommended to update the package lists for the latest versions of available packages. Open a terminal window on the Ubuntu Server and execute the following command:

```bash
sudo apt update
```

## Install Docker Dependencies

Docker requires a few dependencies to be installed on Ubuntu Server. Run the following command to install these dependencies:

```bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
```

## Add Docker’s Official GPG Key

To ensure the integrity of Docker packages, add Docker’s official GPG key to the system. Run the following command to download and add the key:

```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

## Add Docker Repository

Next, add the Docker repository to the system's list of package sources. Use the following command to add the Docker repository for Ubuntu:

```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

## Update Package Lists Again

After adding the Docker repository, update the package lists again to include Docker packages:

```bash
sudo apt update
```

## Install Docker Engine

Now, install Docker Engine by running the following command:

```bash
sudo apt install -y docker-ce
```

Docker Engine is the core component for running and managing Docker containers.

## Verify Docker Installation

Once the installation is complete, verify that Docker has been installed correctly by running the following command:

```bash
sudo docker --version
```

This command should display the installed version of Docker, indicating a successful installation.

## Manage Docker as a Non-Root User (Optional)

By default, Docker commands require root privileges. To use Docker as a non-root user, add the user to the `docker` group. This allows running Docker commands without using `sudo`. Use the following command to add the user to the `docker` group:

```bash
sudo usermod -aG docker $USER
```

Remember to log out and log back in for the changes to take effect.

## Starting Docker Service

After installation, Docker should start automatically. However, if it's not running, start the Docker service using the following command:

```bash
sudo systemctl start docker
```

You can also enable Docker to start on boot with:

```bash
sudo systemctl enable docker
```

## Conclusion

Docker is now successfully installed on the Ubuntu Server. Begin using Docker to create, deploy, and manage containers for applications and services. Refer to Docker's documentation for further guidance on working with containers and images.