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

**4.8.-** Crea un usuari anomenat usuari2XYZ i fical al grup usuaris.

**RESPOSTA**

![image](https://user-images.githubusercontent.com/114162276/199023258-bef54e29-25fe-485d-b7d9-d73db2cbf168.png)

![image](https://user-images.githubusercontent.com/114162276/199023368-96f27096-bd7f-4f1d-95fd-f7c21c8bfee4.png)

**4.9.-** Comparteix un fitxer de usuariXYZ a usuari2XYZ i mostra com l'usuari2XYZ pot veure i descarregar el fitxer.

**RESPOSTA**

**4.10.-** Esborra la carpeta Learn more about owncloud.

**RESPOSTA**

**4.11.-** Recupera la carpeta Learn more about owncloud.

**RESPOSTA**

**4.12.-** Com a usuariXYZ crea una carpeta nova anomenada shared i comparteix-la amb l'usuari usuari2XYZ.

**RESPOSTA**

**4.13.-** Entra a Market instal·la dues aplicacions que no estiguin ja instal·lades i explica què fan i com funcionen.

![image](https://user-images.githubusercontent.com/110727546/196159706-705ff624-c409-4632-acb4-f43ffcc486d4.png)

**RESPOSTA PRIMERA APP**

**RESPOSTA SEGONA APP**

**4.14.-** Crearem una carpeta nova per emmagatzematge a Owncloud, la carpeta serà /media/publicXYZ on XYZ són les teves inicials i apareixerà amb el nom de public als usuaris.

Aquesta carpeta haurà de pertànyer a l'usuari www-data.

**RESPOSTA**

**4.15.-** Connectarem la carpeta publicXYZ com emmagatzematge local, tal i com s'indica [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/local.html). Tots els usuaris tindran accés a la carpeta.

**RESPOSTA**

**4.16.-** Un usuari normal pujarà un fitxer a la carpeta public.

**RESPOSTA**

**OPCIONAL.-** Aquesta tasca és opcional.

Intenta connectar com a emmagatzematge extern el teu compte de Google Drive de l'Institut. Tens com fer-ho [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/google.html).

**RESPOSTA**
