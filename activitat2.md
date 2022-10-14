# INSTAL·LACIÓ OWNCLOUD

## GUIA D'INSTAL·LACIÓ:

### Requeriments:

Apache guarda els fitxers a /var/www/html/index.html




### Instal·lació Apache:

Primer instal·larem el servidor apache2,  
```
sudo apt install apache2
``` 
![image](https://user-images.githubusercontent.com/114162276/193051859-7183fa9d-60d3-4589-9db1-35c3f4d5920d.png)

Desactivem el llistat de directoris del servidor
``` 
sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf
```
![image](https://user-images.githubusercontent.com/114162276/193052841-762c07f8-a820-488d-9852-c6335c7022d2.png)

### Instal·lació MariaDB:

Ara instal·larem MariaDB
``` 
sudo apt-get install mariadb-server mariadb-client -y
```
![image](https://user-images.githubusercontent.com/114162276/193053539-2ab81ddb-6994-4e45-a010-4c1256e29931.png)

Configurem l'instal·lació
``` 
sudo mysql_secure_installation
```
![image](https://user-images.githubusercontent.com/114162276/193054185-d0026f1f-7d4a-498b-a129-84f903e12d52.png)

-Ens apareixeran algunes preguntes sobre la configuració:

La primera ens pregunta si volem canvia la contrasenya de root, en el meu cas he dit que no

![image](https://user-images.githubusercontent.com/114162276/193055901-67325471-f961-441b-a4a5-8f31a000157a.png)

Apartir d'aqui ho deixem per defecte

![image](https://user-images.githubusercontent.com/114162276/193056460-ffd86a0a-a0c4-44dc-9b5e-98f2b5d9ee1a.png)

![image](https://user-images.githubusercontent.com/114162276/193056622-252964c3-0d17-4e71-a153-205dded19d6a.png)

![image](https://user-images.githubusercontent.com/114162276/193056696-032bf200-1522-45ed-a323-7beb8536b433.png)

![image](https://user-images.githubusercontent.com/114162276/193056759-42a07753-1eb6-4d76-8e2a-7d30b03426d2.png)

Per ultim reiniciem el servidor MariaDB
``` 
sudo systemctl restart mariadb.service` o `sudo service mariadb.service restart

```
![image](https://user-images.githubusercontent.com/114162276/193057371-5693cc58-1d32-444b-9426-126c3d590932.png)

### Crea la base de dades de Owncloud:

Entrem a MariaDB
``` 
sudo mysql -u root -p

```
![image](https://user-images.githubusercontent.com/114162276/193058491-0964049d-4dbd-471a-bf72-214a66a263f7.png)

Creem la base de dades
``` 
CREATE DATABASE owncloud;
```
![image](https://user-images.githubusercontent.com/114162276/193059063-606c3313-5396-4dd7-9a7c-3584214eae88.png)

Creem un usuari que es dira **ownclouduser** amb una contrasenya, per exemple **Admin1234**
``` 
CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';

```
![image](https://user-images.githubusercontent.com/114162276/193059746-d776374b-28a6-43d5-a228-539d99ec3983.png)

Li donem accés a l'usuari a la base de dades que hem creat
``` 
GRANT ALL ON owncloud.* TO 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234' WITH GRANT OPTION;
```
![image](https://user-images.githubusercontent.com/114162276/193060087-22bf7bd7-8a43-4122-ad7a-5e43918bd69a.png)

Apliquem els canvis i guardem
``` 
FLUSH PRIVILEGES;
EXIT;
```
![image](https://user-images.githubusercontent.com/114162276/193060420-0bec8a4a-1367-488f-ba89-d81a1cb35811.png)

### Instal·lació PHP i els seus moduls necessaris:

Instal·lem el PHP i creem un repository per a ell
``` 
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:ondrej/php

```
![image](https://user-images.githubusercontent.com/114162276/193062168-fac83f67-b6c5-48f9-bebe-6b7dfd600281.png)

Actualitzem els paquets afegits
``` 
sudo apt update
```
![image](https://user-images.githubusercontent.com/114162276/193062589-67286fd5-7590-40f0-be44-6f3542267107.png)

Instal·lem el PHP i els seus moduls necessaris
``` 
sudo apt install php7.4 libapache2-mod-php7.4 php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-apcu php7.4-smbclient php7.4-ldap php7.4-redis php7.4-gd php7.4-xml php7.4-intl php7.4-json php7.4-imagick php7.4-mysql php7.4-cli php7.4-mcrypt php7.4-ldap php7.4-zip php7.4-curl -y
```
![image](https://user-images.githubusercontent.com/114162276/193063242-9f4ff3f6-3a59-4fea-b226-c700806bb8bd.png)

Ara editem el fitxer **php.ini** i canviem algunes coses
El podem obri amb **nano** i s'obrira al terminal o amb **gedit** i s'obrira a un bloc de notes
``` 
sudo nano /etc/php/7.4/apache2/php.ini
```
![image](https://user-images.githubusercontent.com/114162276/193064158-54c39484-7d15-442f-a497-02432053b7d0.png)

Els valors que hem de canvia son els següents:
**file_uploads = On allow_url_fopen = On memory_limit = 256M upload_max_filesize = 100M display_errors = Off date.timezone = Europe/Madrid**

![image](https://user-images.githubusercontent.com/114162276/193064739-71f6c78d-aeab-42e6-943f-e1328e83a2b8.png)

![image](https://user-images.githubusercontent.com/114162276/193064987-56b8fe59-e1c0-4171-be1f-4b51f8b1ae1e.png)

![image](https://user-images.githubusercontent.com/114162276/193065132-eeed8f8d-f924-43a0-a1fc-5d345d7458f0.png)

![image](https://user-images.githubusercontent.com/114162276/193065270-78d601b6-b6d8-4c33-957e-214600e095c2.png)

![image](https://user-images.githubusercontent.com/114162276/193066569-3f560bbc-fb8a-4dd1-ab74-f11410a853b4.png)

Quan hem acabat guardem

### Instal·lem Owncloud:

Descarguem l'ultima versio del programa, descomprimim els fitxers i els movem a de Owncloud a /var/www/html/owncloud.
``` 
cd /tmp && wget https://download.owncloud.com/server/stable/owncloud-complete-latest.zip
unzip owncloud-10.0.8.zip
sudo mv owncloud /var/www/html/owncloud/

```
![image](https://user-images.githubusercontent.com/114162276/193067653-596691f7-a861-4b88-9d8a-2a46c51b9ce9.png)

![image](https://user-images.githubusercontent.com/114162276/193067730-78dd00f8-0545-4bae-8582-3ab8a113d5b9.png)

![image](https://user-images.githubusercontent.com/114162276/193067839-91ba07a8-b0d2-4cf3-a06d-2e0a8fb9d23a.png)

Canviem el propietari i els permisos dels directoris de Owncloud, **www-data** per a que ho pugue utilitzar Apache i li posem 755 per a que qualsevol usuari de Linux pugui executar i llegir
``` 
sudo chown -R www-data:www-data /var/www/html/owncloud/
sudo chmod -R 755 /var/www/html/owncloud/
```
![image](https://user-images.githubusercontent.com/114162276/193068703-7b1541bc-60c0-42db-ada2-4f0032bb1dc0.png)

![image](https://user-images.githubusercontent.com/114162276/193068795-385a69ab-fdc4-49f3-8f40-1b1f8507d050.png)

Ara canviarem el domini de la nostra pagina web sense utilitzar el DNS, utilitzarem la comanda nano o gedit /etc/hosts
```
sudo gedit /etc/hosts
```
![image](https://user-images.githubusercontent.com/114162276/194344192-e4bd13eb-8eb9-4f30-93ac-c37ecae6f992.png)

### Configuració Apache:

Per a configurar l'Apache utilitzarem aquesta comanda per accedir a l'arxiu de configuració
```
sudo nano /etc/apache2/sites-available/owncloud.conf
```
![image](https://user-images.githubusercontent.com/114162276/195611403-a4e6b4bf-00b0-47dc-bb27-87891096f3d8.png)

- Virtualhost *:80 : aixo vol dir que el servidor contestara amb qualsevol ip, pel port 80
- ServerAdmin: aqui estar el correu de l'administrador del servidor
- DocumentRoot: es la ruta per defecte
- ServerName: aqui va el nom del nostre servidor
- ServerAlias: es un altre nom per al servidor que tambe podem utilitzar per a buscar-lo a internet 

- Alias: 

- Directory: tota la configuracio que esta dins del directori s'aplica a aquest


Habilitem el owncloud i el modul rewrite
```
sudo a2ensite owncloud.conf
sudo a2enmod rewrite
sudo a2enmod headers
sudo a2enmod env
sudo a2enmod dir
sudo a2enmod mime
```
Reiniciem apache
```
sudo service Apache2 restart
```
Ara ja podem accedir a owncloud posan el nom del servidor al buscado

 



