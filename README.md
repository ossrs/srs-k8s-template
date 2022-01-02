# srs-k8s-template

[![](https://github.com/ossrs/srs-k8s-template/actions/workflows/kubernetes.yml/badge.svg)](https://github.com/ossrs/srs-k8s-template/actions/workflows/kubernetes.yml)

Template repository for deploying SRS to any K8s service by kubectl.

## Usage

**Step 1:** Create K8s cluster, update the kubeconfig, check by `kubectl cluster-info`:

* [TKE(Tencent Kubernetes Engine)](https://github.com/ossrs/srs-tke-template#usage)
* [ACK(Alibaba Cloud Container Service for Kubernetes)](https://github.com/ossrs/srs-ack-template#usage)
* [EKS(Amazon Elastic Kubernetes Service)](https://github.com/ossrs/srs-eks-template#usage)
* [AKS(Azure Kubernetes Service)](https://github.com/ossrs/srs-aks-template#usage)

**Step 2:** Click the <kbd>Use this template</kbd> to create your repository, then set the [secrets](https://github.com/ossrs/srs-k8s-template/settings/secrets/actions):

* `KUBECONFIG` is the config of K8s, for example, the content of `cat $HOME/.kube/config`.

**Step 3:** Re-run [Actions](https://github.com/ossrs/srs-k8s-template/actions/workflows/kubernetes.yml) to deploy to your K8s, for example, if your external IP is `81.70.125.89`:

* Website is http://81.70.125.89:8080
* Publish RTMP to rtmp://81.70.125.89/live/livestream
* Play RTMP from rtmp://81.70.125.89/live/livestream
* Play HTTP-FLV from http://81.70.125.89:8080/live/livestream.flv
* Play HLS from http://81.70.125.89:8080/live/livestream.m3u8

Try to motify the [srs.yaml](srs.yaml), then push to your repository, your K8s will be updated automatically.

