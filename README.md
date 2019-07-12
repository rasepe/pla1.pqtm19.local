# Configuració entorn de desenvolupament web

## Introducció


## Índex
1. [Instal·lació Xampp](#1-installació-de-xampp)
2. [Configuració Virtual Host d’Apache](#2-configuració-de-virtualhost-dapache)
3. [Instal·lació de Eclipse](#3-installació-de-eclipse)
4. [Definició de WorkSpace](#4-definició-de-workspace)
5. [Definició de projecte](#5-definició-de-projecte)
6. [Definició del repositori local](#6-definició-del-repositori-local)
7. [Creació de Repositori de GitHub](#7-creació-de-repositori-de-github)
8. [Exportació de la branca “master” local sobre repositori GitHub](#8-exportació-de-la-branca-master-local-sobre-repositori-github)


## 1. Instal·lació de XAMPP

* Anem a la web [https://www.apachefriends.org](https://www.apachefriends.org) i descarreguem la versió de XAMPP que correspongui:
![](media/Install_Xampp/1_Install_Xampp.PNG)


* Descarreguem i obrim el fitxer:
![](media/Install_Xampp/2_Install_Xampp.PNG)


* Ens sortirà un avís, fem OK i s'iniciarà l'assistent d'instal·lació:
![](media/Install_Xampp/3_Install_Xampp.PNG)
![](media/Install_Xampp/4_Install_Xampp.PNG)


* Seleccionem els components que volem instal·lar:
![](media/Install_Xampp/5_Install_Xampp.PNG)


* Seleccionem la carpeta on volem instal·lar XAMPP i anem fent "Next" fins que finalitzi la instal·lació:
![](media/Install_Xampp/6_Install_Xampp.PNG)
![](media/Install_Xampp/7_Install_Xampp.PNG)
![](media/Install_Xampp/8_Install_Xampp.PNG)
![](media/Install_Xampp/9_Install_Xampp.PNG)
![](media/Install_Xampp/10_Install_Xampp.PNG)


* Seleccionem idioma:
![](media/Install_Xampp/11_Install_Xampp.PNG)


* Arrenquem els servidors Apache i MySQL:
![](media/Install_Xampp/12_Install_Xampp.PNG)
![](media/Install_Xampp/13_Install_Xampp.PNG)

* Si tot ha anat bé, si introduïm *localhost* al navegador hauríem de visualitzar aquesta pantalla:
![](media/Install_Xampp/14_Install_Xampp.PNG)

## 2. Configuració de VirtualHost d’Apache

* Primer de tot creem la carpeta del projecte:
![](media/Captura001.PNG)


* Editem el fitxer **httpd-vhosts.conf**, que es troba a la carpeta C:\xampp\apache\conf\extra. 


* Anem sota la línia:

```
NameVirtualHost *:80
```
> El codi que hem d'introduir per crear un *VirtualHost* al directori C:/PQTM19/Projectes/pla1.pqtm19.local és:


```
<VirtualHost *:80>

	ServerAdmin webmaster@pqtm19.local
	DocumentRoot "C:/PQTM19/Projectes/pla1.pqtm19.local"
	ServerName pla1.pqtm19.local
	ErrorLog "logs/pla1.pqtm19.local-error.log"
	CustomLog "logs/pla1.pqtm19.local-access.log" common
	<Directory "C:/PQTM19/Projectes/pla1.pqtm19.local">
		DirectoryIndex index.php index.html index.html
		Options Indexes FollowSymLinks Includes ExecCGI
		AllowOverride All
		Order allow,deny
		Allow from all
		Require all granted
	</Directory>
</VirtualHost>
```
> En la següent captura ressaltem les línies de codi que fan referència a la carpeta del projecte. Cada *Virtualhost* tindrà el seu propi bloc de codi que és idèntic tret de la referència a la carpeta. Per tant, aquesta és l'única part del codi que haurem d'adaptar cada cop que afegim un nou *Virtualhost*.
![](media/Captura002.PNG)

* A continuació, editem el fixer **hosts** situat a la carpeta C:\Windows\System32\drivers\etc :
![](media/Captura003.PNG)
![](media/Captura004.PNG)
![](media/Captura005.PNG)
![](media/Captura006.PNG)
![](media/Captura007.PNG)
![](media/Captura008.PNG)
![](media/Captura009.PNG)
![](media/Captura010.PNG)


## 3. Instal·lació de Eclipse
## 4. Definició de WorkSpace
Descripció de WorkSpace i com es defineix
## 5. Definició de projecte
Descripció pas a pas amb captura de pantalles de com es defineix un projecte dintre d’eclipse.
## 6. Definició del repositori local
Descripció pas a pas amb captures de pantalla de com es defineix un repositori local des de
Eclipse sobre el projecte actual
## 7. Creació de Repositori de GitHub
Descripció pas a pas amb captures de pantalles de com es defineix un repositori dintre de
l’entorn GitHub
## 8. Exportació de la branca “master” local sobre repositori GitHub
Descripció pas a pas amb captures de pantalla de com es replica el repositori local d’Eclipse
sobre la branca “master ” del repositori creat dins de Github