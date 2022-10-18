# example-flyway
Um projeto simples que implementa na prática o Flyway para gerenciar as migrações de banco de dados;

## Tecnologias
<div style="display: inline_block">
    <img align="center" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/java/java-original.svg">
    <img align="center" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/spring/spring-original.svg">
    <img align="center" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/docker/docker-original.svg">
    <img align="center" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original.svg">
    <img align="center" height="30" width="40" src="https://github.com/simple-icons/simple-icons/blob/master/icons/flyway.svg">
</div>

## DOCKER
* Primeiro, deverá ser criado um volume lógico do docker para manter os dados do sistema;
```
docker volume create flyway-mysql
```

* Em seguida, deverá ser executado o container, utilizando o volume criado como referência;
* O comando abaixo, executa o container docker na porta **3306** e com a senha de *root* = **123456**;
```
docker run -d --rm --name mysql-server -v flyway-mysql:/var/lib/mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_DATABASE=example-flyway mysql:8.0
```
