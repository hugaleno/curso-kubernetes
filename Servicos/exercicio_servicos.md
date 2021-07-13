1. Criar namespace chamado exercicio2
2. Criar um pod a partir da seguinte imagem disponível no docker hub: hugaleno/kub-firstapp
- A aplicação rodando nessa imagem escuta na porta 8080

3. Entrar no container e verificar se a aplicação está respondendo na porta 8080 com o comando curl
4. Criar um serviço para expor a aplicação para o mundo externo
5. Expor a porta pelo minikube(Passo requerido apenas nesse ambiente de teste)
- minikube service nome_do_servico -n nome_namespace
6. Acesse a aplicação no web browser. Faça o que se pede na página e veja o resultado no terminal
7. Crie um ingresso para acessar a aplicação pela url: primeiroapp.info
- Edite o arquivo de hosts da sua máquina para adicionar a nova url e o endereço criado pelo kubernetes
- Descubra o IP do ingresso
- Linux: 
    sudo -i
    echo "IP_DO_INGRESSO primeiroapp.info" >> /etc/hosts
- Windows:
    https://king.host/wiki/artigo/como-editar-o-arquivo-hosts-no-windows/

8. Crie um novo pod utilizando a versão nova: hugaleno/kub-firstapp:v2
9. Criar um serviço do tipo ClusterIP para o novo pod
10. Adicionar um redirecionamento do caminho /v2 para o novo pod com a nova versão
11. Testar no browser o redirecionamento