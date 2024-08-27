Usando o terraform, copiar AMI ID na tela de criação de instancia:

![alt text](image-2.png)

No arquivo main.tf, adicionar o ami na tag resource:

![alt text](image-3.png)

Gerar par de chaves. Na barra lateral esquerda, buscar por Key Pairs:

![alt text](image-4.png)

Criar novo par de chave, baixar, adicionar nome da chave a tag resource:

![alt text](image-5.png)

Na barra lateral esquerda, clicar em Security Groups:

![alt text](image-8.png)

Nessa janela, escolher o grupo de segurança e adicionar regras de entrada e saída(Inbound rules, Outbound rules):

![alt text](image-9.png)

Regras de entrada:

Nova regra 1 -> Anywhere IPV4
Nova regra 2 -> Anywhere IPV6

Regras de saída:

Nova regra 1 -> Anywhere IPV4
Nova regra 2 -> Anywhere IPV6

Na aba instance, clicar em connect:

![alt text](image-6.png)

Seguir o tutorial:

![alt text](image-7.png)