Linux

minikube start --vm-driver=virtualbox

criando um pod modo imperativo:
    
$ kubeclt run {nome-do-pod} {imagem-base-do-container}:

$ kubectl run nginx-pod --image=nginx:latest

![alt text](image.png)

ver lista de pods:

$ kubectl get pods:

ver lista de pods com mais informações:

$ kubectl get pods -o wide

![alt text](image-5.png)

ver lista e assistir mudanças:

$ kubectl get pods --watch;

![alt text](image-2.png)

ver informações sobre um pod:

$ kubectl describe pod {nome-do-pod}

$ kubectl describe pod nginx-pod

apagar pods e services:

![alt text](image-15.png)

editar um pod:

$ kubectl edit pod {nome-do-pod}

$ kubectl edit pod nginx-pod

criando um pod modo declarativo:

criar um arquivo .yaml:

![alt text](image-4.png)

apiVersion   => versão da api do kubernetes;
kind         => o que vamos criar;
metadata     => informações sobre o pod;
  name       => nome do pod;
spec         => especificações do pod;
  containers => lista de containers do pod; 
    - name   => nome do container
      image  => imagem em que o container ira se basear

$ kubectl apply -f {nome-do-arquivo-yaml}

$ kubectl apply -f primeiro-pod.yaml

deletar um pod

$ kubectl delete pod {nome-do-pod}

$ kubectl delete pod nginx-pod

deletar um pod declarativo:

$ kubectl delete -f {arquivo-de-configuracao}

$ kubectl delete -f primeiro-pod.yaml


acessando um pod:

$ kubectl exec -it {nome-do-pod} -- bash => abre no modo interativo usando o bash

$ kubectl exec -it portal-noticias -- bash

![alt text](image-3.png)

usando serviços:

![alt text](image-6.png)

![alt text](image-7.png)

ClusterIP => serve para fazer a comunicação interna entre diferentes pods em um mesmo cluster.

criando um serviço do tipo ClusterIP

![alt text](image-8.png)

selector => para qual pod esse serviço ira servir
  app    => nome do pod

ports    => com quais portas o serviço irá trabalhar
  port   => porta de recebimento do serviço
  tartgetPort => porta de despache (a porta do pod na qual o serviço esta servindo)

  * como alternativa, pode-se usar no parametro - port: o mesmo valor. por exemplo - port: 80 => essa declaração irá usar a porta 80 tanto para entra quanto para saída dos redirecionamentos

![alt text](image-9.png)

NodePort => permite a comunicação para o mundo externo:

* funciona também como um clusterip

![alt text](image-10.png)

como criar:

![alt text](image-11.png)

![alt text](image-12.png)

utilizamos o ip do node para acessar o serviço fora do cluster

LoadBalancer => 

![alt text](image-13.png)

como criar:

![alt text](image-14.png)