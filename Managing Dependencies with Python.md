# Managing Dependencies with Python

## Description

This documentation outlines best practices for managing dependencies in Python projects using package management tools such as pip and virtual environments. Managing dependencies efficiently ensures smooth development workflows, version control compatibility, and reproducible environments.

## Prerequisite Check

Before managing dependencies, ensure that Python is installed on the Unix system. Python can be downloaded and installed from the official Python website (https://www.python.org/downloads/).

## Virtual Environments

Virtual environments provide isolated Python environments for projects, preventing conflicts between dependencies across different projects. They allow for the installation of project-specific packages without affecting the global Python environment.

### Creating a Virtual Environment

To create a virtual environment, navigate to the project directory in the terminal and execute the following command:

```bash
python3 -m venv env
```

This command creates a virtual environment named 'env' in the project directory.

### Activating the Virtual Environment

Activate the virtual environment using the following command:

```bash
source env/bin/activate
```

This command activates the virtual environment, enabling the installation and management of dependencies within it.

### Deactivating the Virtual Environment

To deactivate the virtual environment and return to the global Python environment, execute the following command:

```bash
deactivate
```

This command exits the virtual environment and restores the global Python environment.

## Managing Dependencies with pip

pip is the default package manager for Python, used to install, upgrade, and manage Python packages and their dependencies.

### Installing Packages

Within the activated virtual environment, install packages using the following command:

```bash
pip install package_name
```

Replace 'package_name' with the name of the package to install. Versions can also be specified using the format 'package_name==version'.

### Listing Installed Packages

To view a list of installed packages and their versions, run:

```bash
pip list
```

This command displays all installed packages in the virtual environment along with their versions.

### Freezing Dependencies

Freeze the current state of installed packages into a requirements.txt file:

```bash
pip freeze > requirements.txt
```

This file contains a list of installed packages and their versions, facilitating environment replication.

### Installing Dependencies from requirements.txt

To install dependencies from a requirements.txt file, execute:

```bash
pip install -r requirements.txt
```

This command installs all packages listed in requirements.txt, ensuring environment consistency.

## Concluding Remarks

Managing dependencies in Python projects on Unix systems is crucial for maintaining project stability and reproducibility. By utilizing virtual environments and pip for dependency management, developers can ensure a clean and isolated environment for each project, simplifying development and collaboration processes.