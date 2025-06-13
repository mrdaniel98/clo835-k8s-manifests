# clo835-k8s-manifests
# Kubernetes Deployment: Flask App with MySQL

This project shows how to deploy a simple Flask app and a MySQL database using Kubernetes. It includes environment variables, secrets, persistent volumes, and RBAC security.

---

## 🔧 Tools Used
- Kubernetes (YAML files)
- Flask (the app)
- MySQL (the database)
- ConfigMap and Secrets
- Persistent Volume (PVC)
- RBAC (ServiceAccount, Role, RoleBinding)

---

## Files Explained

| File Name | What It Does |
|-----------|----------------|
| flask-deployment.yaml | Deploys the Flask app |
| flask-service.yaml | Exposes the Flask app in the cluster |
| mysql-deployment.yaml | Deploys the MySQL database |
| mysql-service.yaml | Lets other services reach MySQL |
| mysql-secret.yaml | Stores MySQL username and password |
| mysql-pvc.yaml | Creates storage volume for MySQL |
| configmap.yaml | Stores config variables |
| aws-secret.yaml | (Optional) Adds AWS access if needed |
| role.yaml, rolebinding.yaml, serviceaccount.yaml | Adds Kubernetes access security |

---

##  How to Use It

```bash
# 1. Clone this project
git clone https://github.com/mrdaniel98/clo835-k8s-manifests.git
cd clo835-k8s-manifests

# 2. Apply all files to Kubernetes
kubectl apply -f manifests/



What I Learned
How to deploy multiple apps inside Kubernetes

Using secrets to protect passwords

Using persistent volumes to save data

Making sure each part has correct access with RBAC
