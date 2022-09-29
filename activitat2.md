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






































