Linux:

    kubectl
        https://kubernetes.io/pt-br/docs/tasks/tools/install-kubectl-linux/

        Baixar:
            curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
        
        Instalar:
            sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

        Verificar:
            kubectl version --client

    virtualbox:
        https://www.virtualbox.org/wiki/Downloads    

    minikube:
        https://minikube.sigs.k8s.io/docs/start/?arch=%2Flinux%2Fx86-64%2Fstable%2Fbinary+download

        Baixar:
            curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

        Instalar:
            sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

    