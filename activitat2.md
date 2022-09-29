# INSTAL·LACIÓ OWNCLOUD

## GUIA D'INSTAL·LACIÓ:

### Requeriments:

Apache guarda els fitxers a /var/www/html/index.html




### Instal·lació:

Primer instal·larem el servidor apache2, utilitzarem la comanda 
```
sudo apt install apache2
``` 
![image](https://user-images.githubusercontent.com/114162276/193051859-7183fa9d-60d3-4589-9db1-35c3f4d5920d.png)

Desactivem el llistat de directoris del servidor
``` 
sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf
```
![image](https://user-images.githubusercontent.com/114162276/193052841-762c07f8-a820-488d-9852-c6335c7022d2.png)

Ara instal·larem la base de dades MariaDB
``` 
sudo apt-get install mariadb-server mariadb-client -y
```
![image](https://user-images.githubusercontent.com/114162276/193053539-2ab81ddb-6994-4e45-a010-4c1256e29931.png)



