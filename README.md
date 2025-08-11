# Local Kubernetes Deployment with Minikube

This project demonstrates how to deploy, manage, and expose a simple NGINX web server on a local Kubernetes cluster using Minikube. This serves as a foundational exercise for understanding Kubernetes concepts like Deployments and Services.

---
## ## Overview

The objective is to create a multi-pod NGINX deployment and make it accessible from the local machine. This is achieved by defining the application's state declaratively using YAML configuration files and managing it with `kubectl`.

**Key Tools Used:**
* **Kubernetes**
* **Minikube** (for local cluster creation)
* **Docker** (as the container runtime for Minikube)
* **kubectl** (for interacting with the cluster)

---
## ## How to Run This Project

### ### Prerequisites
* [Docker](https://www.docker.com/products/docker-desktop/) installed and running.
* [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed.
* [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) installed.

### ### Steps

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Start the Minikube Cluster**
    ```bash
    minikube start
    ```

3.  **Deploy the NGINX Application**
    Apply the deployment and service configurations to the cluster. The deployment will create the pods, and the service will expose them.
    ```bash
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
    ```

4.  **Access the Application**
    Minikube provides a simple command to get the URL and open it in your browser.
    ```bash
    minikube service my-nginx-service
    ```
    This will open the NGINX welcome page.

---
## ## Verification Commands

Here are some useful commands to check the status of your deployment.

* **Check all resources (pods, services, deployments):**
    ```bash
    kubectl get all
    ```

* **Scale the deployment to 3 replicas:**
    ```bash
    kubectl scale deployment my-nginx-deployment --replicas=3
    ```

* **View detailed information about a specific pod:**
    ```bash
    # First, get the pod name with `kubectl get pods`
    # Then, use the name in the command below
    kubectl describe pod <your-pod-name>
    ```

---
## ## Final Result

Here is a screenshot of the NGINX welcome page running successfully after being accessed through the Minikube service.


*Add your screenshot here by creating a folder named `screenshots`, adding your image to it, and referencing it like this: `![NGINX Welcome Page](screenshots/your-image-name.png)`*
