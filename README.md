# Filebeat Operator

The Filebeat Operator is a Kubernetes Operator that manages Filebeat configurations on a Kubernetes cluster. It provides a Custom Resource Definition (CRD) that allows users to create and manage Filebeat configurations using Kubernetes resources.

## Features

The Filebeat Operator provides the following features:

- Creation of a Filebeat configuration CRD
- Dynamic creation of a Filebeat configuration file
- Adding the configuration to a ConfigMap
- Mounting the ConfigMap to a Filebeat DaemonSet
- Reloading the configuration of Filebeat in the DaemonSet

## Installation

To install the Filebeat Operator, follow these steps:

1. Clone the repository:

    ```
    git clone https://github.com/your-username/filebeat-operator.git
    ```

2. Build the Docker image:

    ```
    docker build -t filebeat-operator .
    ```

3. Push the Docker image to a container registry:

    ```
    docker push your-registry/filebeat-operator:latest
    ```

4. Modify the `deploy/operator.yaml` file to reference the correct image:

    ```
    spec:
        containers:
        - name: filebeat-operator
            image: your-registry/filebeat-operator:latest
    ```

