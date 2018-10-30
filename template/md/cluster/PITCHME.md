## Kubernetes Cluster Creation

---
@title[Cluster Creation - EKS]

@snap[north span-100]
@size[1.5em](Cluster Creation using EKS)
@snapend

@snap[center span-100]
We're going to use a managed Kubernetes service, specifically [EKS](https://aws.amazon.com/eks/):
<br><br>
@snapend

```bash
eksctl create cluster -n richardscluster -N 2 -t t2.medium -r us-west-2
```


