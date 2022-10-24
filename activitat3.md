# Activitat 3:

Per fer aquesta activitat comptem amb que **ja s'ha configurat el servei Owncloud a una Màquina Virtual** (MV).

**3.1.-** Llista els Virtual Hosts d'Apache per tal de veure si **owncloud.XYZ.com** està habilitat amb la comanda:

```
apache2ctl -S
``` 

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/196968870-df6af995-405e-4dcb-8c88-42084d65becd.png)


**3.2.-** A Owncloud podem veure que hi ha una serie de carpetes per defecte, mostra la ruta real a les tres carpetes dins de la teva MV.

![image](https://user-images.githubusercontent.com/110727546/194824543-c49bf482-ac93-432f-884c-d89487e587f3.png)

**RESPOSTA**

La ruta real és: /var/www/html/owncloud/data/ownclouduser/files

**3.3.-** Al directori **Learn more about owncloud** hi ha informació en forma de fitxers pdf. Consulta'ls i respon aquestes preguntes:

- Quin són els tres tipus de protecció de dades que ofereix Owncloud?

   - 1-  Encryption in Transit
   - 2a- Encryption at Rest
   - 2b- Encryption at Rest with Master Key in Hardware Security Module (HSM)
   - 3-  End-to-End Encryption

- Fes una petita descripció de cada un d'ells.
   - 1- Encryption in Transit:
      L'encriptació en trànsit és obligatòria sota el GPDR per a la protecció de dades.
   - 2a- Encryption at Rest: 
      L'encriptatge en repòs significa encriptar tots els fitxers desat des del servidor d'aplicacions             owncloud abans de desar-los a l'emmagatzematge real.
   - 2b- Encryption at Rest with Master Key in Hardware Security Module (HSM):
      Per tal d'excloure l'administrador del sistema de la capacitat de desxifrar fitxers, ownCloud permet         posar la clau maestra en un HSM.
      Un HSM o un mòdul de seguretat de maquinari, que assegura que la clau mestra només reacciona
      a petició de l'aplicació ownCloud.
   - 3- End-to-End Encryption: 
      Si es perd la clau privada, les dades no es poden desxifrar d'una altra manera owncloud proporciona un       extrem a extrem.
      Quan el connector està habilitat per a un usuari, aquest usuari pot xifrar qualsevol carpeta buida. 

- Per quina raó ens recomana utilitzar Owncloud per als documents de Microsoft Office de la nostra empresa?  

      Perquè emmagatzema les dades al núvol i alli estan segures, també el Tribunal de Justícia de les             Comunitats Europees ha derrocat l'anomenat "Escut de la privacitat" en 2020, cosa que significa que ja       no existeix cap base legal per a transferir dades als Estats Units.

- Això passa a tots els països?
- Quina és la llicència d'OWncloud Enterprise?
- I la d'Owncloud Standard?
- Es poden veure videos en Streaming directament des de Owncloud?
- Es poden connectar directoris de Google Drive a Owncloud?
- I Dropbox?
- Compta Owncloud amb antivirus? En cas afirmatiu com es diu? 

**RESPOSTA**

**3.4.-** Mostra els següents canvis de paràmetres d'usuari:

- Posa't una imatge d'usuari.

![image](https://user-images.githubusercontent.com/114162276/196980811-459c4b88-1796-4505-ac0d-15b8919966fb.png)

Aixi quedaria la foto de perfil

![image](https://user-images.githubusercontent.com/114162276/196981802-dc3ffd1a-457e-4a91-bdcb-baf6d3eda2de.png)

- Afegeix el teu mail de l'Institut.

![image](https://user-images.githubusercontent.com/114162276/196982500-d6751efc-526f-476b-a4ab-158913bfba88.png)

- Canvia l'idioma a català.

![image](https://user-images.githubusercontent.com/114162276/196982366-d49f7cd2-816f-4073-bc25-388ea5b9c29f.png)

- Mostra la versió d'Owncloud instal·lada.

![image](https://user-images.githubusercontent.com/114162276/196982012-0a0fbb6e-84d7-4ca7-b16a-1fa622b5f0f6.png)


