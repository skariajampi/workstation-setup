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
---

# other setup commands

```sh

    1  sudo apt update
    8  sudo apt upgrade -y
    9  sudo dpkg --configure -a
   12  sudo apt upgrade -y
   13  sudo apt autoremove -y
   14  sudo ubuntu-drivers autoinstall
   18  sudo ubuntu-drivers -h
   19  sudo apt install ubuntu-drivers-common
   20  sudo ubuntu-drivers autoinstall
   21  ubuntu-drivers devices
   22  apt search nvidia-driver-390
   23  nvidia-smi
   24  df -h
   25  source "$HOME/.sdkman/bin/sdkman-init.sh"
   26  sdk version
   27  sdk list java
   28  sdk install java 11.0.30-amzn
   29  java -version
   30  sdk list java
   31  sdk install java 17.0.18-amzn
   32  sdk list java
   33  sdk install java 21.0.10-amzn
   34  java -version
   35  java
   36  systemd analyze
   37  systemd-analyze
   38  systemd-analyze blame
   39  sudo apt update
   40  sudo apt updgrade -y
   41  sudo apt upgrade -y
   42  sudo apt install -y curl wget git vim 
   43  sudo mkdir -p /home/docker-data
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
   61  sudo apt install -y docker.io
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
  101  history
  102  kubectl get nodes
  103  export KUBECONFIG=~/.kube/config
  104  kubectl get nodes
  105  echo 'export KUBECONFIG=~/.kube/config' >> ~/.bashrc 
  106  source ~/.bashrc 
  107  kubectl get nodes
  108  kubectl -n kube-system edit configmap local-path-config 
  120  kubectl -n kube-system delete pod -l app=local-path-provisioner
  121  kubectl -n kube-system get pods
  122  ls -altr /home/k3s-data/
  123  ls -altr /home/k3s-data/data/
  124  kubectl get pvc
  125  ls /home/k8s-pv/
  126  vi test-pvc.yaml
  127  kubectl apply  -f test-pvc.yaml 
  128  kubectl get pvc
  129  ls -altr /home/k8s-pv/
  130  ls -altr /home/k3s-data/
  131  ls -altr /home/k3s-data/server/
  132  sudo ls -altr /home/k3s-data/server/
  133  sudo ls -altr /home/k3s-data/data/
  134  sudo ls -altr /home/k3s-data/
  135  sudo ls -altr /home/k3s-data/agent/
  136  sudo ls -altr /home/k8s-pv/
  137  kubectl get pvc
  138  vi test-pod.yaml
  139  kubectl apply -f test-pod.yaml 
  140  kubectl get pods
  141  kubectl exec -it pvc-test-pod -- sh
  142  kubectl delete pod pvc-test-pod 
  143  kubectl delete pvc test-pvc 
  144  kubectl get pvc
  145  kubectl apply -f test-pvc.yaml 
  146  kubectl get pvc
  147  kubectl apply -f test-pod.yaml 
  148  kubectl get pods
  149  kubectl get pvc
  150  kubectl delete pod pvc-test-pod 
  151  sudo ls -altr /home/k8s-pv/
  152  kubectl apply -f test-pvc.yaml 
  153  sudo ls -altr /home/k8s-pv/
  154  kubectl apply -f test-pod.yaml 
  155  sudo ls -altr /home/k8s-pv/
  156  cd /home/k8s-pv/
  157  sudo cd /home/k8s-pv/
  158  kubectl delete pod pvc-test-pod 
  159  kubectl delete pvc test-pvc 
  160  sudo ls -altr /home/k8s-pv/
  161  ls -altr /home/k8s-pv
  162  pwd
  163  ls -altr /home/k8s-pv
  164  ls -altr /home/k3s-data/
  165  ls -altr /home/k3s-data/data/
  166  pwd
  167  nvidia-sim
  168  sudo nvidia-sim
  169  sudo nvidia-sim-uc
  170  sudo nvidia-smi
  171  pwd
  172  sudo swapoff -a
  173  kubectl get pods -n kube-system
  174  sudo cat /var/lib/rancher/k3s/server/node-token
  175  ls -altr /home/k3s-data/server/
  176  sudo ls -altr /home/k3s-data/server/
  177  sudo cat /home/k3s-data/server/node-token
  178  ip addr show | grep -E "inet " | grep -v 127.0.0.1 | awk '{print $2}' | cut -d/ -f1
  179  kubectl get pods -A
  180  ip a
  181  # Get internal IP (will be used by laptop)
  182  ip addr show | grep -E "inet " | grep -v 127.0.0.1 | awk '{print $2}' | cut -d/ -f1
  183  # Example: 192.168.1.100
  184  sudo systemctl status k3s-agent
  185  kubectl get nodes
  186  sudo systemctl status k3s
  187  ps aux|grep k3s
  188  kubectl get nodes
  189  kubectl describe node skaria-precision-7510
  190  kubectl run test-on-worker --image=nginx --restart=Never --overrides='{"spec":{"nodeName":"skaria-precision-7510"}}'
  191  kubectl get pod test-on-worker -o wide
  192  kubectl delete  pod test-on-worker -o wide
  193  kubectl delete  pod test-on-worker
  194  kubectl get pods -n kube-system | grep traefik
  195  kubectl get svc -n kube-system | grep traefik
  196  kubectl apply -f https://raw.githubusercontent.com/longhorn/longhorn/v1.6.0/deploy/longhorn.yaml
  197  kubectl get pods -n longhorn-system -o wide -w
  198  kubectl logs -n longhorn-system longhorn-manager-gpfxd --tail=50
  199  sudo apt update
  200  sudo apt install -y open-iscsi
  201  sudo systemctl enable --now iscsid
  202  iscsiadm --version
  203  sudo systemctl status iscsid
  204  sudo modprobe iscsi_tcp
  205  echo "iscsi_tcp" | sudo tee -a /etc/modules
  206  kubectl delete pods -n longhorn-system -l app=longhorn-manager
  207  kubectl get pods -n longhorn-system -w
  208  kubectl get pods -n longhorn-system
  209  kubectl delete pods -n longhorn-system -l app=longhorn-manager
  210  kubectl get pods -n longhorn-system
  211  kubectl get pods -n longhorn-system -w
  212  kubectl get pods -n longhorn-system
  213  kubectl patch storageclass local-path -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"false"}}}'
  214  kubectl patch storageclass longhorn -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
  215  kubectl get storageclass
  216  kubectl apply -f longhorn-test-pvc.yaml 
  217  kubectl get pvc
  218  kubectl apply -f longhorn-test-pod.yaml 
  219  kubectl get pods
  220  kubectl delete pod test-longhorn-pod 
  221  kubectl delete pvc test-longhorn-pvc 
  222  kubectl get pvc
  223  kubectl get pods -n kube-system
  174  sudo cat /var/lib/rancher/k3s/server/node-token
  175  ls -altr /home/k3s-data/server/
  176  sudo ls -altr /home/k3s-data/server/
  177  sudo cat /home/k3s-data/server/node-token
  178  ip addr show | grep -E "inet " | grep -v 127.0.0.1 | awk '{print $2}' | cut -d/ -f1
  179  cat /home/k3s-data/server/node-token
  180  sudo cat /home/k3s-data/server/node-token
  181  kubectl get nodes
  182  sudo cat /var/lib/rancher/k3s/server/node-token
  175  kubectl get pods -A
  180  ip a
  181  # Get internal IP (will be used by laptop)
  182  ip addr show | grep -E "inet " | grep -v 127.0.0.1 | awk '{print $2}' | cut -d/ -f1
  183  # Example: 192.168.1.100
  184  sudo systemctl status k3s-agent
  185  kubectl get nodes
  186  sudo systemctl status k3s
  187  ps aux|grep k3s
  188  kubectl get nodes
  189  kubectl describe node skaria-precision-7510
  190  kubectl run test-on-worker --image=nginx --restart=Never --overrides='{"spec":{"nodeName":"skaria-precision-7510"}}'
  191  kubectl get pod test-on-worker -o wide
  192  kubectl delete  pod test-on-worker -o wide
  193  kubectl delete  pod test-on-worker
  194  kubectl get pods -n kube-system | grep traefik
  195  kubectl get svc -n kube-system | grep traefik
  196  kubectl apply -f https://raw.githubusercontent.com/longhorn/longhorn/v1.6.0/deploy/longhorn.yaml
  197  kubectl get pods -n longhorn-system -o wide -w
  198  kubectl logs -n longhorn-system longhorn-manager-gpfxd --tail=50
  199  sudo apt update
  200  sudo apt install -y open-iscsi
  201  sudo systemctl enable --now iscsid
  202  iscsiadm --version
  203  sudo systemctl status iscsid
  204  sudo modprobe iscsi_tcp
  205  echo "iscsi_tcp" | sudo tee -a /etc/modules
  206  kubectl delete pods -n longhorn-system -l app=longhorn-manager
  207  kubectl get pods -n longhorn-system -w
  208  kubectl get pods -n longhorn-system
  209  kubectl delete pods -n longhorn-system -l app=longhorn-manager
  210  kubectl get pods -n longhorn-system
  211  kubectl get pods -n longhorn-system -w
  212  kubectl get pods -n longhorn-system
  213  kubectl patch storageclass local-path -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"false"}}}'
  214  kubectl patch storageclass longhorn -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
  215  kubectl get storageclass
  216  kubectl apply -f longhorn-test-pvc.yaml 
  217  kubectl get pvc
  218  kubectl apply -f longhorn-test-pod.yaml 
  219  kubectl get pods
  220  kubectl delete pod test-longhorn-pod 
  221  kubectl delete pvc test-longhorn-pvc 
  222  kubectl get pvc
  223  history >> important-setup-commands.txt
  224  more important-setup-commands.txt 
  225  sudo apt install -y curl wget vim git htop net-tools build-essential   apt-transport-https ca-certificates gnupg lsb-release software-properties-common
  226  curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
  227  chmod 700 get_helm.sh
  228  run ./get_helm.sh 
  229  ./get_helm.sh 
  230  rm get_helm.sh 
  231  kubectl create namespace staging
  232  helm repo add bitnami https://charts.bitnami.com/bitnami
  233  helm repo update
  234  helm install postgres bitnami/postgresql -n staging -f postgres-helm.yaml 
  235  kubectl get pods -n staging
  236  helm install kafka bitnami/kafka -n staging -f kafka-helm.yaml 
  237  kubectl wait --for=condition=ready pod -l app.kubernetes.io/name=kafka -n staging --timeout=300s
  238  helm list
  239  helm list -A
  240  helm list -n staging
  241  helm uninstall kafka -n staging
  242  helm list -n staging
  243  kubectl get pods
  244  kubectl get pods -n staging
  245  helm install kafka bitnami/kafka -n staging -f kafka-helm.yaml 
  246  kubectl get pods -n staging
  247  helm install kafka bitnami/kafka -n staging -f kafka-helm.yaml 
  248  kubectl get pods -n staging
  249  helm install kafka bitnami/kafka --set image.repository=bitnamilegacy/kafka -n staging -f kafka-helm.yaml 
  250  kubectl get pods -n staging
  251  helm install kafka bitnami/kafka --set image.repository=bitnamilegacy/kafka -n staging -f kafka-helm.yaml 
  252  kubectl get pods -n staging
  253  helm install zookeeper bitnami/zookeeper --version 12.x   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true
  254  helm install zookeeper bitnami/zookeeper --version 12.x   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  255  helm install kafka bitnami/kafka --set image.repository=bitnamilegacy/kafka -n staging -f kafka-helm.yaml 
  256  kubectl get pods -n staging
  257  helm uninstall my-zk -n staging
  258  kubectl get pods -n staging
  259  pwd
  260  cd kafka-cluster/
  261  cat templates/zookeeper-statefulset.yaml 
  262  cd ..
  263  kubectl get pods -n staging
  264  history |grep helm install
  265  history |grep "helm install"
  266  helm install zookeeper bitnami/zookeeper -n staging 
  267  kubectl get pods -A
  268  kubectl get pods -n staging
  269  kubectl logs zookeeper-0 -n staging
  270  kubectl get pods -n staging
  271  kubectl logs zookeeper-0 -n staging
  272  kubectl describe zookeeper-0 -n staging
  273  kubectl describe pod zookeeper-0 -n staging
  274  helm uninstall zookeeper  -n staging 
  275  helm install zookeeper bitnami/zookeeper --set image.tag=3   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  276  kubectl get pods -n staging
  277  helm install zookeeper bitnami/zookeeper --set image.tag=3   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  278  helm install zookeeper bitnami/zookeeper --set image.tag=3.4.10   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  279  history |grep "bitnamilegacy/zookeeper"
  280  cat /home/k3s-data/server/node-token
  281  sudo cat /home/k3s-data/server/node-token
  282  kubectl get nodes
  283  history 
  284  history >> important-setup-commands.txt 
  285  ls -altr important-setup-commands.txt 
  286  more important-setup-commands.txt 
  287  kubectl get pods -n staging
  288  cat kafka-helm.yaml 
  289  kubectl describe pod kafka-controller-0 -n staging
  290  kubectl get pods -n staging
  291  kubectl describe pod kafka-controller-0 -n staging
  292  helm uninstall kafka -n staging
  293  kubectl describe pod kafka-controller-0 -n staging
  294  helm uninstall kafka -n staging
  295  kubectl describe pod kafka-controller-0 -n staging
  296  helm uninstall kafka -n staging
  297  kubectl describe pod kafka-controller-0 -n staging
  298  kubectl logs pod kafka-controller-0 -n staging
  299  kubectl logs kafka-controller-0 -n staging
  300  kubectl logs kafka-controller-1 -n staging
  301  helm uninstall kafka -n staging
  302  kubectl logs kafka-controller-1 -n staging
  303  kubectl describe pod kafka-controller-0 -n staging
  304  kubectl logs kafka-controller-1 -n staging
  305  kubectl logs kafka-controller-0 -n staging
  306  kubectl describe pod kafka-controller-0 -n staging
  307  helm uninstall kafka -n staging
  308  kubectl delete pvc -l app.kubernetes.io/instance=kafka
  309  kubectl get pvc -l
  310  kubectl get pvc -n staging
  311  kubectl get pvc -l app.kubernetes.io/instance=kafka -n staging
  312  kubectl delete pvc -l app.kubernetes.io/instance=kafka -n staging
  313  kubectl get pods 
  314  helm uninstall zookeeper
  315  kubectl get pods 
  316  kubectl get pods -n staging
  317  kubectl describe pod kafka-controller-0 -n staging
  318  helm uninstall kafka
  319  helm uninstall kafka -n staging
  320  helm uninstall zookeeper -n staging
  321  kubectl get pvc -n staging
  322  kubectl get pvc -l app.kubernetes.io/instance=kafka -n staging
  323  kubectl delete pvc -l app.kubernetes.io/instance=kafka -n staging
  324  helm uninstall kafka -n staging
  325  helm uninstall zookeeper -n staging
  326  kubectl get pvc -l app.kubernetes.io/instance=kafka -n staging
  327  kubectl get pvc -l app.kubernetes.io/instance=zookeeper -n staging
  328  kubectl delete pvc -l app.kubernetes.io/instance=zookeeper -n staging
  329  kubectl get pvc  -n staging
  330  kubectl get pods  -n staging
  331  ls -altr
  332  rm helm-zookeeper.sh 
  333  rm kafka-helm.yaml 
  334  helm create kafka-cluster
  335  cd kafka-cluster/
  336  ls
  337  tree .
  338  sudo apt install tree
  339  tree .
  340  rm templates/service.yaml 
  341  rm templates/deployment.yaml 
  342  touch templates/zookeeper.yaml
  343  ls templates/
  344  vi templates/zookeeper.yaml 
  345  mv templates/zookeeper.yaml templates/zookeeper-service.yaml 
  346  ls templates/
  347  vi templates/zookeeper-statefulset.yaml 
  348  ls
  349  vi values.yaml 
  350  vi templates/zookeeper-service.yaml 
  351  vi templates/zookeeper-statefulset.yaml 
  352  vi values.yaml 
  353  helm my-zk . --namespace -staging --create-namespace
  354  helm install my-zk . --namespace -staging --create-namespace
  355  ls -altr templates/
  356  ls -altr templates/tests/
  357  rm -rf templates/tests/
  358  ls -altr templates/tests/
  359  ls -altr templates/
  360  helm install my-zk . --namespace -staging --create-namespace
  361  rm templates/serviceaccount.yaml 
  362  helm install my-zk . --namespace -staging --create-namespace
  363  rm templates/ingress.yaml 
  364  helm install my-zk . --namespace -staging --create-namespace
  365  rm templates/httproute.yaml 
  366  helm install my-zk . --namespace -staging --create-namespace
  367  rm templates/hpa.yaml 
  368  ls templates/
  369  helm install my-zk . --namespace -staging --create-namespace
  370  rm templates/NOTES.txt 
  371  helm install my-zk . --namespace -staging --create-namespace
  372  helm install my-zk . --namespace staging --create-namespace
  373  kubectl get pods -n staging
  374  cat templates/zookeeper-statefulset.yaml 
  375  kubectl get pods -n staging
  376  cat templates/zookeeper-service.yaml 
  377  cat templates/zookeeper-statefulset.yaml 
  378  cat values.yaml 
  379  vi templates/zookeeper-statefulset.yaml 
  380  vi values.yaml 
  381  kubectl get pods -n staging
  382  helm install my-zk . --namespace staging --create-namespace
  383  kubectl get pods -n staging
  384  kubectl describe pod zookeeper-0 -n staging
  385  kubectl get pods -n staging
  386  kubectl logs zookeeper-0 -n staging
  387  cat values.yaml 
  388  cat templates/zookeeper-statefulset.yaml 
  389  cat templates/zookeeper-service.yaml 
  390  helm uninstall my-zk --namespace staging
  391  kubectl get pods -n staging
  392  vi templates/zookeeper-statefulset.yaml 
  393  helm install my-zk . --namespace staging --create-namespace
  394  kubectl get pods -n staging
  395  kubectl logs zookeeper-0 -n staging
  396  vi templates/zookeeper-statefulset.yaml 
  397  helm uninstall my-zk --namespace staging
  398  helm install my-zk . --namespace staging --create-namespace
  399  kubectl get pods -n staging
  400  kubectl logs zookeeper-0 -n staging
  401  helm uninstall my-zk --namespace staging
  402  vi templates/zookeeper-statefulset.yaml 
  403  helm install my-zk . --namespace staging --create-namespace
  404  kubectl get pods -n staging
  405  kubectl logs zookeeper-0 -n staging
  406  helm uninstall my-zk --namespace staging
  407  kubectl get nodes
  408  helm list
  409  helm list -n staging
  410  helm repo add rhcharts https://ricardo-aires.github.io/helm-charts
  411  helm upgrade --install zkp rhcharts/zookeeper
  412  helm list -n staging
  413  helm list 
  414  helm uninstall zkp
  415  helm list 
  416  helm list -n staging
  417  helm upgrade --install zkp rhcharts/zookeeper -n staging
  418  helm list -n staging
  419  kubectl get pods
  420  kubectl get pods -n staging
  421  helm uninstall zkp -n staging
  422  cd ..
  423  git clone https://github.com/skariajampi/my-helm-charts.git
  424  cd my-helm-charts/
  425  ls
  426  mkdir monitoring
  427  cp ../monitoring/values.yaml monitoring/
  428  ls monitoring/
  429  git status
  430  git add .
  431  git status
  432  git commit -m "added values.yaml for grafana, prometheus monitoring stack"
  433  git push
  434  git config --global credential.helper store
  435  git push
  436  kubectl get pods -A
  437  kubectl drain skariaj-precision-7820-tower   --ignore-daemonsets   --delete-emptydir-data   --grace-period=120   --force
  438  sudo shutdown now
  439  kubectl get pods -A
  440  cd kafka-cluster/
  441  helm install my-zk . --namespace staging --create-namespace
  442  kubectl get pods
  443  kubectl get pods -n staging
  444  kubectl describe pod zookeeper-0 -n staging
  445  kubectl logs zookeeper-0 -n staging
  446  helm uninstall my-zk . --namespace staging
  447  helm uninstall my-zk --namespace staging
  448  helm uninstall my-zk -n staging
  449  kubectl get pods -n staging
  450  kubectl get pvc
  451  kubectl delete pvc
  452  kubectl delete pvc data-zkp-zookeeper-0
  453  kubectl delete pvc data-zkp-zookeeper-1
  454  kubectl delete pvc data-zkp-zookeeper-2
  455  kubectl delete pvc data-zookeeper-0 data-zookeeper-1 data-zookeeper-2 
  456  kubectl get pvc
  457  kubectl delete pvc log-zkp-zookeeper-0 log-zkp-zookeeper-1 log-zkp-zookeeper-2 
  458  kubectl get pvc
  459  kubectl get pvc -n staging
  460  history|grep kubectl delete
  461  history|grep "kubectl delete"
  462  kubectl get pvc -n staging -l app.kubernetes.io/instance=kafka
  463  kubectl get pvc -n staging -l app.kubernetes.io/instance=zookeeper
  464  kubectl delete pvc -n staging -l app.kubernetes.io/instance=zookeeper
  465  kubectl get pvc -n staging -l app.kubernetes.io/instance=zookeeper
  466  kubectl get pvc -n staging 
  467  kubectl get pvc -l app.kubernetes.io/instance=zookeeper -n staging
  468  kubectl get pvc  -n staging
  469  kubectl delete pvc  -n staging data-zkp-zookeeper-0 data-zkp-zookeeper-1 data-zkp-zookeeper-2 datadir-zookeeper-0 datadir-zookeeper-1 datadir-zookeeper-2 
  470  kubectl get pvc  -n staging
  471  kubectl delete pvc  -n staging log-zkp-zookeeper-0 log-zkp-zookeeper-1 log-zkp-zookeeper-2 
  472  kubectl get pvc  -n staging
  473  helm install my-zk . --namespace staging --create-namespace
  474  kubectl get pods
  475  kubectl get pods -n staging
  476  kubectl logs zookeeper-0 -n staging 
  477  helm uninstall my-zk -n staging
  478  helm install my-zk . --namespace staging --create-namespace
  479  kubectl get pods -n staging
  480  kubectl logs zookeeper-0 -n staging
  481  kubectl get pods -n staging
  482  kubectl logs zookeeper-1 -n staging
  483  kubectl logs zookeeper-2 -n staging
  484  kubectl get pods -n staging
  485  kubectl get nodes
  486  kubectl get pods -n staging
  487  helm upgrade my-zk . -n staging
  488  kubectl get pods -n staging 
  489  kubectl logs pod kafka-0 -n staging 
  490  kubectl logs kafka-0 -n staging 
  491  helm uninstall my-zk -n staging
  492  kubectl get pods
  493  kubectl get pods -n staging 
  494  helm install zk-kafka . --namespace staging --create-namespace
  495  kubectl get pods -n staging 
  496  kubectl logs kafka-0 -n staging 
  497  kubectl get pods -n staging 
  498  helm uninstall zk-kafka -n staging
  499  kubectl get pods -n staging 
  500  helm install zk-kafka . --namespace staging --create-namespace
  501  kubectl get pods -n staging 
  502  kubectl logs kafka-0 -n staging 
  503  kubectl get pods -n staging 
  504  kubectl logs kafka-0 -n staging 
  505  helm uninstall zk-kafka -n staging
  506  kubectl get pods -n staging 
  507  kubectl logs kafka-0 -n staging 
  508  kubectl get pods -n staging 
  509  helm install zk-kafka . --namespace staging --create-namespace
  510  kubectl get pods -n staging 
  511  kubectl logs kafka-0 -n staging 
  512  kubectl get pods -n staging 
  513  kubectl logs kafka-0 -n staging 
  514  kubectl get pods -n staging 
  515  kubectl logs kafka-0 -n staging 
  516  kubectl get pods -n staging 
  517  helm uninstall zk-kafka -n staging
  518  kubectl get pods -n staging 
  519  helm install zk-kafka . --namespace staging --create-namespace
  520  kubectl get pods -n staging 
  521  kubectl logs kafka-0 -n staging 
  522  kubectl logs -f kafka-0 -n staging 
  523  kubectl get pods -n staging 
  524  kubectl logs -f kafka-1 -n staging 
  525  kubectl logs -f kafka-2 -n staging 
  526  kubectl get pods -n staging 
  527  kubectl logs -f kafka-1 -n staging 
  528  kubectl get pods -n staging 
  529  kubectl logs -f kafka-2 -n staging 
  530  kubectl get pods -n staging 
  531  kubectl logs -f kafka-2 -n staging 
  532  kubectl get pods -n staging 
  533  kubectl logs -f zookeeper-0 -n staging 
  534  ls -altr
  535  ls -altr Chart.yaml 
  536  cat Chart.yaml 
  537  ls -altr charts/
  538  ls
  539  ls templates/
  540  cat templates/_helpers.tpl 
  541  ls
  542  git init
  543  git status
  544  git add .
  545  git status
  546  git commit -m "initial commit"
  547  git config --global user.email "skariajampi@gmail.com"
  548  git config --global user.name "skariaj"
  549  git commit -m "initial commit"
  550  git status
  551  git branch -M main
  552  git remote add origin https://github.com/skariajampi/my-helm-charts.git
  553  git push -u origin main
  554  git status
  555  git push -u origin main
  556  git status
  557  kubectl get nodes
  558  kubectl label node skaria-precision-7510 role=secondary
  559  kubectl get nodes
  560  kubectl label node skariaj-precision-7820-tower role=main
  561  kubectl get nodes
  562  cd ..
  563  mkdir monitoring
  564  cd monitoring/
  565  kubectl get pvc -n staging 
  566  touch values.yaml
  567  vi values.yaml 
  568  kubectl get nodes --show-labels
  569  helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
  570  helm repo update
  571  kubectl create namespace staging-monitoring
  572  helm install prometheus prometheus-community/kube-prometheus-stack   --namespace staging-monitoring   --values values.yaml   --wait --timeout 10m
  573  kubectl get pods -n staging-monitoring 
  574  kubectl get pods -n staging-monitoring -o wide
  575  kubectl get nodes -o wide | grep secondary
  576  kubectl get nodes -o wide -n staging-monitoring| grep secondary
  577  kubectl get nodes -o wide -n staging-monitoring| grep 192
  578  ls
  579  cd ..
  580  ls
  581  ls -altr
  582  cd monitoring/
  583  ls
  584  kubectl get pods -n staging-monitoring -o wide
  585  kubectl get nodes
  586  kubectl drain skaria-precision-7510   --ignore-daemonsets   --delete-emptydir-data   --grace-period=120
  587  kubectl get nodes
  588  kubectl cordon skariaj-precision-7820-tower
  589  kubectl drain skariaj-precision-7820-tower   --ignore-daemonsets   --delete-emptydir-data   --grace-period=120
  590  kubectl get nodes
  591  kubectl uncordon skariaj-precision-7820-tower
  592  kubectl get nodes
  593  kubectl uncordon skaria-precision-7510 
  594  kubectl get nodes
  595  kubectl get nodes -o wide
  596  history
  597  history >> important-setup-commands.txt 
    1  lsblk
    2  pwd
    3  ls
    4  df -h
    5  sudo apt update
    6  sudo ubuntu-drivers autoinstall
    7  sudo apt update
    8  sudo apt upgrade -y
    9  sudo apt update
   10  sudo apt upgrade -y
   11  sudo dpkg --configure -a
   12  sudo apt upgrade -y
   13  sudo apt autoremove -y
   14  sudo apt upgrade
   15  sudo reboot
   16  sudo apt update
   17  sudo ubuntu-drivers autoinstall
   18  sudo ubuntu-drivers -h
   19  sudo apt install ubuntu-drivers-common
   20  sudo ubuntu-drivers autoinstall
   21  ubuntu-drivers devices
   22  apt search nvidia-driver-390
   23  nvidia-smi
   24  df -h
   25  source "$HOME/.sdkman/bin/sdkman-init.sh"
   26  sdk version
   27  sdk list java
   28  sdk install java 11.0.30-amzn
   29  java -version
   30  sdk list java
   31  sdk install java 17.0.18-amzn
   32  sdk list java
   33  sdk install java 21.0.10-amzn
   34  java -version
   35  java
   36  systemd analyze
   37  systemd-analyze
   38  systemd-analyze blame
   39  sudo apt update
   40  sudo apt updgrade -y
   41  sudo apt upgrade -y
   42  sudo apt install -y curl wget git vim 
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
  101  history
  102  kubectl get nodes
  103  export KUBECONFIG=~/.kube/config
  104  kubectl get nodes
  105  echo 'export KUBECONFIG=~/.kube/config' >> ~/.bashrc 
  106  source ~/.bashrc 
  107  kubectl get nodes
  108  docker run hello-world
  109  docker ps -a
  110  docker container rm eab56
  111  docker ps -a
  112  docker images ls
  113  docker image ls
  114  docker system prune -a
  115  docker image ls
  116  docker ps -a
  117  df -k
  118  df -h
  119  kubectl -n kube-system edit configmap local-path-config 
  120  kubectl -n kube-system delete pod -l app=local-path-provisioner
  121  kubectl -n kube-system get pods
  122  ls -altr /home/k3s-data/
  123  ls -altr /home/k3s-data/data/
  124  kubectl get pvc
  125  ls /home/k8s-pv/
  126  vi test-pvc.yaml
  127  kubectl apply  -f test-pvc.yaml 
  128  kubectl get pvc
  129  ls -altr /home/k8s-pv/
  130  ls -altr /home/k3s-data/
  131  ls -altr /home/k3s-data/server/
  132  sudo ls -altr /home/k3s-data/server/
  133  sudo ls -altr /home/k3s-data/data/
  134  sudo ls -altr /home/k3s-data/
  135  sudo ls -altr /home/k3s-data/agent/
  136  sudo ls -altr /home/k8s-pv/
  137  kubectl get pvc
  138  vi test-pod.yaml
  139  kubectl apply -f test-pod.yaml 
  140  kubectl get pods
  141  kubectl exec -it pvc-test-pod -- sh
  142  kubectl delete pod pvc-test-pod 
  143  kubectl delete pvc test-pvc 
  144  kubectl get pvc
  145  kubectl apply -f test-pvc.yaml 
  146  kubectl get pvc
  147  kubectl apply -f test-pod.yaml 
  148  kubectl get pods
  149  kubectl get pvc
  150  kubectl delete pod pvc-test-pod 
  151  sudo ls -altr /home/k8s-pv/
  152  kubectl apply -f test-pvc.yaml 
  153  sudo ls -altr /home/k8s-pv/
  154  kubectl apply -f test-pod.yaml 
  155  sudo ls -altr /home/k8s-pv/
  156  cd /home/k8s-pv/
  157  sudo cd /home/k8s-pv/
  158  kubectl delete pod pvc-test-pod 
  159  kubectl delete pvc test-pvc 
  160  sudo ls -altr /home/k8s-pv/
  161  ls -altr /home/k8s-pv
  162  pwd
  163  ls -altr /home/k8s-pv
  164  ls -altr /home/k3s-data/
  165  ls -altr /home/k3s-data/data/
  166  pwd
  167  nvidia-sim
  168  sudo nvidia-sim
  169  sudo nvidia-sim-uc
  170  sudo nvidia-smi
  171  pwd
  172  sudo swapoff -a
  173  kubectl get pods -n kube-system
  174  sudo cat /var/lib/rancher/k3s/server/node-token
  175  ls -altr /home/k3s-data/server/
  176  sudo ls -altr /home/k3s-data/server/
  177  sudo cat /home/k3s-data/server/node-token
  178  ip addr show | grep -E "inet " | grep -v 127.0.0.1 | awk '{print $2}' | cut -d/ -f1
  179  kubectl get pods -A
  180  ip a
  181  # Get internal IP (will be used by laptop)
  182  ip addr show | grep -E "inet " | grep -v 127.0.0.1 | awk '{print $2}' | cut -d/ -f1
  183  # Example: 192.168.1.100
  184  sudo systemctl status k3s-agent
  185  kubectl get nodes
  186  sudo systemctl status k3s
  187  ps aux|grep k3s
  188  kubectl get nodes
  189  kubectl describe node skaria-precision-7510
  190  kubectl run test-on-worker --image=nginx --restart=Never --overrides='{"spec":{"nodeName":"skaria-precision-7510"}}'
  191  kubectl get pod test-on-worker -o wide
  192  kubectl delete  pod test-on-worker -o wide
  193  kubectl delete  pod test-on-worker
  194  kubectl get pods -n kube-system | grep traefik
  195  kubectl get svc -n kube-system | grep traefik
  196  kubectl apply -f https://raw.githubusercontent.com/longhorn/longhorn/v1.6.0/deploy/longhorn.yaml
  197  kubectl get pods -n longhorn-system -o wide -w
  198  kubectl logs -n longhorn-system longhorn-manager-gpfxd --tail=50
  199  sudo apt update
  200  sudo apt install -y open-iscsi
  201  sudo systemctl enable --now iscsid
  202  iscsiadm --version
  203  sudo systemctl status iscsid
  204  sudo modprobe iscsi_tcp
  205  echo "iscsi_tcp" | sudo tee -a /etc/modules
  206  kubectl delete pods -n longhorn-system -l app=longhorn-manager
  207  kubectl get pods -n longhorn-system -w
  208  kubectl get pods -n longhorn-system
  209  kubectl delete pods -n longhorn-system -l app=longhorn-manager
  210  kubectl get pods -n longhorn-system
  211  kubectl get pods -n longhorn-system -w
  212  kubectl get pods -n longhorn-system
  213  kubectl patch storageclass local-path -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"false"}}}'
  214  kubectl patch storageclass longhorn -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
  215  kubectl get storageclass
  216  kubectl apply -f longhorn-test-pvc.yaml 
  217  kubectl get pvc
  218  kubectl apply -f longhorn-test-pod.yaml 
  219  kubectl get pods
  220  kubectl delete pod test-longhorn-pod 
  221  kubectl delete pvc test-longhorn-pvc 
  222  kubectl get pvc
  223  history >> important-setup-commands.txt
  224  more important-setup-commands.txt 
  225  sudo apt install -y curl wget vim git htop net-tools build-essential   apt-transport-https ca-certificates gnupg lsb-release software-properties-common
  226  curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
  227  chmod 700 get_helm.sh
  228  run ./get_helm.sh 
  229  ./get_helm.sh 
  230  rm get_helm.sh 
  231  kubectl create namespace staging
  232  helm repo add bitnami https://charts.bitnami.com/bitnami
  233  helm repo update
  234  helm install postgres bitnami/postgresql -n staging -f postgres-helm.yaml 
  235  kubectl get pods -n staging
  236  helm install kafka bitnami/kafka -n staging -f kafka-helm.yaml 
  237  kubectl wait --for=condition=ready pod -l app.kubernetes.io/name=kafka -n staging --timeout=300s
  238  helm list
  239  helm list -A
  240  helm list -n staging
  241  helm uninstall kafka -n staging
  242  helm list -n staging
  243  kubectl get pods
  244  kubectl get pods -n staging
  245  helm install kafka bitnami/kafka -n staging -f kafka-helm.yaml 
  246  kubectl get pods -n staging
  247  helm install kafka bitnami/kafka -n staging -f kafka-helm.yaml 
  248  kubectl get pods -n staging
  249  helm install kafka bitnami/kafka --set image.repository=bitnamilegacy/kafka -n staging -f kafka-helm.yaml 
  250  kubectl get pods -n staging
  251  helm install kafka bitnami/kafka --set image.repository=bitnamilegacy/kafka -n staging -f kafka-helm.yaml 
  252  kubectl get pods -n staging
  253  helm install zookeeper bitnami/zookeeper --version 12.x   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true
  254  helm install zookeeper bitnami/zookeeper --version 12.x   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  255  helm install kafka bitnami/kafka --set image.repository=bitnamilegacy/kafka -n staging -f kafka-helm.yaml 
  256  kubectl get pods -n staging
  257  helm uninstall my-zk -n staging
  258  kubectl get pods -n staging
  259  pwd
  260  cd kafka-cluster/
  261  cat templates/zookeeper-statefulset.yaml 
  262  cd ..
  263  kubectl get pods -n staging
  264  history |grep helm install
  265  history |grep "helm install"
  266  helm install zookeeper bitnami/zookeeper -n staging 
  267  kubectl get pods -A
  268  kubectl get pods -n staging
  269  kubectl logs zookeeper-0 -n staging
  270  kubectl get pods -n staging
  271  kubectl logs zookeeper-0 -n staging
  272  kubectl describe zookeeper-0 -n staging
  273  kubectl describe pod zookeeper-0 -n staging
  274  helm uninstall zookeeper  -n staging 
  275  helm install zookeeper bitnami/zookeeper --set image.tag=3   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  276  kubectl get pods -n staging
  277  helm install zookeeper bitnami/zookeeper --set image.tag=3   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  278  helm install zookeeper bitnami/zookeeper --set image.tag=3.4.10   --set replicaCount=3   --set persistence.enabled=true   --set persistence.size=20Gi   --set persistence.storageClass=longhorn   --set auth.enabled=false   --set allowAnonymousLogin=true --set image.repository=bitnamilegacy/zookeeper -n staging
  279  history |grep "bitnamilegacy/zookeeper"
  280  cat /home/k3s-data/server/node-token
  281  sudo cat /home/k3s-data/server/node-token
  282  kubectl get nodes
  283  history 
  284  history >> important-setup-commands.txt 
  285  ls -altr important-setup-commands.txt 
  286  more important-setup-commands.txt 
  287  kubectl get pods -n staging
  288  cat kafka-helm.yaml 
  289  kubectl describe pod kafka-controller-0 -n staging
  290  kubectl get pods -n staging
  291  kubectl describe pod kafka-controller-0 -n staging
  292  helm uninstall kafka -n staging
  293  kubectl describe pod kafka-controller-0 -n staging
  294  helm uninstall kafka -n staging
  295  kubectl describe pod kafka-controller-0 -n staging
  296  helm uninstall kafka -n staging
  297  kubectl describe pod kafka-controller-0 -n staging
  298  kubectl logs pod kafka-controller-0 -n staging
  299  kubectl logs kafka-controller-0 -n staging
  300  kubectl logs kafka-controller-1 -n staging
  301  helm uninstall kafka -n staging
  302  kubectl logs kafka-controller-1 -n staging
  303  kubectl describe pod kafka-controller-0 -n staging
  304  kubectl logs kafka-controller-1 -n staging
  305  kubectl logs kafka-controller-0 -n staging
  306  kubectl describe pod kafka-controller-0 -n staging
  307  helm uninstall kafka -n staging
  308  kubectl delete pvc -l app.kubernetes.io/instance=kafka
  309  kubectl get pvc -l
  310  kubectl get pvc -n staging
  311  kubectl get pvc -l app.kubernetes.io/instance=kafka -n staging
  312  kubectl delete pvc -l app.kubernetes.io/instance=kafka -n staging
  313  kubectl get pods 
  314  helm uninstall zookeeper
  315  kubectl get pods 
  316  kubectl get pods -n staging
  317  kubectl describe pod kafka-controller-0 -n staging
  318  helm uninstall kafka
  319  helm uninstall kafka -n staging
  320  helm uninstall zookeeper -n staging
  321  kubectl get pvc -n staging
  322  kubectl get pvc -l app.kubernetes.io/instance=kafka -n staging
  323  kubectl delete pvc -l app.kubernetes.io/instance=kafka -n staging
  324  helm uninstall kafka -n staging
  325  helm uninstall zookeeper -n staging
  326  kubectl get pvc -l app.kubernetes.io/instance=kafka -n staging
  327  kubectl get pvc -l app.kubernetes.io/instance=zookeeper -n staging
  328  kubectl delete pvc -l app.kubernetes.io/instance=zookeeper -n staging
  329  kubectl get pvc  -n staging
  330  kubectl get pods  -n staging
  331  ls -altr
  332  rm helm-zookeeper.sh 
  333  rm kafka-helm.yaml 
  334  helm create kafka-cluster
  335  cd kafka-cluster/
  336  ls
  337  tree .
  338  sudo apt install tree
  339  tree .
  340  rm templates/service.yaml 
  341  rm templates/deployment.yaml 
  342  touch templates/zookeeper.yaml
  343  ls templates/
  344  vi templates/zookeeper.yaml 
  345  mv templates/zookeeper.yaml templates/zookeeper-service.yaml 
  346  ls templates/
  347  vi templates/zookeeper-statefulset.yaml 
  348  ls
  349  vi values.yaml 
  350  vi templates/zookeeper-service.yaml 
  351  vi templates/zookeeper-statefulset.yaml 
  352  vi values.yaml 
  353  helm my-zk . --namespace -staging --create-namespace
  354  helm install my-zk . --namespace -staging --create-namespace
  355  ls -altr templates/
  356  ls -altr templates/tests/
  357  rm -rf templates/tests/
  358  ls -altr templates/tests/
  359  ls -altr templates/
  360  helm install my-zk . --namespace -staging --create-namespace
  361  rm templates/serviceaccount.yaml 
  362  helm install my-zk . --namespace -staging --create-namespace
  363  rm templates/ingress.yaml 
  364  helm install my-zk . --namespace -staging --create-namespace
  365  rm templates/httproute.yaml 
  366  helm install my-zk . --namespace -staging --create-namespace
  367  rm templates/hpa.yaml 
  368  ls templates/
  369  helm install my-zk . --namespace -staging --create-namespace
  370  rm templates/NOTES.txt 
  371  helm install my-zk . --namespace -staging --create-namespace
  372  helm install my-zk . --namespace staging --create-namespace
  373  kubectl get pods -n staging
  374  cat templates/zookeeper-statefulset.yaml 
  375  kubectl get pods -n staging
  376  cat templates/zookeeper-service.yaml 
  377  cat templates/zookeeper-statefulset.yaml 
  378  cat values.yaml 
  379  vi templates/zookeeper-statefulset.yaml 
  380  vi values.yaml 
  381  kubectl get pods -n staging
  382  helm install my-zk . --namespace staging --create-namespace
  383  kubectl get pods -n staging
  384  kubectl describe pod zookeeper-0 -n staging
  385  kubectl get pods -n staging
  386  kubectl logs zookeeper-0 -n staging
  387  cat values.yaml 
  388  cat templates/zookeeper-statefulset.yaml 
  389  cat templates/zookeeper-service.yaml 
  390  helm uninstall my-zk --namespace staging
  391  kubectl get pods -n staging
  392  vi templates/zookeeper-statefulset.yaml 
  393  helm install my-zk . --namespace staging --create-namespace
  394  kubectl get pods -n staging
  395  kubectl logs zookeeper-0 -n staging
  396  vi templates/zookeeper-statefulset.yaml 
  397  helm uninstall my-zk --namespace staging
  398  helm install my-zk . --namespace staging --create-namespace
  399  kubectl get pods -n staging
  400  kubectl logs zookeeper-0 -n staging
  401  helm uninstall my-zk --namespace staging
  402  vi templates/zookeeper-statefulset.yaml 
  403  helm install my-zk . --namespace staging --create-namespace
  404  kubectl get pods -n staging
  405  kubectl logs zookeeper-0 -n staging
  406  helm uninstall my-zk --namespace staging
  407  kubectl get nodes
  408  helm list
  409  helm list -n staging
  410  helm repo add rhcharts https://ricardo-aires.github.io/helm-charts
  411  helm upgrade --install zkp rhcharts/zookeeper
  412  helm list -n staging
  413  helm list 
  414  helm uninstall zkp
  415  helm list 
  416  helm list -n staging
  417  helm upgrade --install zkp rhcharts/zookeeper -n staging
  418  helm list -n staging
  419  kubectl get pods
  420  kubectl get pods -n staging
  421  helm uninstall zkp -n staging
  422  cd ..
  423  git clone https://github.com/skariajampi/my-helm-charts.git
  424  cd my-helm-charts/
  425  ls
  426  mkdir monitoring
  427  cp ../monitoring/values.yaml monitoring/
  428  ls monitoring/
  429  git status
  430  git add .
  431  git status
  432  git commit -m "added values.yaml for grafana, prometheus monitoring stack"
  433  git push
  434  git config --global credential.helper store
  435  git push
  436  kubectl get pods -A
  437  kubectl drain skariaj-precision-7820-tower   --ignore-daemonsets   --delete-emptydir-data   --grace-period=120   --force
  438  sudo shutdown now
  439  kubectl get pods -A
  440  cd kafka-cluster/
  441  helm install my-zk . --namespace staging --create-namespace
  442  kubectl get pods
  443  kubectl get pods -n staging
  444  kubectl describe pod zookeeper-0 -n staging
  445  kubectl logs zookeeper-0 -n staging
  446  helm uninstall my-zk . --namespace staging
  447  helm uninstall my-zk --namespace staging
  448  helm uninstall my-zk -n staging
  449  kubectl get pods -n staging
  450  kubectl get pvc
  451  kubectl delete pvc
  452  kubectl delete pvc data-zkp-zookeeper-0
  453  kubectl delete pvc data-zkp-zookeeper-1
  454  kubectl delete pvc data-zkp-zookeeper-2
  455  kubectl delete pvc data-zookeeper-0 data-zookeeper-1 data-zookeeper-2 
  456  kubectl get pvc
  457  kubectl delete pvc log-zkp-zookeeper-0 log-zkp-zookeeper-1 log-zkp-zookeeper-2 
  458  kubectl get pvc
  459  kubectl get pvc -n staging
  460  history|grep kubectl delete
  461  history|grep "kubectl delete"
  462  kubectl get pvc -n staging -l app.kubernetes.io/instance=kafka
  463  kubectl get pvc -n staging -l app.kubernetes.io/instance=zookeeper
  464  kubectl delete pvc -n staging -l app.kubernetes.io/instance=zookeeper
  465  kubectl get pvc -n staging -l app.kubernetes.io/instance=zookeeper
  466  kubectl get pvc -n staging 
  467  kubectl get pvc -l app.kubernetes.io/instance=zookeeper -n staging
  468  kubectl get pvc  -n staging
  469  kubectl delete pvc  -n staging data-zkp-zookeeper-0 data-zkp-zookeeper-1 data-zkp-zookeeper-2 datadir-zookeeper-0 datadir-zookeeper-1 datadir-zookeeper-2 
  470  kubectl get pvc  -n staging
  471  kubectl delete pvc  -n staging log-zkp-zookeeper-0 log-zkp-zookeeper-1 log-zkp-zookeeper-2 
  472  kubectl get pvc  -n staging
  473  helm install my-zk . --namespace staging --create-namespace
  474  kubectl get pods
  475  kubectl get pods -n staging
  476  kubectl logs zookeeper-0 -n staging 
  477  helm uninstall my-zk -n staging
  478  helm install my-zk . --namespace staging --create-namespace
  479  kubectl get pods -n staging
  480  kubectl logs zookeeper-0 -n staging
  481  kubectl get pods -n staging
  482  kubectl logs zookeeper-1 -n staging
  483  kubectl logs zookeeper-2 -n staging
  484  kubectl get pods -n staging
  485  kubectl get nodes
  486  kubectl get pods -n staging
  487  helm upgrade my-zk . -n staging
  488  kubectl get pods -n staging 
  489  kubectl logs pod kafka-0 -n staging 
  490  kubectl logs kafka-0 -n staging 
  491  helm uninstall my-zk -n staging
  492  kubectl get pods
  493  kubectl get pods -n staging 
  494  helm install zk-kafka . --namespace staging --create-namespace
  495  kubectl get pods -n staging 
  496  kubectl logs kafka-0 -n staging 
  497  kubectl get pods -n staging 
  498  helm uninstall zk-kafka -n staging
  499  kubectl get pods -n staging 
  500  helm install zk-kafka . --namespace staging --create-namespace
  501  kubectl get pods -n staging 
  502  kubectl logs kafka-0 -n staging 
  503  kubectl get pods -n staging 
  504  kubectl logs kafka-0 -n staging 
  505  helm uninstall zk-kafka -n staging
  506  kubectl get pods -n staging 
  507  kubectl logs kafka-0 -n staging 
  508  kubectl get pods -n staging 
  509  helm install zk-kafka . --namespace staging --create-namespace
  510  kubectl get pods -n staging 
  511  kubectl logs kafka-0 -n staging 
  512  kubectl get pods -n staging 
  513  kubectl logs kafka-0 -n staging 
  514  kubectl get pods -n staging 
  515  kubectl logs kafka-0 -n staging 
  516  kubectl get pods -n staging 
  517  helm uninstall zk-kafka -n staging
  518  kubectl get pods -n staging 
  519  helm install zk-kafka . --namespace staging --create-namespace
  520  kubectl get pods -n staging 
  521  kubectl logs kafka-0 -n staging 
  522  kubectl logs -f kafka-0 -n staging 
  523  kubectl get pods -n staging 
  524  kubectl logs -f kafka-1 -n staging 
  525  kubectl logs -f kafka-2 -n staging 
  526  kubectl get pods -n staging 
  527  kubectl logs -f kafka-1 -n staging 
  528  kubectl get pods -n staging 
  529  kubectl logs -f kafka-2 -n staging 
  530  kubectl get pods -n staging 
  531  kubectl logs -f kafka-2 -n staging 
  532  kubectl get pods -n staging 
  533  kubectl logs -f zookeeper-0 -n staging 
  534  ls -altr
  535  ls -altr Chart.yaml 
  536  cat Chart.yaml 
  537  ls -altr charts/
  538  ls
  539  ls templates/
  540  cat templates/_helpers.tpl 
  541  ls
  542  git init
  543  git status
  544  git add .
  545  git status
  546  git commit -m "initial commit"
  547  git config --global user.email "skariajampi@gmail.com"
  548  git config --global user.name "skariaj"
  549  git commit -m "initial commit"
  550  git status
  551  git branch -M main
  552  git remote add origin https://github.com/skariajampi/my-helm-charts.git
  553  git push -u origin main
  554  git status
  555  git push -u origin main
  556  git status
  557  kubectl get nodes
  558  kubectl label node skaria-precision-7510 role=secondary
  559  kubectl get nodes
  560  kubectl label node skariaj-precision-7820-tower role=main
  561  kubectl get nodes
  562  cd ..
  563  mkdir monitoring
  564  cd monitoring/
  565  kubectl get pvc -n staging 
  566  touch values.yaml
  567  vi values.yaml 
  568  kubectl get nodes --show-labels
  569  helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
  570  helm repo update
  571  kubectl create namespace staging-monitoring
  572  helm install prometheus prometheus-community/kube-prometheus-stack   --namespace staging-monitoring   --values values.yaml   --wait --timeout 10m
  573  kubectl get pods -n staging-monitoring 
  574  kubectl get pods -n staging-monitoring -o wide
  575  kubectl get nodes -o wide | grep secondary
  576  kubectl get nodes -o wide -n staging-monitoring| grep secondary
  577  kubectl get nodes -o wide -n staging-monitoring| grep 192
  578  ls
  579  cd ..
  580  ls
  581  ls -altr
  582  cd monitoring/
  583  ls
  584  kubectl get pods -n staging-monitoring -o wide
  585  kubectl get nodes
  586  kubectl drain skaria-precision-7510   --ignore-daemonsets   --delete-emptydir-data   --grace-period=120
  587  kubectl get nodes
  588  kubectl cordon skariaj-precision-7820-tower
  589  kubectl drain skariaj-precision-7820-tower   --ignore-daemonsets   --delete-emptydir-data   --grace-period=120
  590  vi idea.sh
  591  ls -altr
  592  chmod u=x,g=x,o=x idea.sh 
  593  ls -altr
  594  ./idea.sh 
  595  chmod 755 idea.sh 
  596  ./idea.sh 
  597  cd ~
  598  cd my-helm-charts/jenkins/
  599  ls
  600  history 
  601  kubectl get nodes
  602  kubectl uncordon skariaj-precision-7820-tower
  603  kubectl get nodes
  604  kubectl uncordon skaria-precision-7510 
  605  kubectl get nodes
  606  kubectl get nodes -o wide
  607  history
  608  history >> important-setup-commands.txt 
  609  ls -latr important-setup-commands.txt 
  610  cd my-helm-charts/
  611  ls
  612  ls -altr templates/
  613  ls templates/
  614  ls monitoring/
  615  mkdir jenkins
  616  cd jenkins/
  617  touch values.yaml
  618  vi values.yaml 
  619  git status
  620  cd ..
  621  git status
  622  helm repo update
  623  helm repo add jenkins https://charts.jenkins.io
  624  helm repo update
  625  kubectl create namespace jenkins
  626  ls jenkins/values.yaml 
  627  cd jenkins/
  628  cat values.yaml 
  629  helm install jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  630  helm install jenkins jenkins/jenkins   --namespace jenkins   --values values.yaml   --wait
  631  ls
  632  ls -altr
  633  vi values.yaml 
  634  helm install jenkins jenkins/jenkins   --namespace jenkins   --values values.yaml   --wait
  635  vi values.yaml 
  636  cat values.yaml 
  637  helm install jenkins jenkins/jenkins   --namespace jenkins   --values values.yaml   --wait
  638  cd ~/software/idea-ultimate/idea-2026.1/
  639  ls
  640  cd idea-IU-261.22158.277/bin/
  641  ls -altr
  642  pwd
  643  ls
  644  ./idea.sh 
  645  pwd
  646  ls -altr
  647  cd ~
  648  kubectl get nodes --show-labels | grep role
  649  helm uninstall jenkins --namespace jenkins
  650  kubectl delete namespace jenkins --wait
  651  ubectl create namespace jenkins
  652  kubectl create namespace jenkins
  653  cd my-helm-charts/jenkins/
  654  ls
  655  ls jenkins-values.yaml 
  656  helm install jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  657  kubectl get pods -n jenkins 
  658  kubectl get pods -n jenkins -o wide
  659  kubectl get secret -n jenkins jenkins -o jsonpath="{.data.jenkins-admin-password}" | base64 --decode && echo
  660  kubectl get svc -n jenkins
  661  kubectl get nodes 
  662  kubectl get nodes -o wide
  663  kubectl get labels
  664  kubectl show labels
  665  helm upgrade jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  666  kubectl get pods -n jenkins -o wide
  667  helm upgrade jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  668  kubectl get pods -n jenkins -o wide
  669  kubectl get pods -n jenkins -l jenkins=agent
  670  kubectl get pods -n jenkins 
  671  kubectl get pods -n jenkins -o wide
  672  kubectl get pods -n jenkins 
  673  kubectl get pods -n jenkins -o wide
  674  history 
  675  cd ..
  676  mkdir sample-git-flow-app
  677  cd sample-git-flow-app/
  678  git init
  679  git add README.md
  680  touch README.md
  681  vi README.md 
  682  git add README.md
  683  git commit -m "initial commit"
  684  git branch -M main
  685  git status
  686  ls
  687  git remote add origin https://github.com/skariajampi/sample-git-flow-app.git
  688  git push -u origin main
  689  git status
  690  git checkout -b develop
  691  git push -u origin develop
  692  git status
  693  git branch -a
  694  git flow init -d
  695  sudo apt update
  696  sudo apt install git-flow
  697  git flow version
  698  git flow init
  699  ls -altr
  700  git status
  701  git flow feature start git-flow-trial
  702  git status
  703  ls
  704  mvn
  705  sdkman list maven
  706  sdkman list java
  707  sdk list java
  708  sdk list maven
  709  sdk install maven 3.9.0
  710  mvn -version
  711  cd sample-git-flow-app/
  712  git status
  713  pwd
  714  ls
  715  mvn clean compile
  716  mvn test
  717  mvn verify
  718  git status
  719  git add .
  720  git status
  721  git commit -m "added minimal spring boot code to test"
  722  git status
  723  mkdir -p k8s/staging
  724  git status
  725  df -k
  726  df -h
  727  cd Desktop/
  728  cat <<EOF > ~/intellij_app.desktop
  729  [Desktop Entry]
  730  Name=Intellij
  731  Comment=Intellij
  732  Exec=software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea
  733  Icon=software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea.png
  734  Terminal=false
  735  Type=Application
  736  EOF
  737  chmod +x ~/intellij_app.desktop
  738  ls
  739  cd ~
  740  ls
  741  cd Desktop/
  742  vi intellij_app.desktop 
  743  cat intellij_app.desktop 
  744  ls -altr ~/software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea
  745  ls -altr ~/software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea.png 
  746  chmod u=x ~/software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea.png
  747  ls -altr ~/software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea.png 
  748  ls -altr intellij_app.desktop 
  749  ls
  750  vi intellij_app.desktop 
  751  ls software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin/idea.png
  752  vi intellij_app.desktop 
  753  htop
  754  ls 
  755  cd ..
  756  ls software/idea-ultimate/idea-2026.1/
  757  ls software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/
  758  ls software/idea-ultimate/idea-2026.1/idea-IU-261.22158.277/bin
  759  pwd
  760  htop
  761  kubectl get nodes
  762  cd my-helm-charts/jenkins/
  763  ls
  764  helm upgrade jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  765  history grep jenkins
  766  history| grep jenkins
  767  kubectl get pods -n jenkins -w
  768  kubectl logs jenkins-0 -n jenkins
  769  kubectl get pods -n jenkins -w
  770  helm rollback jenkins 16 -n jenkins
  771  kubectl get pods -n jenkins -w
  772  kubectl get pods -n jenkins 
  773  kubectl delete pod jenkins-0 -n jenkins
  774  kubectl get pods -n jenkins 
  775  kubectl get pods -n jenkins -w
  776  kubectl get pods -n jenkins 
  777  kubectl get pods -n jenkins -w
  778  kubectl logs jenkins-0 -n jenkins
  779  kubectl get pods -n jenkins -w
  780  helm rollback jenkins 21 -n jenkins
  781  kubectl delete pod jenkins-0 -n jenkins
  782  kubectl get pods -n jenkins -w
  783  helm upgrade jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  784  kubectl get pods -n jenkins -w
  785  kubectl get pods -n jenkins
  786  helm history jenkins -n jenkins
  787  helm upgrade jenkins jenkins/jenkins   --namespace jenkins   --values jenkins-values.yaml   --wait
  788  helm history jenkins -n jenkins
  789  kubectl get pods -n jenkins -w
  790  cd sample-git-flow-app/k8s/
  791  ls
  792  kubectl apply -f maven_cache_pvc.yaml 
  793  kubectl get pvc
  794  kubectl get pvc -A
  795  kubectl delete pvc maven-cache-pvc
  796  kubectl get pvc -n jenkins
  797  kubectl get pvc -A
  798  kubectl get pods -n jenkins -w
  799  kubectl logs -f sample-git-flow-app-main-9-rr6r8-g2g3t-54fh1 -n jenkins
  800  kubectl logs sample-git-flow-app-main-10-k327c-kj2p6-5z10j -n jenkins
  801  kubectl logs sample-git-flow-app-main-10-k327c-kj2p6-5z10j -A
  802  kubectl describe pod sample-git-flow-app-main-10-k327c-kj2p6-5z10j
  803  kubectl describe pod sample-git-flow-app-main-10-k327c-kj2p6-5z10j -n jenkins
  804  kubectl describe pod sample-git-flow-app-main-10-k327c-kj2p6-5z10j -A
  805  git status
  806  git pull origin develop
  807  git status
  808  git checkout main
  809  git pull origin main
  810  git checkout develop
  811  git status
  812  git pull origin main
  813  git status
  814  kubectl get pods -n jenkins -w
  815  helm history jenkins
  816  helm history jenkins -n jenkins
  817  kubectl get nodes -o wide
  818  kubectl create namespace production
  819  cd sample-git-flow-app/k8s/
  820  ls
  821  kubectl apply -f jenkins-rbac.yaml
  822  kubectl get nodes
  823  kubectl get pods -n production
  824  kubectl logs -f sample-gitflow-app-576bd5d8cf-8pnwv
  825  kubectl logs -f sample-gitflow-app-576bd5d8cf-8pnwv -n production 
  826  kubectl get pods -n production
  827  kubectl get nodes
  828  kubectl get pods -n jenkins -w
  829  kubectl get pods -n jenkins 
  830  kubectl get pods -n jenkins -w
  831  kubectl get nodes
  832  kubectl get pods -n jenkins -w
  833  kubectl get nodes
  834  kubectl get pods -n jenkins
  835  kubectl get pods -A
  836  kubectl get pods -n jenkins
  837  history
  838  history >> important-setup-commands.txt

```

---
