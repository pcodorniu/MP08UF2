# Activitat 4:

## Gestió d'usuaris:

Hi ha dos tipus d'usuaris, els admins amb permissos per gestionar Owncloud i els usuaris normals.

On fica resposta afegeix una captura de pantalla on es vegi que has fet l'acció que es demana.

**Aquesta part de la pràctica la feu amb un company/a, li creeu un usuari i li doneu el vostre nom de domini d'Owncloud.**

Per a que pugui accedir necessitarà:

- La MV amb owncloud ha d'estar en mode "adaptador pont".
- El fitxer /etc/hosts del company ha de tenir la IP de la MV i el nom de domini de la MV del company/a.


**4.1.-** Crea un usuari admin que es digui adminXYZ, on XYZ són les inicials del teu nom:

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/198641161-ef146986-9048-4d1d-8354-d58d9b3f6e85.png)

![image](https://user-images.githubusercontent.com/114162276/198641985-91851f8c-c6a5-4274-bb70-7efac04ba501.png)

**4.2.-** Inicia sessió com a l'usuari adminXYZ.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/198645496-3b9efe26-548e-4f1d-b968-49020a1d25ce.png)

**4.3.-** Crea un usuari XYZ on XYZ son les inicials del company/a i afegeix-lo al grup usuaris, aquest usuari tindrà una quota de 512 MB.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/198653807-bc41bc06-9155-4d67-9000-75258483ae46.png)

![image](https://user-images.githubusercontent.com/114162276/198654360-101d6000-4620-460b-860e-798c48e0c25c.png)

**4.4.-** Podem crear fitxers d'una mida determinada a Linux amb la comanda:

```
truncate -s 10M file.txt
```

A l'exemple es crea un fitxer de 10MB.

Crea 6 fitxers de 100MB i pujal's a Owncloud un per un.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/198659829-43f76b7d-5d51-4396-b6f0-d72eb77b7fea.png)

**4.5.-** Mostra el missatge d'error per haver superat la quota d'usuari.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/198669661-e7723bb4-4781-4011-9c4d-512607193427.png)

**4.6.-** Busca al teu perfil quin percentatge de quota estas utilitzant.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199021836-8cc21040-c367-4d93-9501-fed65479a4a9.png)

**4.7.-** Canvia la quota de l'usuari a 1GB i mostra tots els fitxers pujats.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199021989-108ad510-d570-46ac-99bf-a8585dec9928.png)

![image](https://user-images.githubusercontent.com/114162276/199025295-af545bb9-bfbe-4106-a084-3d440129e032.png)

**4.8.-** Crea un usuari anomenat usuari2XYZ i fical al grup usuaris.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199023258-bef54e29-25fe-485d-b7d9-d73db2cbf168.png)

![image](https://user-images.githubusercontent.com/114162276/199023368-96f27096-bd7f-4f1d-95fd-f7c21c8bfee4.png)

**4.9.-** Comparteix un fitxer de usuariXYZ a usuari2XYZ i mostra com l'usuari2XYZ pot veure i descarregar el fitxer.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199025630-90cbc7c6-6f7f-4137-814e-fb6e193d81d3.png)

![image](https://user-images.githubusercontent.com/114162276/199025789-9222cc55-f679-407c-b0f8-917773c54b16.png)

![image](https://user-images.githubusercontent.com/114162276/199025931-1695fa00-2e7b-4124-99a3-f9f1bf469b28.png)

**4.10.-** Esborra la carpeta Learn more about owncloud.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199026190-94278b4a-5b1e-4042-b46b-c88d510f5467.png)

**4.11.-** Recupera la carpeta Learn more about owncloud.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199026394-e9125779-0f8d-4fff-8f26-a99f5622a7ae.png)

![image](https://user-images.githubusercontent.com/114162276/199026489-88065151-2d6c-45fd-90ed-41d069cb28cb.png)

**4.12.-** Com a usuariXYZ crea una carpeta nova anomenada shared i comparteix-la amb l'usuari usuari2XYZ.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199026634-caeec566-d375-4d13-b841-47112287c267.png)

![image](https://user-images.githubusercontent.com/114162276/199026795-6c32295c-3829-4204-b0a6-6a60d8d0c9c0.png)

**4.13.-** Entra a Market instal·la dues aplicacions que no estiguin ja instal·lades i explica què fan i com funcionen.

![image](https://user-images.githubusercontent.com/110727546/196159706-705ff624-c409-4632-acb4-f43ffcc486d4.png)

**RESPOSTA PRIMERA APP**

Instal·larem una app per a poder afegir contactes
![image](https://user-images.githubusercontent.com/114162276/199262038-e70c0f8f-759a-413a-b6d4-131feb4bbfc2.png)

Una vegada instal·lada ens apareixera a les tres ralles de d'alt a l'esquerra un  nou apartat que es dira contactes, entrem i alli podrem afegir els contactes que vulguem, hi ha diferents apartats que pots emplenar com per exemple el telefon, ciutat, codi postal, adreça, etc. 
![image](https://user-images.githubusercontent.com/114162276/199262187-83850431-36d7-4578-9117-eab2ec2049eb.png)

**RESPOSTA SEGONA APP**

La segona app que instal·larem sera un calendari
![image](https://user-images.githubusercontent.com/114162276/199262941-30dada06-0895-4dad-bad5-bac1c152086a.png)

Una vegada instal·lada ens apareixera a les tres ralles de d'alt a l'esquerra un nou apartat que es dira calendari, alli ens apareixera un calendari on podrem afegir esdeveniments.
![image](https://user-images.githubusercontent.com/114162276/199263071-30b136ed-d773-47ff-becd-444bd1814c86.png)

**4.14.-** Crearem una carpeta nova per emmagatzematge a Owncloud, la carpeta serà /media/publicXYZ on XYZ són les teves inicials i apareixerà amb el nom de public als usuaris.

Aquesta carpeta haurà de pertànyer a l'usuari www-data.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/200334821-ccea0574-0b0f-40d6-b39b-edb1fa0a9267.png)

![image](https://user-images.githubusercontent.com/114162276/200336069-87be10d0-b97b-4b18-a621-468f8447f6fa.png)

**4.15.-** Connectarem la carpeta publicXYZ com emmagatzematge local, tal i com s'indica [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/local.html). Tots els usuaris tindran accés a la carpeta.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/200338116-98e1c7a1-c365-418a-87c1-9d322ef83da9.png)

![image](https://user-images.githubusercontent.com/114162276/200338615-c40e1f2e-e135-449c-8346-256f05ca3ea1.png)

**4.16.-** Un usuari normal pujarà un fitxer a la carpeta public.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/200343943-3f143859-bf7f-459a-81dc-6fbefec794e2.png)

**OPCIONAL.-** Aquesta tasca és opcional.

Intenta connectar com a emmagatzematge extern el teu compte de Google Drive de l'Institut. Tens com fer-ho [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/google.html).

**RESPOSTA**
