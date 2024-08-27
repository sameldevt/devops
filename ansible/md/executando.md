Criar arquivos hosts.yml e playbook.yml:

![alt text](image.png)

Configurar Host e Tarefas:

Host:
![alt text](image-1.png)

Tarefas:
![alt text](image-2.png)

Executando:

ansible-playbook playbook.yml -u ubuntu --private-key ../terra-form/iac-alura.pem -i hosts.yml

playbook.yml    -> arquivo de tarefas
-u              -> usuario da instancia na AWS
--private-key   -> chave .pem
-i              -> arquivo de hosts

![alt text](image-3.png)