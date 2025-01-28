# Argo CD Continuous Deployment Setup

This guide explains how to set up Argo CD for continuous deployment in Kubernetes.

## Steps

### 1. **Download Argo CD Operator**

  curl -sL https://github.com/operator-framework/operator-lifecycle-manager/releases/download/v0.31.0/install.sh | bash -s v0.31.0

- **Why**: Installs the Operator Lifecycle Manager (OLM) needed to manage Kubernetes operators like Argo CD.

### 2. **Install Argo CD Operator**

```bash
kubectl create -f https://operatorhub.io/install/argocd-operator.yaml
```
- **Why**: Deploys the Argo CD operator in the Kubernetes cluster.

- Refer the Article for downloading Argocd - https://operatorhub.io/operator/argocd-operator

### 3. **Verify Installation**

```bash
kubectl get csv -n operators
```
- **Why**: Checks that the Argo CD operator is installed correctly.

### 4. **Apply Argo CD Configuration**

```bash
kubectl apply -f argo-basic.yaml
```
- **Why**: Deploys the Argo CD application using the provided YAML configuration.

### 5. **Check Running Pods**

```bash
kubectl get pods
```
- **Why**: Verifies that Argo CD pods are running as expected.

### 6. **Check Services**

```bash
kubectl get svc
```
- **Why**: Lists the services in your cluster, including Argo CD.

### 7. **Access Argo CD Server**

```bash
minikube service argocd-server -n operators
```
- **Why**: Opens a tunnel to the Argo CD server so you can access the UI locally.

### 8. **Get Service URL**

```bash
minikube service list
```
- **Why**: Retrieves the URL to access the Argo CD server UI.

### 9. **Get Argo CD Password**

```bash
kubectl get secret
```
- **Why**: Fetches the Kubernetes secrets, including the Argo CD password.

### 10. **Edit Secret for Password**

```bash
kubectl edit secret example-argocd-cluster
```
- **Why**: Edits the secret to retrieve the Argo CD password.

### 11. **Login to Argo CD UI**

- Use the password to log in to the Argo CD UI.

### 12. **Create Argo CD Project**

- Create a new project in the Argo CD UI and add the necessary application data.

---

This completes the setup of Argo CD for continuous deployment on Kubernetes.

## Outputs:

<img width="950" alt="Succefully Deployed on argocd" src="https://github.com/user-attachments/assets/c13d9745-d305-49bb-a9f4-a36c8765dd1d" />

