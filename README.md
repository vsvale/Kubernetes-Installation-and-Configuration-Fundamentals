# Kubernetes-Installation-and-Configuration-Fundamentals
- `sudo apt-get install -y containerd`
- 
## Install kubernetes
- `sudo apt install curl git`
- `curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64`
- `chmod +x ./minikube`
- `sudo mv ./minikube /usr/local/bin/`
- `sudo apt install -y conntrack`
- `sudo apt install -yqq daemonize dbus-user-session fontconfig`
- `minikube -p minikube start --container-runtime=containerd --cni=cilium --extra-config=kubelet.runtime-request-timeout=10m0s`
- `minikube kubectl -- get po -A`
- `sudo apt-get update`
- `sudo apt-get install -y ca-certificates curl`
- `sudo apt-get install -y apt-transport-https`
- `sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg <https://packages.cloud.google.com/apt/doc/apt-key.gpg>`
- `echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] <https://apt.kubernetes.io/> kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list`
- `sudo apt-get update`
- `sudo apt-get install -y kubectl kubeadm kubelet`