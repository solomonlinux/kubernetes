# 第一章、kubernetes集群部署

## 第一节、部署

### 一、规划



··· bash
\# cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://mirrors.aliyun.com/kubernetes/yum/repos/kubernetes-el7-x86_64/
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://mirrors.aliyun.com/kubernetes/yum/doc/yum-key.gpg https://mirrors.aliyun.com/kubernetes/yum/doc/rpm-package-key.gpg
EOF
\# setenforce 0
\# yum install -y kubelet kubeadm kubectl
\# systemctl enable kubelet && systemctl start kubelet
```