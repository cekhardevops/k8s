install docker

install kubectl

install eksctl

run aws configure

install docker
-------------
```
curl https://raw.githubusercontent.com/cekhardevops/k8s/refs/heads/main/install-docker.sh | sudo bash
```
install kubectl
---------------
```
curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.31.0/2024-09-12/bin/linux/amd64/kubectl

chmod +x ./kubectl

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH

echo 'export PATH=$HOME/bin:$PATH' >> ~/.bashrc

sudo mv kubectl /usr/local/bin/kubectl

kubectl version
```
install eksctl
----------------
```
ARCH=amd64
PLATFORM=$(uname -s)_$ARCH
curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"
tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz
sudo mv /tmp/eksctl /usr/local/bin
eksctl version
aws configure
```