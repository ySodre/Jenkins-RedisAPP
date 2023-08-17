#Aplicação simples utilizando node.js e redis
1. Crie uma rede especifica para o projeto
    #docker network create devops
2. Faça a criação da imagem com o docker build
    #docker build -t devops/node-app . 
3. Inicie o redis antes da aplicação
    #docker run --net devops -d redis-server redis
4. Inicie o o container da aplicação
    #docker run --net devops -p 8080:8081 devops/node-app