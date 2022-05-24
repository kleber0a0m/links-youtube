
# Como hospedar um site em sua rede LAN local e instalar o LAMP no Ubuntu Server

#### Vídeo:
  [![Foo](https://raw.githubusercontent.com/kleber0a0m/links-youtube/main/imagens/znqwoyts.png)](https://youtu.be/biGSfoglrJ8)
# Comandos

## Instalação do Apache e Atualização do Firewall
```
sudo apt update
```
```
sudo apt install apache2
```
#### Ajustar o Firewall para Permitir Tráfego Web
```
sudo ufw app list
```
```
sudo ufw app info "Apache Full"
```
```
sudo ufw allow in "Apache Full"
```
## Instalação do MySQL
```
sudo apt install mysql-server
```
## Instalação do PHP
```
sudo apt install php libapache2-mod-php php-mysql
```
```
sudo systemctl restart apache2
```
```
sudo systemctl restart apache2
```
## Testando o Processamento PHP no seu Servidor Web
```
sudo nano /var/www/html/info.php
```
```
<?php
phpinfo();
?>
```


##### [Saiba mais](https://www.digitalocean.com/community/tutorials/como-instalar-a-pilha-linux-apache-mysql-php-lamp-no-ubuntu-18-04-pt)
