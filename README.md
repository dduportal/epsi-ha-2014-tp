Tp HA EPSI Lyon 2014
===============

Pré-requis
----------


* Vagrant : 
  * Description : Outil Open-Source, gratuit et multi-plateforme, pour configurer, partager et utiliser des VMs de tous types, via une simple CLI et un fichier texte.
  * URL : http://www.vagrantup.com/
  * Contraintes : visez la version 1.5.4 au moins, dans l'idéal la dernière version récente.
* VirtualBox : 
  * Description : Moteur de virtualisation géré par Oracle, existant en version Open Source. Moins performant que VMWare ou Hyper-V, mais amplement suiffsisant et surtout gratuit + multi-plateforme !
  * URL : https://www.virtualbox.org/
  * Contraintes : visez la dernière version stable de la branche 4.3.x.
* Git :
  * Description : SCM décentralisé popularisé par le site Github et les dévelopeurs du kernel Linux, il est 100 % open-sourc,e gratuit, et multi-plateforme.
  * URL : http://git-scm.com/
  * Contraintes : utilisez impérativement une version >= 1.9.0


Précautions
-----------

Sous Windows
************

* Attention à l'installation de Git-SCM :
  * Ajoutez bien les binaires Unix dans votre PATH Windows, quitte à rempalcer les commandes existantes comme "find"
  * Veillez à bien configurer les projets pour commiter en "Unix-style" (retours chariots \n, sans \r)
* Vérifiez que les ajouts à votre PATH soient bien au niveau "système" et non au niveau "utilisateur"
* Test pour les binaires Git à effectuer :
```
> ssh -V
OpenSSH_...
```

Sous MacOS
**********
* Je vous recommande d'utiliser homebrew ( http://brew.sh/ ) pour installer Git.
* Attention à bien ajouter "/usr/local/bin" dans votre PATH


Vérification de fonctionnement (toutes plateformes)
***************************************************
* Pour commencer, il est important d'installer les différents outils, et de vérifier que les PATH de vos outils en ligne de commande puissent bien les utiliser. Ainsi, validez les retours sans erreurs dans vos terminaux respectifs, des commandes suivantes :
```
> git --version
...
> VBoxManage -v
...
> vagrant -v
```

Que faire ?
-----------

L'objectif est de pouvoir lancer la VM vagrant présente dans ce dépôt.
* Pour commencer, il faut "cloner" le dépôt git :
```
> cd <VOTRE REPERTOIRE DE TRAVAIL>
> git clone https://github.com/dduportal/epsi-ha-2014-tp
[...]
> cd epsi-ha-2014-tp
```
* Ensuite, on démarre la VM (avec configuration automatique) :
```
> vagrant up
...
```
* La VM a démarré, on s'y connecte en SSH et on télécharge une image ubuntu de base pour docker :
```
> vagrant ssh
[...]
```
