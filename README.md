# workstation-setup
# docker and k3s setup
```sh

sudo apt install -y curl wget git vim 
   43  df -h
   44  df -k
   45  curl -s "https://get.sdkman.io" | bash
   46  curl
   47  wget
   48  docker
   49  mkdir -p /home/docker-data
   50  sudo mkdir -p /home/docker-data
   51  sudo chown -R root:root /home/docker-data
   52  ls -altr /home/docker-data/
   53  sudo chmod 711 /home/docker-data/
   54  ls -altr /home/docker-data/
   55  ls -altr /home/docker-data
   56  sudo ls -altr /home/docker-data
   57  sudo chmod u=rwx, g=x, o=x /home/docker-data/
   58  chmod --help
   59  sudo chmod u=rwx,g=x,o=x /home/docker-data/
   60  sudo ls -altr /home/docker-data
   61  sudo apt update
   62  sudo apt install -y docker.io
   63  sudo systemctl enable docker
   64  sudo systemctl stop docker
   65  ls /etc/docker/
   66  sudo vi /etc/docker/daemon.json
   67  cat /etc/docker/daemon.json 
   68  ls /home/docker-data/
   69  sudo systemctl start docker
   70  docker info |grep "Docker Root Dir"
   71  sudo systemctl status docker
   72  sudo usermod -aG docker $USER
   73  exit
   74  newgrp docker
   75  sudo systemctl stop docker
   76  sudo systemctl start docker
   77  docker info
   78  docker info| grep "Docker Root Dir"
   79  ls -altr /home/docker-data/
   80  sudo ls -altr /home/docker-data/
   81  newgrp docker
   82  pwd
   83  sudo mkdir -p /home/k8s-pv
   84  sudo mkdir -p /home/k3s-data
   85  sudoc chown -R root:root /home/k8s-pv /home/k3s-data
   86  sudo chown -R root:root /home/k8s-pv /home/k3s-data
   87  sudo chmod u=rwx,g=rx,o=rx /home/k8s-pv
   88  sudo ls -altr /home/k8s-pv
   89  sudo chmod 755 /home/k8s-pv
   90  sudo ls -altr /home/k8s-pv
   91  curl -sfL https://get.k3s.io | sh -s - --data-dir /home/k3s-data
   92  sudo kubectl get nodes
   93  mkdir -p ~/.kube
   94  sudo cp /etc/rancher/k3s/k3s.yaml ~/.kube/config
   95  sudo chown $USER:$USER ~/.kube/config 
   96  kubectl get nodes
   97  ls -altr ~/.kube/config 
   98  cat ~/.kube/config
   99  ls -altr ~/.kube/
  100  echo $KUBECONFIG
```

