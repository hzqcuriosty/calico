
**Calico是一个纯三层的数据中心网络方案，Calico支持广泛的平台，包括Kubernetes、OpenStack等。**


**下载Calico.yaml**

    git clone https://github.com/hzqcuriosty/calico.git

**下载后需要修改里面定义Pod网络（CALICO_IPV4POOL_CIDR），与前面kubeadm init指定的网络保持一样
：**

    - name: CALICO_IPV4POOL_CIDR
    value: "10.244.0.0/16"
    
**修改完后应用清单**

    $ kubectl apply -f calico.yaml
    $ kubectl get pods -n kube-system
