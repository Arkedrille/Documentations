# Créer une clé bootable avec Balena Etcher

Pour installer un OS sur un poste physique il faudra utiliser une clé bootable.



## Prérequis

Télécharger [Balena Etcher](https://www.balena.io/etcher/) puis valider le programme d'installation

![image-20201111150321246](C:\Users\Arkedrille\AppData\Roaming\Typora\typora-user-images\image-20201111150321246.png)

Télécharger également l'ISO de l'OS à installer (ici [Ubuntu Serveur 20.04.1 LTS](https://ubuntu.com/download/server))

Il faudra également une clé usb d'environ 4Go (8Go au mieux)



**Création de la clé bootable**

Exécuter Balena Etcher puis cliquer sur **Select image**, sélectionner l"ISO fraîchement téléchargé, finalement cliquer sur **Ouvrir**

![image-20201111151342300](C:\Users\Arkedrille\AppData\Roaming\Typora\typora-user-images\image-20201111151342300.png)

Cliquer sur **Change** sous l'icône de disque dur si la clé sélectionnée n'est pas la bonne puis cliquer sur **Continue**

![image-20201111151454355](C:\Users\Arkedrille\AppData\Roaming\Typora\typora-user-images\image-20201111151454355.png)

Cliquer sur **Flash** et valider l'autorisation Windows

![image-20201111151609936](C:\Users\Arkedrille\AppData\Roaming\Typora\typora-user-images\image-20201111151609936.png)

Une fois fini, Balena Etcher montre cette fenêtre

![image-20201111151727854](C:\Users\Arkedrille\AppData\Roaming\Typora\typora-user-images\image-20201111151727854.png)

La clé bootable est prête, il ne reste plus qu'à la brancher sur le poste et redémarrer l'ordinateur en donnant la priorité de boot sur la clé