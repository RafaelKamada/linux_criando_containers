# Linux criando containers com docker

Desafio de projeto para configurar um ambiente com mysql e php utilizando Docker.

Curso: Utilização prática no cenário de Microsserviços - [Denilson Bonatti](https://github.com/denilsonbonatti), Instrutor - Digital Innovation One



## Requisitos
1 - Uma VM Linux.

2 - Docker instalado.
  
  
## Procedimentos:
Na sua VM do linux copiar os arquivos abaixo para o diretório de sua preferência:
 - [index.php](https://github.com/RafaelKamada/linux_criando_containers/blob/main/index.php)
 - [docker-compose.yml](https://github.com/RafaelKamada/linux_criando_containers/blob/main/docker-compose.yml)

Executar o seguinte comando docker para inicialização dos containers:

```sh
docker-compose up --build
```

Abrir outro terminal e conectar no container de mysql

```sh
docker exec -it database bash
```

Conectar-se no banco mysql dentro desse container:
```sh
mysql -uroot -p
```

A senha para acessar o banco de dados é 'root', a mesma foi configurada no arquivo [docker-compose.yml](https://github.com/RafaelKamada/linux_criando_containers/blob/main/docker-compose.yml)
![alt text](https://github.com/RafaelKamada/linux_criando_containers/blob/main/images/docker-compose.png)


Após acessa-lo, criar a tabela "dados" utilizando o script: [configuracaoBanco.sql](https://github.com/RafaelKamada/linux_criando_containers/blob/main/configuracaoBanco.sql)

![alt text](https://github.com/RafaelKamada/linux_criando_containers/blob/main/images/mysql.png)


Após isso é só executar seu navegador na url de (http://localhost) e ir dando refresh com F5 na página e verificando se está sendo inserido novos registros na tabela do mysql. 

![alt text](https://github.com/RafaelKamada/linux_criando_containers/blob/main/images/navegador.png)
