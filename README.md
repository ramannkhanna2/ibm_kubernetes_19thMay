# ibm_kubernetes_19thMay

```
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAu4Fc41QrS8W1zG6ekBelHzhs7o8cc+J/P/2iHo05eRYb0Lxe
74kPY5Zl7l78agMG9iB9RTLmvtqiYRhiD78+h5MZWxtlxSYiyopL4dGXFW5dbvCE
g68MUQBHX2uioFl7bjHRgKAn2t21LXqU/g7y+E6wfoIdJopnXd3UEFtlJAf6dFm1
VOrfuETviyjh7sLr4eCNuPunKX/W7N7dvlHj7GCwGQDSOfU91WHP4yT6m5byupxe
diHOFx53jtRJxutL7LXFPpxdLm2IIIoIktiPA0/B1FZjkOY1sVKLEeh+4MCV27o6
rPHdsRBAjCD8N5ikpDWiDfS//K2pTvmIXfwbfwIDAQABAoIBAHgZRt7Q1Z6F94kG
vYc7rebOZG90uNu9EpZxJXr+J/bX418SmJhCqNm3xngk3PYmFDpn2vUMwmEydtlM
HdtKOonp/U6uwMPDRnuGk04DygrPEwdxBN+3qmLjk9OZhKPCTN3rCO6jJoP4iAim
QHJuLtA+zqtpObSq58RmxmLnt2OYo2a0YjEaVYZdZnLJTbbEamFOAjFuMN5jXpfX
BKZkfP1dpf1Vz6LjUkPIohNYiur0kAwfeB/PpLpJPCeaLf975XAPkzlvMhmRg14o
tnI7kFYsHWjRbnUD5A07dqA8b7ImPOHMeni9gUbcj/jJqZxgkhHqG91vbEvhUWJt
FkeKBSECgYEA6XdGZMWuF5MB08tKAk2SLqPMHb10rjG6tWOm6XVUlhTz6A5LmpO0
OOyUMJr7QIkmQ2G+iWjpm0iYbH4QASXLqRodJlAJfPAK9M35Rur+aunJRnE8IKRz
/dwb2+piKJUQNXQwCrbXfzTJkkGSXYfp7ZC118nprpaLcd/BSxCRuXECgYEAzZpx
yEP6T0FaRy0j7LkNpzjkx7U4cgb1zDpS2iHEx7XUf20Y8pW6ItDwqlz2Iypw9Zk7
3uxsO/3a2nw3LWB8Qv72l5IlsJpg3Lb9gKtoU20gwqABAvows176Mwm4euIwqPPx
9YePcYEy2WmCdoVSFlOvhNelNg4/2REOBVNqK+8CgYBjXkbx4UmF8yYV9TKc5FNR
0pmwFtEwyy3CwpVqTGwiLOzbWipHspJEoD06qtxBzZ4hk9q7NZIoa6+kjctWEbYr
VVgO1IYVTT38kCaHTsHW04a9mriS1CwiYqrg4VPCHh/2AGvqQ4RZOiiJPauEb7Lb
UHp1TBVQH/deEnR89KJxoQKBgQCsPs9D728sJpvzNSX7k6yUg11m0bNQE/Sn+9Sd
Wdz5UqOLfWKBGF6v/Esi7m5mV4/6sT0vLPIf8DQBBj9TjJmNpvv/Tzi0EyFCxyrp
OLBV8/6WDmXKkL9sBg2l5Gbgy83oPTZfdAoAFTT8XyAlGtwCSGmq6N5HwvhKabdN
TuyLkQKBgQCXOrUdAKj9Q8Lft8ROnAJaBLDEpdHUwV1HupP1sJRJPALFZkjhcBhR
JFqJDfAtcvlafrH3rVeaT9sXrakWkJRNipruG7MZRc2x4yOPt1SVrlt2KMEfDXX2
BkC7bSk/NnJtNtU17y0cJfcYaZI5wGqfXx0VQwgWWSWT1CZ6PB0QKQ==
-----END RSA PRIVATE KEY-----

https://github.com/ramannkhanna2/ibm_kubernetes_19thMay.git


deploy my application for my clients /users .....

kubernetes ... open source project ...  



why move towards containerization...

            physical deployment of application s         >>>     virtualization                    >>>       containerization ( deploy as containerization)

scaling was an issue , not effectively usage of resources , failure , capacity planning 


lightweight , 

for same use case , i can create more no of containers as compare to vms ~~ more availability for my users 
less downtime for my users ( cz it will be booting quickey ) ( cz of shared os /kernel with the physical linux host)



=========================================================

we discussed ?
how we came to containrization   >>>>>>>>>>>>> kubernetes 



container is similar to vm without an os of its own...

crt :
    docker
    rkt
    crio
    pdman
    
    
    
    orchestrator : manages everything 
      mesos
      docker swarm
      
      
      people started creating these kube clusters on there physical vms ....
      
      
      
      
      
      kubernetes : open source 
          eks , aks , gke, oke ...
          
  ========================================================================
  
  
kubenretes/docker swarm/mesos : manager/orchestration , docker/podman , crio-d : engineer  


=====================================================


login creds :
    
https://685421549691.signin.aws.amazon.com/console

ibm_19thMay

  yh9y#D1-
  
  ===================================================
  
  
  region : oregon ..... >> ec2 service ...
  
  
  ====================================================
  
  using kubernetes to do bewlow :
  purpose to deploy my containerized application on my clsuter 


=========================================================

frame of our 3 node kube clsuster :
    
    master node , : ibm-raman-master
    
    ami : ubuntu
    inst type : t2.medium
    keypair : raman-ibm19th-oregon-key
    ntwrk settings >> edit ..
    reuse  raman-ibm-sg
    storage : 20 gb 
    
    
    
    
    w1, w2:
        ami : ubuntu
    inst type : t2.micro
    reuse ur own keypair
     ntwrk settings >> edit .. reuse  raman-ibm-sg 
    storage : 20 gb 
        
    
    
 
    
    ======================================
    
    login to each server : change hostnames

 sudo -i
 
 hostnamectl set-hostname master
 bash
 
 sudo -i
 hostnamectl set-hostname w1
 bash
 
 sudo -i
  hostnamectl set-hostname w2
  bash
  
  
  ===============================
    
    https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/
    
    
    ** kubernetes has no network of its own **
    
    calico , falnnel , weave , etc
    
    ====================================
    
    history for referbce :
        
        docker
    2  clear
    3  vi script
    4  sh script 
    5  kubectl
    6  kubectl get pods
    7  docker ps
    8  clear
    9  docker ps
   10  ls
   11  clear
   12  vi config.yml
   13  docker ps
   14  kubeadm init --config=config.yml >> cluster_initialized.txt
   15  ls
   16  cat cluster_initialized.txt 
   17  clear
   18  docker ps
   19  clear
   20  docker ps
   21  kubectl get pods
   22  clear
   23  ls
   24  cat cluster_initialized.txt 
   25  docker ps
   26  clear
   27  mkdir -p $HOME/.kube
   28  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
   29  sudo chown $(id -u):$(id -g) $HOME/.kube/config
   30  ls .kube/
   31  cat config.yml 
   32  cat .kube/config 
   33  clear
   34  kubectl get pods
   35  kubectl get nodes
   36  kubectl get pods -A
   37  docker ps
   38  clear
   39  kubectl get pods -A
   40  kubectl get nodes 
   41  kubectl describe node master
   42  kubectl get nodes
   43  kubectl apply -f https://raw.githubusercontent.com/projectcalico/calico/v3.25.0/manifests/calico.yaml
   44  clear
   45  docker ps
   46  clear
   47  kubectl get pods -A
   48  KUBECTL GET NODES
   49  kubectl get nodes
   50  kubectl get pods -A
   51  clear
   52  kubectl get pods -A -o wide
   53  netstat -tulnp
   54  systemctl status kubelet
   55  clear
   56  history
   
   ================
   
   research about below
   code >> dockerfile  >> docker build  >>docker custom image(baseimage+custom image ) 
   
   
   ================================================
   
   
   
-- create namespace of urs first and than do further activuty ....
   
 alias k=kubectl
   85  k get nodes
   86  k get pods
   87  clear
   88  docker ps
   89  clear
   90  k get pods
   91  k get pods -A
   92  k get pods -n kube-system -o wide
   93  k get pods -A -o wide
   94  clear
   95  k api-resources
   96  clear
   97  k run ramanapp --image httpd
   98  k get pods
   99  k get pods -A
  100  k get pods -A -o wide
  101  clear
  102  k get pods -o wide
  103  clear
  104  k get pods -o wide
  105  clear
  106  k get pods
  107  k create ns raman
  108  k get ns
  109  clear
  110  k delete pod ramanapp
  111  k run ramanapp --image httpd -n raman
  112  k get pods
  113  k get pods -n raman
  114  k get pods -A
  115  k get pods -n raman -o wide


=================================================



 mkdir raman
  153  clear
  154  ls
  155  cd raman/
  156  ls
  157  k api-resources
  158  clear
  159  ls
  160  vi pod.yml
  161  cat pod.yml
  162  vi pod.yml
  163  k create -f pod.yml
  164  k get pods -n raman
  165  k get pods -o wide -n raman
  166  k describe pod nginxpod -n raman
  167  clear
  168  k delete pods --all -n raman
  169  ls
  170  k create -f pod.yml
  171  k get pods -o wide -n raman
  172  k get pods -n raman
  173  k delete pod nginxpod -n raman
  174  k get pods -n raman





 vi multiconpod.yml
  177  k create -f multiconpod.yml
  178  k get pods
  179  k get pods -n raman
  180  k get pods -n raman-o wide
  181  k get pods -n raman -o wide
  182  k describe pod -n raman
  183  clear
  184  k get pods -n raman
  185  history
  186  clear
  187  k get pods -n raman
  188  cat multiconpod.yml
  189  k exec -it multiconpod -c nginxcon -- /bin/bash
  190  k exec -it multiconpod -c nginxcon -n raman -- /bin/bash
  191  k exec -it multiconpod -c rediscon -n raman -- /bin/bash
  192  k exec -it multiconpod -c rediscon -n raman -- ls
  193  k exec -it multiconpod -c rediscon -n raman -- ls /data
  194  k exec -it multiconpod -c rediscon -n raman -- ls /root
  195  k exec -it multiconpod -c nginxcon -n raman -- ls
  196  k exec -it multiconpod -c nginxcon -n raman -- mkdir ramantest
  197  k exec -it multiconpod -c nginxcon -n raman -- ls
  198  k exec -it multiconpod -c nginxcon -n raman -- /bin/bash



root@master:~/raman# ls
multiconpod.yml  pod.yml
root@master:~/raman# cat pod.yml
apiVersion: v1
kind: Pod
metadata:
  name: nginxpod
  namespace: raman
spec:
  containers:
  - name: nginxcon
    image: nginx:1.14.2
    ports:
    - containerPort: 80
    
    
    
    
root@master:~/raman# cat multiconpod.yml
apiVersion: v1
kind: Pod
metadata:
  name: multiconpod
  namespace: raman
spec:
  containers:
  - name: nginxcon
    image: nginx:1.14.2
    ports:
    - containerPort: 80
  - name: rediscon
    image: redis
    ports:
    - containerPort: 6379



=======================================================================




 k get pods -A
  402  clear
  403  k run ramanapp --image httpd -n raman
  404  k describe pod -n raman
  405  clear
  406  k run ramanapp2 --image httpd -n raman
  407  k get pods -n raman
  408  k describe pods -n raman | grep -i label
  409  k get pods --selector run=ramanapp1
  410  k get pods --selector run=ramanapp2
  411  k get pods --selector run=ramanapp2 -n raman
  412  k get ns
  413  k run ramanapp -n amal --image httpd
  414  k get pods --selector run=ramanapp2 -A
  415  k get pods --selector run=ramanapp -A
  416  k api-resources
  417  clear
  418  k get ns raman
  419  k describe ns raman
  420  clear
  421  ls
  422  k get pods --selector run=ramanapp2 -n raman
  423  k get pods --selector run=ramanapp -A
  424  ls
  425  cd ram
  426  cd raman
  427  ls
  428  vi pod.yml
  429  k create -f pod.yml
  430  k get pods -A
  431  k get pods --selector run=ramanapp
  432  k get pods --selector run=ramanapp -A
  433  k get pods --selector purpose=training -A


 k get nodes
  438  k describe nodes master
  439  k describe nodes w1
  440  clear
  441  k get pods -o wide -A
  442  k get pods -o wide -A
  443  k label pod ramanapp -n raman "owner=raman"
  444  k describe pod ramanapp -n raman | grep -i label
  445  clear
  446  k get nodes
  447  k label node w1 "a=b"
  448  k describe node w1
  449  k label node w1 "owner=raman"
  450  k describe node w1
  451  k label node w1 "env=prod"
  452  k describe node w1
  453  k label node w2 "env=dev"
  454  k describe node w2
  455  clear
  456  k get nodes --selector "env=dev"
  457  k describe node w1 | grep -i label -A3
  458  k describe node w1 | grep -i label -A5
  459  k describe node w1 | grep -i label -A6
  460  k describe node w1 | grep -i label -A7
  461  k describe node w1 | grep -i label -A8
  462  k describe node w1 | grep -i label -A7
  463  clear
  464  k describe node w1 | grep -i label -A7
  465  k label node w1 "a"-
  466  k describe node w1 | grep -i label -A7
  467  k label node w1 "owner=ramankhanna" --overwrite
  468  k describe node w1 | grep -i label -A7
  469  clear
  470  k describe node w1 | grep -i label -A7
  471  k describe node w2 | grep -i label -A7
  472  k get pods -n raman
  473  k delete pods --all -n raman
  474  ls
  475  vi pod.yml
  476  k create -f pod.yml
  477  k get pods -o wide -n raman
  478  vi pod.yml
  479  k create -f pod.yml
  480  k get pods -n raman -o wide
  481  vi pod.yml
  482  k create 0f pod.yml
  483  k create -f pod.yml
  484  k get pods -n raman -o wide


root@master:~/raman# cat pod.yml
apiVersion: v1
kind: Pod
metadata:
  #name: nginxpod
  #name: nginxpod2
  name: nginxpod3
  namespace: raman
  labels:
    run: ramanapp  # <-- This is your custom label
    purpose: training
    project: test
spec:
  containers:
  - name: nginxcon
    image: nginx:1.14.2
    ports:
    - containerPort: 80
  nodeSelector:
    env: dev


======================================================

deployment , replicaset : apps/v1 ~ replication/deployment controller ~ controller manager ....


k get pods -A
  501  clear
  502  k api-resources
  503  clear
  504  vi pod.yml
  505  k create -f pod.yml
  506  k get pods -n raman
  507  cat pod.yml
  508  k getpods --selector "project=test"-A
  509  k getpods --selector "project=test" -A
  510  k get pods --selector "project=test" -A
  511  k delete pod nginxpod1 -n raman
  512  k get pods -n raman
  513  k delete pod -n raman --all


root@master:~/raman# cat pod.yml
apiVersion: v1
kind: Pod
metadata:
  name: nginxpod1
  namespace: raman
  labels:
    run: ramanapp  # <-- This is your custom label
    purpose: training
    project: test
spec:
  containers:
  - name: nginxcon
    image: nginx:1.14.2
    ports:
    - containerPort: 80
---
apiVersion: v1
kind: Pod
metadata:
  name: nginxpod2
  namespace: raman
  labels:
    run: ramanapp  # <-- This is your custom label
    purpose: training
    project: test
spec:
  containers:
  - name: nginxcon
    image: nginx:1.14.2
    ports:
    - containerPort: 80
---
apiVersion: v1
kind: Pod
metadata:
  name: nginxpod3
  namespace: raman
  labels:
    run: ramanapp  # <-- This is your custom label
    purpose: training
    project: test
spec:
  containers:
  - name: nginxcon
    image: nginx:1.14.2
    ports:
    - containerPort: 80


--------------------------------------------------------------------------


 k api-reources | grep dep
  518  k api-resources | grep -i dep
  519  k create -h
  520  clear
  521  k create deploy ramandep --image nginxdemos/hello --replicas 4
  522  k delete deploy --all -A
  523  clear
  524  k get pods -A
  525  k get nodes
  526  k get pods -n raman
  527  k describe deploy ramandep -n raman
  528  k get rs -n raman
  529  clear
  530  k get rs -n raman
  531  k describe rs -n raman
  532  clear
  533  k get deploy -n raman
  534  k get rs -n raman
  535  k get pods -n raman
  536  k get pods -n raman -o wide
  537  curl 192.168.190.65
  538  clear
  539  k get pods -n raman
  540  k scale deploy ramandep --replicas 1 -n raman
  541  k get pods -n raman
  542  k scale deploy ramandep --replicas 5 -n raman
  543  k get pods -n raman
  544  k delete pod ramandep-9b98c4fcb-zxfrc -n raman
  545  k get pods -n raman
  546  clear
  547  ls
  548  k get deploy -n raman
  549  k edit deploy ramandep -n raman
  550  k get pods -n raman
  551  clear
  552  ls
  553  k get deploy -n raman
  554  k get deploy -n raman -o yaml
  555  clear
  556  k get deploy -n raman -o yaml > testdeploy.yml
  557  ls
  558  cat testdeploy.yml
  559  clear
  560  ls
  561  rm -rf testdeploy.yml
k delete deploy -n raman --all
=========================================================================


application  : paused ~ downtime ....
update all ~ recreate / rolling update strategy ..

at 1 time ~ only 3 servers to be getting updated 

sys1
sys2
sys3
sys4
sys5
sys6
sys7
sys8
sys9
sys10



100 pods(v1)

changed the deploy file , updated the image 
rolling update , max surge : 25%


                    25 pods (v1 version)---------------------------100 pods(v1)  ------------------ 25 pods (newer version )
                    
                    
                    75 v1 pods , 25 new pods 
                    
                  25 pods (v1)                                            25 new pods 



=========================================================


 k delete deploy --all -n raman
  599  clear
  600  ls
  601  vi deploy.yml
  602  cat deploy.yml
  603  vi deploy.yml
  604  k create -f deploy.yml --record=true
  605  k rollout status raman-dep -n raman
  606  k rollout deploy status raman-dep -n raman
  607  k rollout status deploy raman-dep -n raman
  608  k get deploy
  609  k get deploy  -n raman
  610  k describe deploy raman-dep -n raman
  611  clear
  612  k get deploy -n raman
  613  k get rs -n raman
  614  k get pods -n raman
  615  k describe pods -n raman | grep -i image
  616  clear
  617  vi deploy.yml
  618  k rollout history deploy raman-dep -n raman
  619  kubectl rollout history deployment raman-dep --revision=1 -n raman
  620  cat deploy.yml
  621  k apply -f deploy.yml --record=true -n raman
  622  clear
  623  k get deploy -n raman
  624  k get rs  -n raman
  625  k describe rs raman-dep-7c49b759b7
  626  k describe rs raman-dep-7c49b759b7 -n raman
  627  clear
  628  k get rs -n raman
  629  k get pods -n raman
  630  k rollout history deploy raman-dep -n raman
  631  kubectl rollout history deployment raman-dep --revision=2 -n raman
  632  k describe pods -n raman | grep -i image
  633  clear
  634  vi deploy.yml
  635  k apply -f deploy.yml --record=true
  636  k rollout status deploy raman-dep -n raman
  637  k get deploy -n raMAN
  638  k get deploy -n raman
  639  k get rs -n raman
  640  k get pods -n raman
  641  kubectl rollout history deployment raman-dep --revision=1 -n raman
  642  kubectl rollout history deployment raman-dep -n raman
  643  k describe pods -n raman | grep -i image
  644  clear
  645  kubectl rollout undo deployment raman-dep --to-revision=1
  646  kubectl rollout undo deployment raman-dep --to-revision=1 -n raman
  647  k describe pods -n raman | grep -i image
  648  kubectl rollout undo deployment raman-dep --to-revision=2 -n raman
  649  k describe pods -n raman | grep -i image
  650  k get rs -n raman


root@master:~/raman# cat deploy.yml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-dep
  namespace: raman
  labels:
    app: web2-prod-app
spec:
  replicas: 5
  strategy:
    type: Recreate
#    type: RollingUpdate
#    rollingUpdate:
#      maxSurge: 25%
#      maxUnavailable: 25%
  selector:
    matchLabels:
      app: rk
  template:
    metadata:
      labels:
        app: rk
    spec:
      containers:
      - name: nginx
        #image: nginx:1.14.1
        #image: nginx:1.14.2
        image: nginx:latest
        ports:
        - containerPort: 80


below just fr reference :
    
    
    v1--- nginx:1.14.1
raman-dep
raman-dep-7b5f547448
raman-dep-7b5f547448-55j9c   1/1     Running   0          3m34s
raman-dep-7b5f547448-bm5j8   1/1     Running   0          3m34s
raman-dep-7b5f547448-f2vj4   1/1     Running   0          3m34s
raman-dep-7b5f547448-n4dxg   1/1     Running   0          3m34s
raman-dep-7b5f547448-tldxw   1/1     Running   0          3m34s


v2 --- nginx:1.14.2
raman-dep
raman-dep-7c49b759b7
raman-dep-7c49b759b7-4hbm7   1/1     Running   0          4m6s
raman-dep-7c49b759b7-fvn9w   1/1     Running   0          4m6s
raman-dep-7c49b759b7-jbr8z   1/1     Running   0          4m6s
raman-dep-7c49b759b7-mtm78   1/1     Running   0          4m6s
raman-dep-7c49b759b7-z2l4f   1/1     Running   0          4m6s


v3--latest
raman-dep
raman-dep-664fdf6568  
raman-dep-664fdf6568-bhtmb   1/1     Running   0          89s
raman-dep-664fdf6568-c9f98   1/1     Running   0          89s
raman-dep-664fdf6568-dpv2s   1/1     Running   0          89s
raman-dep-664fdf6568-f2g2p   1/1     Running   0          89s
raman-dep-664fdf6568-sghkh   1/1     Running   0          89s




========================================================================
 21st may :


docker run --name c1 -p 8082:80 httpd



services : expose my application(deployment/pod) :
    
    either internally : clusterIp service  , 
    either externally : nodeport svc , loadbalancer svc 


========================================================


k get nodes
 2003  clear
 2004  k get nodes
 2005  k get pods -A
 2006  k get deploy -A
 2007  clear
 2008  k api-resources | grep -i service
 2009  clear
 2010  k run ramanapp -n raman --image httpd
 2011  k get pods -n raman
 2012  k get pods -n raman -o wide
 2013  curl 192.168.190.99:80
 2014  k expose pod ramanapp -n raman --type NodePort --target-port 80 --port 80 --name extpodsvc
 2015  k get svc -n raman
 2016  k delete svc extpodsvc -n raman
 2017  clear
 2018  k expose pod ramanapp -n raman --type LoadBalancer --target-port 80 --port 80 --name extpodsvc
 2019  k get svc -n raman
 2020  k get pods -n raman
 2021  k get svc -n raman
 2022  k delete svc -n raman extpodsvc
 2023  k expose pod ramanapp -n raman --type NodePort --target-port 80 --port 80 --name extpodsvc
 2024  k get svc -n raman



for exploratory refernce :
    
    https://github.com/ramannkhanna2/kubernetes_end2end_front-backend.git
    
    
=========================================================================




root@master:~/raman# cat depservice.yml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
  namespace: raman
  labels:
    app: nginx
spec:
  replicas: 4
  selector:
    matchLabels:
      app: tr
  template:
    metadata:
      labels:
        app: tr
    spec:
      containers:
      - name: nginx
        image: nginxdemos/hello
        ports:
        - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
  name: raman-service
  namespace: raman
spec:
  type: NodePort
  selector:
    app: tr
  ports:
    - port: 80
      # By default and for convenience, the `targetPort` is set to
      # the same value as the `port` field.
      targetPort: 80
      # Optional field
      # By default and for convenience, the Kubernetes control plane
      # will allocate a port from a range (default: 30000-32767)
      nodePort: 30007




 k get pods -n raman
 2036  k get svc -n raman
 2037  k delete pods --all -n raman
 2038  k delete svc --all -n raman
 2039  clear
 2040  ls
 2041  vi depservice.yml
 2042  k create -f depservice.yml
 2043  k get pods -n raman
 2044  k get pods -n raman -o wide
 2045  vi depservice.yml
 2046  k apply -f depservice.yml
 2047  cat depservice.yml
 2048  clear
 2049  k get pods -n raman
 2050  k get pods -o wide
 2051  k get pods -o wide -n raman
 2052  k get svc -n raman
 2053  k describe svc raman-service -n raman
 2054  vi depservice.yml
 2055  k apply -f depservice.yml
 2056  k describe svc raman-service -n raman
 2057  k get pods -n raman
 2058  k get pods -n raman -o wide
 2059  k get ep
 2060  k get ep -n raman
 2061  clear
 2062  ls
 2063  cat depservice.yml


============================================================




root@master:~/raman# cat deploy.yml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-blue-original-dep
  namespace: raman
  labels:
    app: web2-prod-app
spec:
  replicas: 5
  selector:
    matchLabels:
      ap: ng
  template:
    metadata:
      labels:
        ap: ng
    spec:
      containers:
      - name: nginx
        image: nginx:latest
        ports:
        - containerPort: 80
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-green-testing-dep
  namespace: raman
  labels:
    app: web2-prod-app2
spec:
  replicas: 5
  selector:
    matchLabels:
      ap: ht
  template:
    metadata:
      labels:
        ap: ht
    spec:
      containers:
      - name: httpd
        image: httpd
        ports:
        - containerPort: 80




root@master:~/raman# cat service.yml
apiVersion: v1
kind: Service
metadata:
  name: raman-service
  namespace: raman
spec:
  type: NodePort
  selector:
    ap: ng
  ports:
    - port: 80
      # By default and for convenience, the `targetPort` is set to
      # the same value as the `port` field.
      targetPort: 80
      # Optional field
      # By default and for convenience, the Kubernetes control plane
      # will allocate a port from a range (default: 30000-32767)
      nodePort: 30007





 k get pods -o wide
 2082  k get pods -o wide -n raman
 2083  cat depservice.yml
 2084  clear
 2085  vi service.yml
 2086  k create -f service.yml
 2087  k get svc -n raman
 2088  k delete svc -n raman --all
 2089  k create -f service.yml
 2090  k get pods -n raman
 2091  k get svc -n raman
 2092  vi deploy.yml
 2093  k apply -f deploy.yml
 2094  k get pods -n raman -o wide
 2095  cat service.yml
 2096  vi service.yml
 2097  k apply -f service.yml
 2098  vi service.yml
 2099  k apply -f service.yml
 2100  clear
 2101  ls
 2102  cat deploy.yml
 2103  cat service.yml


=======================================================================




root@master:~/raman# cat deploy.yml
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-v1-dep
  namespace: raman
  labels:
    app: web2-prod-app
spec:
  replicas: 2
  selector:
    matchLabels:
      app: canary
  template:
    metadata:
      labels:
        app: canary
    spec:
      containers:
      - name: nginx
        image: nginx:latest
        ports:
        - containerPort: 80
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-v2-dep
  namespace: raman
  labels:
    app: web2-prod-app2
spec:
  replicas: 3
  selector:
    matchLabels:
      app: canary
  template:
    metadata:
      labels:
        app: canary
    spec:
      containers:
      - name: httpd
        image: httpd
        ports:
        - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
  name: raman-service
  namespace: raman
spec:
  type: NodePort
  selector:
    app: canary
  ports:
    - port: 80
      # By default and for convenience, the `targetPort` is set to
      # the same value as the `port` field.
      targetPort: 80
      # Optional field
      # By default and for convenience, the Kubernetes control plane
      # will allocate a port from a range (default: 30000-32767)
      nodePort: 30008



 cat deploy.yml
 2143  k create -f deploy.yml
 2144  k get pods
 2145  clear
 2146  k get pods -n raman
 2147  k get svc -n raman
 2148  k describe svc -n raman
 2149  vi deploy.yml
 2150  k apply -f deploy.yml
 2151  clear
 2152  k get pods
 2153  clear
 2154  k get pods -n raman
 2155  k get svc -n raman
 2156  k describe svc -n raman
 2157  clear
 2158  k get pods -n raman
 2159  vi deploy.yml
 2160  k apply -f deploy.yml
 2161  k get pods -n raman
 2162  vi deploy.yml
 2163  k apply -f deploy.yml
 2164  vi deploy.yml
 2165  k apply -f deploy.yml
 2166  ls
 2167  clear
 2168  cat deploy.yml




while true; do
  clear
  curl http://44.244.89.20:30008/
  sleep 1
done

=================================================================






---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-v1-dep
  namespace: raman
  labels:
    app: web2-prod-app
spec:
  replicas: 10
  selector:
    matchLabels:
      app: canary
  template:
    metadata:
      labels:
        app: canary
    spec:
      containers:
      - name: nginx
        image: nginx:latest
        ports:
        - containerPort: 80
          #nodeName: w1



 k get nodes
 2197  k describe node master
 2198  clear
 2199  k describe node master | grep -i taint
 2200  k describe node w1 | grep -i taint
 2201  k describe node w2 | grep -i taint
 2202  k describe node master
 2203  clear
 2204  ls
 2205  k create dep2.yml
 2206  k create -f dep2.yml
 2207  k get pods -n raman
 2208  k get pods -n raman -o wide
 2209  clear
 2210  k get pods -n raman -o wide | grep -i w1
 2211  k describe nodes | grep -i taint
 2212  k describe node w1 |grep -i label -A4
 2213  k describe node w2 |grep -i label -A4
 2214  k describe node master |grep -i label -A4
 2215  k describe node master |grep -i label -A6
 2216  kubectl taint nodes w1 env=prod:NoSchedule
 2217  k describe node w1 |grep -i label -A4
 2218  k describe node master | grep -i taint
 2219  k describe node w1 | grep -i taint
 2220  k describe node w2 | grep -i taint
 2221  k get pods -n raman -o wide | grep w1
 2222  k get pods -n raman -o wide | grep w2
 2223  k delete pod -n raman raman-v1-dep-76d4b575bf-w2fzv
 2224  clear
 2225  k describe node master | grep -i taint
 2226  k describe node w1 | grep -i taint
 2227  k describe node w2 | grep -i taint
 2228  k get pods -n raman -o wide | grep w1
 2229  k get pods -n raman -o wide | grep w2
 2230  vi deploy.yml
 2231  vi dep2.yml
 2232  k apply -f dep2.yml
 2233  k get pods -n raman -o wide | grep w1
 2234  k get pods -n raman -o wide | grep w2
 2235  vi dep2.yml
 2236  k apply -f dep2.yml
 2237  k get pods -n raman -o wide | grep w1
 2238  k get pods -n raman -o wide | grep w2
 2239  k describe node w1 | grep -i taint
 2240*
 2241  k describe node w1 | grep -i taint
 2242  k describe node w2 | grep -i taint
 2243  k describe node master | grep -i taint
 2244  kubectl taint nodes w2 env=dev:NoExecute
 2245  k describe node w2 | grep -i taint
 2246  k get pods -n raman -o wide | grep -i w1
 2247  k get pods -n raman -o wide | grep -i w2
 2248  kubectl taint nodes w2 env-
 2249  clear
 2250  k describe nodes | grep -i taint



===================================================




---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: raman-v1-dep
  namespace: raman
  labels:
    app: web2-prod-app
spec:
  replicas: 10
  selector:
    matchLabels:
      app: canary
  template:
    metadata:
      labels:
        app: canary
    spec:
      containers:
      - name: nginx
        image: nginx:latest
        ports:
        - containerPort: 80
          #nodeName: w1
      nodeSelector:
        node-role.kubernetes.io/control-plane: ""  # Or "master" if using that label
      tolerations:
      # these tolerations are to have the app runnable on control plane nodes
      # remove them if your control plane nodes should not run pods
      - key: node-role.kubernetes.io/control-plane
        operator: Exists
        effect: NoSchedule
      - key: node-role.kubernetes.io/master
        operator: Exists
        effect: NoSchedule



k describe nodes | grep -i taint
 2256  clear
 2257  k describe nodes | grep -i taint
 2258  vi dep2.yml
 2259  k create -f dep2.yml
 2260  k deploy -n raman --all
 2261  k delete deploy -n raman --all
 2262  k create -f dep2.yml
 2263  k get pods -n raman -o wide
 2264  cat dep2.yml
 2265  k delete -f dep2.yml
 2266  k get pods -n raman -o wide
 2267  vi dep2.yml
 2268  k create -f dep2.yml
 2269  k get pods -n raman -o wide
 2270  clear
 2271  k get pods -A | grep -i master
 2272  clear
 2273  k get pods -A -o wide | grep -i master
 2274  k delete -f dep2.yml
 2275  k get pods -A -o wide | grep -i master
 2276  cleat


==================================================


deployments , daemonset


root@master:~/raman# cat daemon.yml
apiVersion: apps/v1
kind: DaemonSet
metadata:
  name: fluentd-elasticsearch
  namespace: raman
  labels:
    k8s-app: fluentd-logging
spec:
  selector:
    matchLabels:
      name: raman
  template:
    metadata:
      labels:
        name: raman
    spec:
      tolerations:
      # these tolerations are to have the daemonset runnable on control plane nodes
      # remove them if your control plane nodes should not run pods
      - key: node-role.kubernetes.io/control-plane
        operator: Exists
        effect: NoSchedule
      - key: node-role.kubernetes.io/master
        operator: Exists
        effect: NoSchedule
      containers:
      - name: fluentd-elasticsearch
        image: nginx
        resources:
          limits:
            memory: 200Mi
          requests:
            cpu: 100m
            memory: 200Mi
        volumeMounts:
        - name: rkhanna
          mountPath: /var/log
      # it may be desirable to set a high priority class to ensure that a DaemonSet Pod
      # preempts running Pods
      # priorityClassName: important
      terminationGracePeriodSeconds: 30
      volumes:
      - name: rkhanna
        hostPath:
          path: /var/log




 k get pods -n raman
 2285  vi daemon.yml
 2286  k create -f daemon.yml
 2287  k get pods -n raman
 2288  k delete -f daemon.yml
 2289  vi daemon.yml
 2290  k create -f daemon.yml
 2291  k get pods -n raman
 2292  vi daemon.yml
 2293  cd /var/log/
 2294  cd ~
 2295  k get pods
 2296  k get pods -n raman
 2297  k describe pod fluentd-elasticsearch-8m6tj -n raman
 2298  clear
 2299  k get pods -n raman
 2300  k get pods -n raman -o wide
 2301  k delete pod fluentd-elasticsearch-npf67 -n raman
 2302  k get pods -n raman -o wide
 2303  k delete -f daemon.yml
 2304  cd raman
 2305  k delete -f daemon.yml


========================================================


22nd :
    

2 secrets:

$SECRET_USERNAME ~code

$SECRET_PASSWD ~code 

------

username :
   echo 'ramankhanna' | base64   : cmFtYW5raGFubmEK

password :
   echo 'ramankhanna123' | base64  : cmFtYW5raGFubmExMjMK



-- create a secret on kbe-cluster :

root@master:~# cat secret.yml
apiVersion: v1
kind: Secret
metadata:
  name: my-secrets
  namespace: raman
type: Opaque
data:
  username: cmFtYW5raGFubmEK
  password: cmFtYW5raGFubmExMjMK









--- deploy.yml :


apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp-deployment
  labels:
    app: myapp
spec:
  replicas: 1
  selector:
    matchLabels:
      app: myapp
      type: front-end
  template:
    metadata:
      labels:
        app: myapp
        type: front-end
    spec:
      containers:
      - name: httpd-container
        image: httpd
        env:
        - name: SECRET_USERNAME
          valueFrom:
            secretKeyRef:
              name: my-secrets
              key: username
        - name: SECRET_PASSWD
          valueFrom:
            secretKeyRef:
              name: my-secrets
              key: password



 k get pods -A
 2021  echo 'ramankhanna' | base64
 2022  echo 'ramankhanna123' | base64
 2023  vi secretdeploy.yml
 2024  vi secret.yml
 2025  vi secret.yml
 2026  k create -f secret.yml
 2027  k get secrets
 2028  k get secrets -n raman
 2029  k describe secret -n raman
 2030  cat secret.yml
 2031  rm -rf secret.yml
 2032  k describe secret -n raman
 2033  k get pods -A
 2034  k describe secret -n raman
 2035  clear
 2036  k get all -n raman
 2037  k get secrets -n raman
 2038  k get pods -n raman
 2039  ls
 2040  cd raman
 2041  ls
 2042  vi secdeploy.yml
 2043  vi secdeploy.yml
 2044  k create -f secdeploy.yml
 2045  k get pods
 2046  k get pods -n raman
 2047  k describe pod -n raman
 2048  clear
 2049  k get secrets -n raman
 2050  k get pod -n raman
 2051  k exec -it myapp-deployment-58c6b5c57c-tkw7b -- /bin/bash
 2052  k exec -it myapp-deployment-58c6b5c57c-tkw7b -n raman -- /bin/bash

====================================================================






echo "hell from prod" > prod.html
 2061  ls
 2062  k get cm -n raman
 2063  k create cm prod.cmap -h
 2064  clear
 2065  k create cm prod.cmap --from-file=prod.html
 2066  ls
 2067  cat prod.html
 2068  k delete cm prod.cmap
 2069  k create cm prod.cmap --from-file=prod.html -n raman
 2070  k get cm -n raman
 2071  k describe cm -n raman prod.cmap
 2072  k get cm -n raman
 2073  k get cm prod.cmap -n raman
 2074  k get cm prod.cmap -n raman -o yaml
 2075  k get cm prod.cmap -n raman -o yaml > prod-cmap.yml
 2076  ls
 2077  cat prod-cmap.yml
 2078  clear
 2079  ls
 2080  clear
 2081  k get cm -n raman
 2082  k get pods -n raman
 2083  k delete deploy --all -n raman
 2084  vi podcm.yml
 2085  cat podcm.yml
 2086  k create -f podcm.yml
 2087  k get pods -n raman
 2088  k get cm -n raman
 2089  k get pods -n raman-o wide
 2090  k get pods -n raman -o wide
 2091  curl 192.168.190.105:80
 2092  k expose pod nginx -n raman --type NodePort -port 80 --target-port 80 --name cmsvc
 2093  k expose pod nginx -n raman --type NodePort --port 80 --target-port 80 --name cmsvc
 2094  clear
 2095  k get cm -n raman
 2096  k get pods -n raman
 2097  k get svc -n raman
 2098  echo "hell from dev" > dev.html
 2099  ls
 2100  k create cm dev.cmap --from-file=dev.html -n raman
 2101  k get cm -n raman
 2102  ls
 2103  vi podcm.yml
 2104  k apply -f podcm.yml
 2105  k get pods
 2106  k get pods -n raman
 2107  clear
 2108  k replace --force -f podcm.yml




root@master:~/raman# cat prod.html
hell from prod

root@master:~/raman# cat dev.html
hell from dev

root@master:~/raman# cat podcm.yml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
  namespace: raman
  labels:
    app: nginx
spec:
  containers:
  - name: nginx
    image: nginx:latest
    ports:
    - containerPort: 80
    volumeMounts:
    - name: rk
      mountPath: /usr/share/nginx/html
  volumes:
    - name: rk
      configMap:
        name: prod.cmap
        #name: dev.cmap
        items:
         - key: prod.html
       # - key: dev.html
          path: index.html

=========================================================================================




developer code ~~ docker build ~ custom image ~  talk to the kubernets adminstartor abt the storage for thier application 

machine leraning : 100 gb pv , 
first tier based app : 20 gb data
db app : 50 gb 


a few persistent vol ~ 10 , 20 , 40 gb , 100 gb 



Volumes in Kubernetes :

✅ 1. Ephemeral Volumes (tied to Pod lifecycle)

Volume Type                                                     Description
emptyDir                        Created when Pod is assigned to a node, deleted when Pod is removed.
configMap                        Mounts ConfigMap data into the Pod.
secret                                Mounts secret data securely into the Pod.
downwardAPI                        Provides Pod metadata (like labels, annotations) to the container.
projected                        Combines multiple sources (ConfigMap, Secret, DownwardAPI, etc.) into one.



🧊 Persistent Volumes (PVs) (independent of Pod lifecycle)

Volume Type                                                        Description
hostPath                                                Maps a file or directory from the host node’s filesystem. (Not recommended in production)
local                                                          Uses a specific local disk on a node. Suitable for single-node use.
nfs                                                            Mounts a directory from a remote NFS server.
iscsi                                                          Connects to storage using iSCSI protocol.
glusterfs                                                Mounts volumes using GlusterFS.
cephfs                                                        Connects to CephFS distributed filesystem.
azureDisk / azureFile                                Azure storage support (block and file storage).
awsElasticBlockStore (EBS)                        AWS block storage.
gcePersistentDisk                                  Google Cloud Persistent Disks.
vsphereVolume                                            For vSphere environments.
portworxVolume                                          Enterprise storage plugin by Portworx.


==================================================

[ BACKEND STORAGE LAYER ]
+---------------------------+
|  NFS Server / EBS / GCE  |
|  Disk / LocalDisk etc.   |
+---------------------------+
            ▲
            │
            │ Provisioned manually or dynamically
            │
[ ADMIN or STORAGE CLASS ]
+----------------------------------+
| PersistentVolume (PV)           |◄──── Admin-defined or auto-created
|----------------------------------|     via StorageClass + PVC
| Capacity: 10Gi                   |
| Access Modes: RWO,ROX,RWX       |
| Reclaim Policy: Retain/Delete   |
| Volume Source: awsElasticBlock  |
+----------------------------------+
            ▲
            │
            │ Bound by Kubernetes scheduler
            │
[ USER / DEVELOPER ]
+----------------------------------+
| PersistentVolumeClaim (PVC)     |◄───── User-defined request
|----------------------------------|
| Requested: 5Gi                   |
| Access Modes: ReadWriteOnce     |
| StorageClass: fast-ssd          |
| Status: Bound (to PV)           |
+----------------------------------+
            ▲
            │
            │ Mounted as volume in Pod
            │
[ WORKLOAD ]
+--------------------------------------------------+
| Pod: my-app-pod                                  |
|--------------------------------------------------|
| Container: my-app                                |
|--------------------------------------------------|
| VolumeMount: /app/data                           |
|   ▲                                              |
|   │                                              |
|   │ Reference: PVC → Bound PV → Real Storage     |
+--------------------------------------------------+



------------------------------------------------------------------------------------------------------------------



 apt install -y nfs-server       or    apt-get install nfs-common    (ubuntu)
 mkdir /efs
 cd /
 sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.12.142:/ efs
 df -h
 cd /efs
 ls -l




root@master:~/raman# cat pv.yml
apiVersion: v1
kind: PersistentVolume
metadata:
  name: raman-website
spec:
  capacity:
    storage: 11Mi
  accessModes:
    - ReadWriteMany
  mountOptions:
    - hard
    - nfsvers=4.1
  nfs:
    path: /
    server: 172.31.17.79
root@master:~/raman# cat pvc.yml
apiVersion: v1
kind: PersistentVolumeClaim
metadata:
  name: raman-demo
  namespace: raman
spec:
  accessModes:
  - ReadWriteMany
  resources:
    requests:
      storage: 5Mi
  volumeName: raman-website
root@master:~/raman# cat pvdeploy.yml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nfs-raman
  namespace: raman
spec:
  replicas: 5
  selector:
    matchLabels:
      role: nfs-raman
  template:
    metadata:
      labels:
        role: nfs-raman
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
        volumeMounts:
        - name: nfs
          mountPath: /usr/share/nginx/deploydata
      volumes:
      - name: nfs
        persistentVolumeClaim:
          claimName: raman-demo




apt-get install nfs-common
 2011  mkdir /efs
 2012  ls /
 2013  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.15.0:/ efs
 2014  cd /
 2015  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.15.0:/ efs
 2016  cd /
 2017  ls
 2018  cd efs/
 2019  ls
 2020  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.15.0:/efs
 2021  cd ..
 2022  ls
 2023  clear
 2024  pwd
 2025  ls
 2026  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.15.0:/ efs
 2027  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.15.0:/efs
 2028  ls
 2029  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.17.79:/ efs
 2030  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.17.79:/efs
 2031  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.17.79: /efs
 2032  clear
 2033  sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport 172.31.17.79:/ efs
 2034  cd efs
 2035  ls
 2036  rm -rf ironman
 2037  ls
 2038  cd /root
 2039  cd raman
 2040  ls
 2041  vi pv.yml
 2042  k create -f pv.yml
 2043  k get pv
 2044  vi pvc.yml
 2045  vi pvc.yml
 2046  k delete pv --all
 2047  vi pv.yml
 2048  k create -f pv.yml
 2049  vi pvc.yml
 2050  k get pv
 2051  k create -f pvc.yml
 2052  k get pvc
 2053  k delete pvc --all
 2054  vi pvc.yml
 2055  k create -f pvc.yml
 2056  clear
 2057  k get pv
 2058  k get pvc
 2059  k get pvc -n raman
 2060  k get pods -n raman
 2061  k delete pods -n raman --all
 2062  vi pvdeploy.yml
 2063  vi pvdeploy.yml
 2064  k create -f pvdeploy.yml
 2065  k get pods -n raman
 2066  k get pods -n raman -w
 2067  clear
 2068  k get pods -n raman
 2069  k describe pod nfs-raman-677796cfbb-nvkwr -n raman
 2070  clear
 2071  k get pods
 2072  k delete deploy --all -n raman
 2073  cat pv.yml
 2074  cat pvc.yml
 2075  cat pvdeploy.yml
 2076  k get pvc
 2077  k get pvc -n raman
 2078  clear
 2079  cat pv.yml
 2080  cat pvc.yml
 2081  cat pvdeploy.yml
 2082  k create -f pvdeploy.yml
 2083  k get pods
 2084  k describe clear
 2085  k describe pod -n raman
 2086  clear
 2087  cat pv.yml
 2088  cat pvc.yml
 2089  k get pv
 2090  k get pv -n raman
 2091  k get pods -n raman
 2092  clear
 2093  k delete deploy --all -n raman
 2094  k delete pvc -n raman
 2095  k get pv
 2096* k get pvc -n
 2097  k get pvc -n raman
 2098  k delete pv -n raman --all
 2099  k delete pv raman-website
 2100  clear
 2101  k get pv
 2102  ls
 2103  k create -f pv.yml
 2104  k get pv
 2105  vi pvc.yml
 2106  k create -f pvc.yml
 2107  k get pvc -n raman
 2108  clear
 2109  k get pv
 2110  k get pvc -n raman
 2111  k create -f pvdeploy.yml
 2112  k get pods
 2113  k get pods -n raman
 2114  k exec -it -n raman nfs-raman-677796cfbb-4hbtq -- /bin/bash
 2115  k get pods -n raman
 2116  k exec -it nfs-raman-677796cfbb-td4pv -n raman -- /bin/bash
 2117  cat pv.yml


-====================================================

authentication :

badge: bob.key
id card ~ bob.crt


bob wants to enter into a building :

bob shud be having a badge with his personal details ....

reception/security center  : taking ur badge seeing ur details, on that badge they will attach a chip and give u an id card ( registration)   


--------------------------------------------------------------------------------

bob wants to access the kubernetes cluster :
    
bob.key  (badge details)  , reshma , rakesh , etc....

kubernetes adminstrator ~ they will create a csr (certificate signing request ) to the api server to sign them with a self signed certificate ca.crt ...

api server will sign the csr and then send back bob.crt, rakesh.crt , reshma.crt



raman who is not there in above proces :

( bob.key , bob.crt )
( reshma.key , reshma.crt )

raman.key , fake.crt ~ api server will reject his accesibility///...

----------------------------------------------------------------------------------------------------------------------


🧪 Lab: Creating and Managing Users in Kubernetes

-- Kubernetes does not store user objects like traditional Linux systems. Instead, authentication is handled externally (e.g., via certificates, tokens, or external identity providers), and authorization is handled inside Kubernetes using RBAC.

Authentication: Validates the identity (e.g., certificates, tokens).

Authorization: Grants permissions (e.g., Roles, ClusterRoles, RoleBindings).


                           Kubernetes Cluster
                              (API Server)
                                   │
                        ┌──────────┴──────────┐
                        │                     │
              Trusts this CA cert       Rejects others
               (ca.crt public key)
                        │
                        ▼
           ┌────────────────────────┐
           │ Certificate Authority  │
           │ (ca.crt + ca.key)      │
           └────────────────────────┘
                       ▲
                       │
       ┌─────────────────────────────┐
       │ You generate a CSR for Bob │
       │    (bob.csr from bob.key)   │
       └─────────────────────────────┘
                       │
   Sign bob.csr with ca.crt + ca.key
                       ▼
          🔏 You get bob.crt (signed cert)
                       │
                       ▼
  Add to kubeconfig:
  - user: bob
  - cert: bob.crt
  - key:  bob.key
                       │
                       ▼
     🔒 Bob runs `kubectl` ➝ API Server checks:
     - Is cert signed by trusted CA? ✅
     - Does Bob have permission? 🔒 RBAC


----------------------------------------------------------------

🧠 What’s Happening in Kubernetes
👤 Bob uses kubectl to connect to the Kubernetes API server.

He provides:

bob.crt (his certificate)

bob.key (his private key)

The API server checks:

“Was bob.crt signed by someone I trust — my CA (ca.crt)?”

If yes → ✅ Bob is authenticated.
----------------------------------------------------------------




🔧 Prerequisites
kubectl and openssl installed


Step 1: 🔐 Generate a Certificate for a New User
1.1 Create a private key and CSR (Certificate Signing Request)

openssl genrsa -out bob.key 2048

openssl req -new -key bob.key -out bob.csr -subj "/CN=bob"


#openssl req -new -key bob.key -out bob.csr -subj "/CN=bob/O=developers"    
#openssl req -new -key bob.key -out bob.csr -subj "/CN=reshma/O=developers"    
#openssl req -new -key bob.key -out bob.csr -subj "/CN=rakesh/O=developers"    
# above one if want to add bob in a group called developers to which u can assign a role afterwards just like a user

-- CN=bob: The username
-- O=developers: Group

Step 2: 🖋️ Sign the CSR with Kubernetes CA
Find your Kubernetes CA cert and key. Usually found in:

/etc/kubernetes/pki/ca.crt
/etc/kubernetes/pki/ca.key

-- Use them to sign the certificate:

openssl x509 -req -in bob.csr -CA ca.crt -CAkey ca.key -CAcreateserial \
-out bob.crt -days 365

-- This generates bob.crt, the signed certificate.


Step 3 : Create a backup of config file:  (JustIn Case)

root@master:~# cd .kube/
root@master:~/.kube# ls
cache  config
root@master:~/.kube# cp config config_bak
root@master:~/.kube# ls
cache  config  config_bak



🛠️ Step 4: Add User and Context to Existing Kubeconfig
3.1 Add user

kubectl config set-credentials bob \
  --client-certificate=bob.crt \
  --client-key=bob.key
  
  
  

-- This updates ~/.kube/config and adds a new user entry named bob.

3.2 Add a context for the new user
-- Find your current cluster name:


kubectl config get-clusters
kubectl config get-users

-- Use that cluster name in the context:

kubectl config set-context bob@kubernetes \
  --cluster=kubernetes \
  --user=bob \
  --namespace=default     


-- Set the context:

kubectl config use-context bob@kubernetes


-- Check your current context:

kubectl config current-context

🧪 Step 4: Test Access (Should Be Forbidden)

kubectl get pods

-- Expected result:

Error from server (Forbidden): User "bob" cannot list resource "pods" in API group "" in the namespace "default"

Try adding RBAC and see the user responding accordingly ...
--------

-- Delete the user and related objects :

kubectl config delete-context bob-context
kubectl config delete-user bob
rm -rf bob.key bob.crt bob.csr

kubectl config view 
kubectl config use-context kubernetes-admin@kubernetes
kubectl config view 


================================================================================
RBAC :


Lab Activity: Enforce Namespace-Specific Permissions and Test Access
Step 1: Create a Namespace
Create a new namespace for testing:

bash
Copy
kubectl create namespace test
Verify the namespace:

bash
Copy
kubectl get namespaces
Step 2: Create a Role
Create a Role that allows read-only access to Pods in the test-namespace:

Write the following YAML to a file (pod-reader-role.yaml):


apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  namespace: test-namespace
  name: pod-reader
rules:
- apiGroups: [""]
  resources: ["pods"]
  verbs: ["get", "list", "watch"]
Apply the Role:

bash
Copy
kubectl apply -f pod-reader-role.yaml
Verify the Role:

bash
Copy
kubectl get roles -n test-namespace
Step 3: Create a ServiceAccount
Create a ServiceAccount in the test-namespace:

bash
Copy
kubectl create serviceaccount test-sa -n test-namespace
Verify the ServiceAccount:

bash
Copy
kubectl get serviceaccounts -n test-namespace
Step 4: Create a RoleBinding
Bind the pod-reader Role to the test-sa ServiceAccount:

Write the following YAML to a file (pod-reader-rolebinding.yaml):

apiVersion: rbac.authorization.k8s.io/v1
kind: RoleBinding
metadata:
  name: pod-reader-binding
  namespace: raman
subjects:
- #kind: ServiceAccount
  kind: User
  #kind: Group
  #name: developers
  name: bob
  #namespace: raman
roleRef:
  kind: Role
  name: pod-reader
  apiGroup: rbac.authorization.k8s.io

  
  
Apply the RoleBinding:

bash
Copy
kubectl apply -f pod-reader-rolebinding.yaml
Verify the RoleBinding:

bash
Copy
kubectl get rolebindings -n test-namespace
Step 5: Test Access Using kubectl auth can-i
Authenticate as the ServiceAccount:

Use the --as flag to impersonate the test-sa ServiceAccount and test access.

Test Permissions:

Check if the ServiceAccount can list Pods in the test-namespace:

bash
Copy
kubectl auth can-i list pods --namespace test-namespace --as system:serviceaccount:test-namespace:test-sa
Expected Output: yes.

Check if the ServiceAccount can create Pods in the test-namespace:

bash
Copy
kubectl auth can-i create pods --namespace test-namespace --as system:serviceaccount:test-namespace:test-sa
Expected Output: no (since the Role only allows get, list, and watch).

Check if the ServiceAccount can list Pods in the default namespace:

bash
Copy
kubectl auth can-i list pods --namespace default --as system:serviceaccount:test-namespace:test-sa
Expected Output: no (since the Role is namespace-specific).




history for refernece :

 cd /root/raman
 2129  ls
 2130  ls -ltr
 2131  clear
 2132  openssl genrsa -out bob.key 2048
 2133  ls -ltr
 2134  cat bob.key
 2135  cat /root/.kube/
 2136  cat /root/.kube/config
 2137  clear
 2138  openssl req -new -key bob.key -out bob.csr -subj "/CN=bob"
 2139  ls -ltr
 2140  cat bob.csr
 2141  k get csr
 2142  k get csr -A
 2143  clear
 2144  ls -ltr
 2145  cp /etc/kubernetes/pki/ca.crt .
 2146  ls
 2147  cp /etc/kubernetes/pki/ca.key .
 2148  ls -ltr
 2149  openssl x509 -req -in bob.csr -CA ca.crt -CAkey ca.key -CAcreateserial -out bob.crt -days 365
 2150  ls -ltr
 2151  cat bob.crt
 2152  cat bob.key
 2153  clear
 2154  kubectl --server=https://54.186.132.223:6443   --certificate-authority=/etc/kubernetes/pki/ca.crt   --client-certificate=./bob.crt   --client-key=./bob.key   get pods
 2155  clear
 2156  cd /root/.kube/
 2157  ls
 2158  cp config config_bak
 2159  ls
 2160  k config -h
 2161  k config get-users
 2162  k config view
 2163  ls -ltr
 2164  clear
 2165  cd /root/
 2166  ls
 2167  cd ram
 2168  cd raman/
 2169  ls
 2170  ls -ltr
 2171  kubectl config set-credentials bob   --client-certificate=bob.crt   --client-key=bob.key
 2172  cat /root/.kube/config
 2173  kubectl --server=https://54.186.132.223:6443   --certificate-authority=/etc/kubernetes/pki/ca.crt   --client-certificate=./bob.crt   --client-key=./bob.key   get pods
 2174  clear
 2175  cat /root/.kube/config
 2176  clear
 2177  k config -h
 2178  k config get-users
 2179  k config get-clusters
 2180  k config view
 2181  clear
 2182  kubectl get pods
 2183  kubectl get deploy -A
 2184  k config view
 2185  k config -h
 2186  clear
 2187  kubectl config set-context bob-context   --cluster=kubernetes   --user=bob   --namespace=default
 2188  k config -h
 2189  k config get-users
 2190  k config get-contexts
 2191  kubectl config set-context bob@kubernetes   --cluster=kubernetes   --user=bob   --namespace=default
 2192  k config get-contexts
 2193  k config delete-context bob-context
 2194  k config get-contexts
 2195  k get pods -A
 2196  clear
 2197  kubectl config use-context bob@kubernetes
 2198  k config get-context
 2199  k config get-contexts
 2200  k get pods
 2201  k config -h
 2202  clear
 2203  k get pods
 2204  k get pods -n raman
 2205  kubectl create namespace test
 2206  k config -h
 2207  k config set-context kubernetes-admin@kubernetes
 2208  k get pods -n raman
 2209  history
 2210  k config get-contexts
 2211  k config use-context kubernetes-admin@kubernetes
 2212  k get pods
 2213  clear
 2214  ls
 2215  vi role.yml
 2216  k create -f role.yml
 2217  k get roles -n raman
 2218  vi rolebind.yml
 2219  k create -f rolebind.yml
 2220  k get role -n raman
 2221  k describe role -n raman
 2222  k get rolebinding -n raman
 2223  k describe  rolebinding -n raman
 2224  k config view
 2225  k config use-context bob@kubernetes
 2226  k get pods
 2227  k get pods -n raman
 2228  clear
 2229  k get pods -n raman
 2230  k config use-context kubernetes-admin@kubernetes
 2231  k get roles -n raman
 2232  cat role.yml
 2233  cat rolebinding.yml
 2234  ls
 2235  cat rolebind.yml
 2236  k config view
 2237  vi rolebind.yml
 2238  k apply -f rolebind.yml
 2239  k config use-context bob@kubernetes
 2240  k get pods
 2241  k get pods -n raman
 2242  k run ramanapp -n raman httpd
 2243  k run ramanapp -n raman --image httpd
 2244  k config use-context kubernetes-admin@kubernetes
 2245  vi role.yml
 2246  k apply -f role.yml
 2247  k config use-context bob@kubernetes
 2248  k get pods
 2249  k get secrets
 2250  k get deploy
 2251  k pods -n raman
 2252  k get pods -n raman
 2253  k get deploy -n raman
 2254  k run ramanapp -n raman --image httpd
 2255  k get pods
 2256  k get pods -n raman
 2257  ls
 2258  cat rolebind.yml



==============================================================


23rd :
    
    
    etcd backup :
        
    location of my static pods : apiserver, etcd , controllermanager, scheduler ....
    
    kubelet manages thes static poids above ; so i have to frstly find kubelets config file ~ static pod path...
    
kubeetes config file path : /var/lib/kubelet/config.yaml
staticPodPath: /etc/kubernetes/manifests


---------------------------------------------------------------------------


ETCD Backup and Restoration:


--- create some random pods ...


-- https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/#backing-up-an-etcd-cluster

apt  install etcd-client

 export ETCDCTL_API=3


-- finding the static files path :

ps -ef | grep kubelet
  652  cd /var/lib/kubelet/
  653  ls
  654  cat config.yaml 


BACKUP :

etcdctl --endpoints=https://127.0.0.1:2379 \
  --cacert=<trusted-ca-file> --cert=<cert-file> --key=<key-file> \
  snapshot save <backup-file-location>



etcdctl --endpoints=https://127.0.0.1:2379 \
  --cacert=/etc/kubernetes/pki/etcd/ca.crt --cert=/etc/kubernetes/pki/etcd/server.crt --key=/etc/kubernetes/pki/etcd/server.key \
  snapshot save /root/myclust.db



-- after taking bckup delete allpods ...


echo "🔥 Deleting all Deployments (except kube-system)..."
kubectl get deployments --all-namespaces --no-headers | \
awk '$1 != "kube-system" {print "kubectl delete deployment " $2 " -n " $1}' | bash

------------------------------------------------------------------------------------------------------------------------------------



RESTORE NOW :



etcdctl --data-dir <data-dir-location> snapshot restore snapshot.db

-- find the original data directory :

ps -ef | grep etcd

/var/lib/etcd : original data directory 


-- restore at new data dir location : (DONT CREATE A DIRECTORY WITH MKDIR RESTORE COMMND WILL AUTOM CREATE etcd-new DIRECT)

etcdctl --data-dir /var/lib/etcd-new snapshot restore /root/myclust.db



-- now to make changes into effect ,change the hostpath in manifest file acc to new data directory :

vi /etc/kubernetes/manifests/etcd.yaml

... ... ...


 volumes:
  - hostPath:
      path: /etc/kubernetes/pki/etcd
      type: DirectoryOrCreate
    name: etcd-certs
  - hostPath:
      path: /var/lib/etcd-new
      type: DirectoryOrCreate
    name: etcd-data


--- will take some time , after sometime ... check ur pods will b bck again

 2029  watch -n 1 docker ps -a

========================================================================


kubeadm >> 

kubernetes...
https://v1-30.docs.kubernetes.io/docs/tasks/administer-cluster/kubeadm/kubeadm-upgrade/


for master node :
-- on master :
    

✅ Step 1: Add Kubernetes v1.30 APT Repo
Kubernetes now uses pkgs.k8s.io for package distribution. Use the v1.30 repo like this:


sudo tee /etc/apt/sources.list.d/kubernetes.list <<EOF
deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.30/deb/ /
EOF


--upgraded kubeadm software to 1.30.0 :

# replace x in 1.30.x-* with the latest patch version
sudo apt-mark unhold kubeadm && \
sudo apt-get update && sudo apt-get install -y kubeadm='1.30.0-1.1' && \
sudo apt-mark hold kubeadm


plan :
    
kubeadm upgrade plan --ignore-preflight-errors=CoreDNSUnsupportedPlugins,CoreDNSMigration


-- real upgrade of master is happening:
kubeadm upgrade apply v1.30.0 --ignore-preflight-errors=CoreDNSUnsupportedPlugins,CoreDNSMigration



-- upgrade kubectl as well as agent node i.e kubelte :
    
# replace x in 1.30.x-* with the latest patch version
sudo apt-mark unhold kubelet kubectl && \
sudo apt-get update && sudo apt-get install -y kubelet='1.30.0-1.1' kubectl='1.30.0-1.1' && \
sudo apt-mark hold kubelet kubectl


sudo systemctl daemon-reload
sudo systemctl restart kubelet


master   Ready    control-plane   3d23h   v1.30.0
w1       Ready    <none>          3d22h   v1.29.15
w2       Ready    <none>          3d22h   v1.29.15

=====================================================================

for worker nodes :
    
    on w1 :
    
sudo tee /etc/apt/sources.list.d/kubernetes.list <<EOF
deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v1.30/deb/ /
EOF

on w1 :
    
    
    # replace x in 1.30.x-* with the latest patch version
sudo apt-mark unhold kubeadm && \
sudo apt-get update && sudo apt-get install -y kubeadm='1.30.0-1.1' && \
sudo apt-mark hold kubeadm


on master :
    
# execute this command on a control plane node
# replace w1 with the name of your node you are draining
kubectl drain w1 --ignore-daemonsets



on w1 :
    
sudo kubeadm upgrade node

# replace x in 1.30.x-* with the latest patch version
sudo apt-mark unhold kubelet kubectl && \
sudo apt-get update && sudo apt-get install -y kubelet='1.30.0-1.1' kubectl='1.30.0-1.1' && \
sudo apt-mark hold kubelet kubectl


sudo systemctl daemon-reload
sudo systemctl restart kubelet



on master :
    
# execute this command on a control plane node
# replace <node-to-uncordon> with the name of your node
kubectl uncordon w1



root@master:~# k get nodes
NAME     STATUS   ROLES           AGE     VERSION
master   Ready    control-plane   3d23h   v1.30.0
w1       Ready    <none>          3d22h   v1.30.0
w2       Ready    <none>          3d22h   v1.29.15

===============================================================================


k describe 

k get events

k logs -f ramanapp -n raman

docker ps


🧠 1. Troubleshooting etcd Failure
etcd is the key-value store used as the source of truth for all cluster data.
🔍 Common Symptoms

API server cannot connect (connection refused, context deadline exceeded)


kubectl get commands hang or fail


Cluster components restart or behave inconsistently
🧰 Troubleshooting Steps✅ a. Check etcd Pod Status (if using static pods)
bash
CopyEdit
kubectl get pods -n kube-system -l component=etcd
✅ b. Check Logs
bash
CopyEdit
journalctl -u etcd -f# or, if running as a pod:
kubectl logs -n kube-system etcd-<node-name>

Look for:


Disk I/O errors


Corrupt WAL entries


Snapshot failures


Quorum issues
✅ c. Check etcd Health Manually
bash
CopyEdit
ETCDCTL_API=3 etcdctl \
  --endpoints=https://127.0.0.1:2379 \
  --cacert=/etc/kubernetes/pki/etcd/ca.crt \
  --cert=/etc/kubernetes/pki/etcd/server.crt \
  --key=/etc/kubernetes/pki/etcd/server.key \
  endpoint health
✅ d. Check Disk Space
etcd requires space for its WAL (write-ahead log) and snapshots:
bash
CopyEdit
df -h
✅ e. Check etcd Cluster Status
bash
CopyEdit
ETCDCTL_API=3 etcdctl member list
ETCDCTL_API=3 etcdctl endpoint status --write-out=table

Look for:


Inconsistent member statuses


Lagging followers
✅ f. Restore from Snapshot (if required)
If corruption is detected:
bash
CopyEdit
ETCDCTL_API=3 etcdctl snapshot restore snapshot.db

You must update the static pod manifest with the new data directory.
🧠 2. Troubleshooting Kubelet Failure
Kubelet is the node agent that registers the node and manages pod lifecycles.
🔍 Common Symptoms

Node NotReady


Pods stuck in Pending, Unknown, or Terminating


kubelet not starting
🧰 Troubleshooting Steps✅ a. Check Kubelet Status
bash
CopyEdit
systemctl status kubelet
journalctl -u kubelet -f
✅ b. Validate Configuration
Check for:


Invalid flags (from /var/lib/kubelet/config.yaml or systemd unit)


Certificate issues


Incorrect cgroup driver (systemd vs cgroupfs)
✅ c. Check Node Status
bash
CopyEdit
kubectl get nodes
kubectl describe node <node-name>
✅ d. Check API Server Connectivity
bash
CopyEdit
curl -k https://localhost:10250/metrics

If Kubelet is failing due to API server unavailability, look at:
bash
CopyEdit
journalctl -u kubelet | grep 'Unable to connect'
✅ e. Check Pod Manifest Directory
Static pods may cause kubelet failure due to:


Invalid YAMLs in /etc/kubernetes/manifests


Syntax errors
✅ f. Check Resource Limits
Ensure the node has enough:


CPU, memory


Inodes


Disk space
🧠 3. Troubleshooting Container Runtime Failure
This refers to issues in CRI (Container Runtime Interface) layer: containerd, Docker (deprecated), CRI-O, etc.
🔍 Common Symptoms

Pods stuck in ContainerCreating


Image pull failures


Container start failures


Kubelet errors in logs about runtime
🧰 Troubleshooting Steps✅ a. Check Runtime Daemon
bash
CopyEdit
# For containerd
systemctl status containerd
journalctl -u containerd -f
# For CRI-O
systemctl status crio
journalctl -u crio -f
✅ b. Check Kubelet Logs for Runtime Errors
bash
CopyEdit
journalctl -u kubelet | grep -i "container runtime"
✅ c. Check crictl Tool Output
bash
CopyEdit
crictl ps -a
crictl images
crictl info
crictl pods
crictl inspect <container_id>

Make sure crictl is configured to point to correct socket (e.g., /run/containerd/containerd.sock)
✅ d. Check Image Pull Issues
bash
CopyEdit
kubectl describe pod <pod-name>  # Check Events section

Common problems:


Invalid registry


Wrong image name


Missing pull secrets
✅ e. Containerd-Shim / OOM Errors

Look for /run/containerd/... errors


Confirm containerd-shim is not OOM killed
🧠 4. Troubleshooting Scheduler Failure
The Kubernetes scheduler assigns Pods to Nodes.
🔍 Common Symptoms

Pods remain in Pending state with no scheduling


Events say "no nodes available"


Scheduler pod is crashed or not running
🧰 Troubleshooting Steps✅ a. Check Scheduler Pod Status
bash
CopyEdit
kubectl get pods -n kube-system -l component=kube-scheduler
kubectl logs -n kube-system kube-scheduler-<node-name>
✅ b. Check kubectl describe pod <pod>
Focus on Events:


0/1 nodes are available: ...


Taints not tolerated


Resource requests not satisfied


NodeSelector, Affinity/Anti-Affinity failures
✅ c. Check Node Availability
bash
CopyEdit
kubectl get nodes
kubectl describe node <node-name>

Look for:


Unschedulable (kubectl cordon)


Taints


Pressure conditions (disk/memory)
✅ d. Check Scheduler Config (for custom schedulers)
Validate:


Policy configuration


Plugins


Logs
✅ e. Check for Multiple Schedulers (rare)
Make sure no competing custom schedulers are interfering.
✅ Summary Table
ComponentKey ToolingCheck LogsHealth Check Commandetcdetcdctljournalctl -u etcdetcdctl endpoint healthKubeletsystemd / logsjournalctl -u kubelet/metrics on port 10250Container Runtimecrictl, containerdjournalctl -u containerdcrictl ps, crictl infoSchedulerkubectl, logskubectl logs -n kube-systemPod events + Scheduler logs


============================================================================================


Note : make sure u have t3.large nodes in ur cluster...

curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
  261  chmod 700 get_helm.sh
  262  ./get_helm.sh
  263  clear
  264  helm
  265  clear
  266  ls
  267  helm repo list
  268  helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
  269  helm search repo prometheus-community
  270  helm search repo prometheus-community/kube-prometheus-stack
  271  helm search repo prometheus-community/kube-prometheus-stack --versions
  276  helm install prometheus prometheus-community/kube-prometheus-stack   --version 45.7.1   --namespace monitoring   --create-namespace   --set kubeEtcd.enabled=false
  277  helm list
  278  helm list -n monitoring
  279  clear
  280  k get pods -n monitoring
  281  k get svc -n monitoring

  k edit svc -n monitoring prometheus-operated 

#make it to nodeport and Remove these lines:

clusterIP: None
clusterIPs:
  - None


  285  cat /tmp/kubectl-edit-64500117.yaml
  286  k replace --force -f /tmp/kubectl-edit-64500117.yaml
  287  clear
  288  k get svc -n monitoring


-- browse 56.125.5.201:31585 for promethus-operated svc exposition..

-- in prom ql query in prometheus search for query : 
kube_pod_container_status_running                                                                                                              ( check for the pods running)
100 * (1 - avg(rate(node_cpu_seconds_total{mode="idle", instance="172.31.27.229:9100"}[5m])))               ( check the nodes cpu )   

k edit svc -n monitoring prometheus-grafana 
  300  k get svc -n monitoring

-- expose grafana dashboard ....
username : admin
password : prom-operator
-- 
kubectl get secret -n monitoring prometheus-grafana -o jsonpath="{.data.admin-password}" | base64 --decode





-- more fam dashboards for kubernetes :

https://github.com/dotdc/grafana-dashboards-kubernetes?tab=readme-ov-file#install-via-grafanacom

https://0xdc.me/blog/a-set-of-modern-grafana-dashboards-for-kubernetes/






















---- try creating an alert :

add the dashoard for view nodes : 15759 ignore if already added


go to dashobards >> Kubernetes / Views / Nodes >> cpu w2 ... >> more >>new alert rule


set time range in A section to 5 min 

-- change the prom ql query which tracks % cpu on node 

remove section B and make C s input as B >> click preview to test

keep pending period to 1m


we can use this query to convert cpu seconds into % utilization while creatingalert :

100 * (1 - avg(rate(node_cpu_seconds_total{mode="idle", instance="172.31.37.208:9100"}[5m]))) 





=================

notification : goto test_grafana teams >> add channel


go to test_grafana team >> more apps >> search for incoming webhook ,..
configure and copy paste the webhook url to grafana and test
===========


now attach rult to notif channel :

-- go to notificationpolicies under alerting :

labels : teams = kube (wtever u like u can write) 

-- now go to alerting >> in 4. Configure labels and notifications >> mention teams=kube and than do preview 


==========================================================================================


root@master:~# cat /tmp/kubectl-edit-1444436957.yaml
# Please edit the object below. Lines beginning with a '#' will be ignored,
# and an empty file will abort the edit. If an error occurs while saving this file will be
# reopened with the relevant failures.
#
# services "prometheus-operated" was not valid:
# * spec.clusterIPs[0]: Invalid value: "None": may not be set to 'None' for NodePort services
#
apiVersion: v1
kind: Service
metadata:
  creationTimestamp: "2025-05-23T10:00:21Z"
  labels:
    operated-prometheus: "true"
  name: prometheus-operated
  namespace: monitoring
  ownerReferences:
  - apiVersion: monitoring.coreos.com/v1
    kind: Prometheus
    name: prometheus-kube-prometheus-prometheus
    uid: a3947c10-807b-4041-abd3-4680a9cbb746
  resourceVersion: "196095"
  uid: 2a5cac11-e902-4c8e-a8d1-5ef7699495fc
spec:
  internalTrafficPolicy: Cluster
  ipFamilies:
  - IPv4
  ipFamilyPolicy: SingleStack
  ports:
  - name: http-web
    port: 9090
    protocol: TCP
    targetPort: http-web
  selector:
    app.kubernetes.io/name: prometheus
  sessionAffinity: None
  type: NodePort
status:
  loadBalancer: {}
  
  ===============

```
