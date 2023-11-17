![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) ![Helm](https://img.shields.io/badge/Helm-0F1689?style=for-the-badge&logo=Helm&labelColor=0F1689) ![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white) ![Github Pages](https://img.shields.io/badge/github%20pages-121013?style=for-the-badge&logo=github&logoColor=white) ![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
# vContainer Storage Interface
![dev-staging-env](https://badgen.net/badge/DEV-STAGING/environment/blue?icon=github)
<hr>

# 1. Installation
## 1.1. Prerequisites
- Helm 3.0+
- `KUBECONFIG` environment variable pointing to the `.kubeconfig` file with access to your Kubernetes cluster.

## 1.2. Install `vcontainer-storage-interface` on Kubernetes
- Following the below steps to install `vcontainer-storage-interface` on your Kubernetes cluster:
  - **Step 1**: Add the `vcontainer-helm-infra` Helm repository:
    ```
    helm repo add vcontainer-helm-infra https://vngcloud.github.io/vcontainer-helm-infra
    helm repo update
    ```

  - **Step 2**: Install `vcontainer-storage-interface`:
    ```
    helm install vcontainer-storage-interface vcontainer-helm-infra/vcontainer-storage-interface --replace \
      --namespace kube-system \
      --set vcontainerConfig.clientID=<PUT_YOUR_CLIENT_ID> \
      --set vcontainerConfig.clientSecret=<PUT_YOUR_CLIENT_SECRET>
    ```

