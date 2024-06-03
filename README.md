# datascience-repo

Demo repo for SCaLE 2024. 

Link to SCaLE Session

[![IMAGE ALT TEXT HERE](https://i.ytimg.com/vi/TT3POS35dDw/sddefault.jpg)](https://www.youtube.com/watch?v=TT3POS35dDw)


https://i.ytimg.com/vi/TT3POS35dDw/sddefault.jpg

## Deployment

### Pre-reqs

An EKS Cluster with [Karpenter](https://karpenter.sh/), [Kuberay-operator](https://github.com/ray-project/kuberay/tree/master/helm-chart/kuberay-operator), [ACK-S3-Controller](https://aws-controllers-k8s.github.io/community/docs/user-docs/install/), [ACK-EKS-Controller](https://aws-controllers-k8s.github.io/community/docs/user-docs/install/), [Argo CD](https://argo-cd.readthedocs.io/en/stable/), [S3-MountPoint](https://docs.aws.amazon.com/eks/latest/userguide/s3-csi.html), [NVIDIA Device Plugin](https://github.com/NVIDIA/k8s-device-plugin/blob/v0.15.0/deployments/helm/nvidia-device-plugin/values.yaml) 

### Deploy the ArgoCD ApplicationSet

```
# Clone the repo
git clone https://github.com/askulkarni2/datascience-repo/
cd datascience-repo

# Login to argo cd
argocd login

# Create Application Set
argocd appset create git-generator-files.yaml
```
