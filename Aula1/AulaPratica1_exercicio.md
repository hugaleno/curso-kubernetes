1. Criar um namespace "exercicio" de forma imperativa
2. Criar um pod com o nome "pod-apache" baseado na imagem do apache no namespace "exercicio" de forma declarativa
3. Utilizar a ferramenta de describe do kubernetes pra obter detalhes do pod recém criado
4. Criar um novo pod com o nome "pod-apache-2" no namespace "exercicio".
5. Logar no pod "pod-apache" e verificar se o serviço está escutando na porta 80 com o comando curl
5.1  Instalar o curl dentro do container
    apt-get update && apt-get install curl
6. Tentar acessar o outro pod(pod-apache-2) na porta 80 utilizando o comando curl
7. Definir um liveness probe do tipo http para o container "pod-apache"
