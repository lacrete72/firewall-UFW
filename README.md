# firewall-UFW

Cette commande vous indiquera l’état actuel d’UFW.

```
sudo ufw status
```
démarrer ufw 

```
sudo ufw enable
```

arrêter ufw 

```
sudo ufw disable
```
Une unique commande qui vous permettra de jeter un œil sur la totalité des instructions que vous avez indiquées à UFW 
```
sudo ufw status verbose
```

autoriser l'accès à un service ( 80 par exemple ou ssh) il faut préciser le protocole utilisé 
```
sudo ufw allow 80/tcp
sudo ufw allow 22/ssh
```
pour bloquer un port en particulier
```
sudo ufw deny 80/tcp
```

bloquer une ip en particulier en faisant cette commande la règle va à la suite des autres donc il faudra la placer avant.
```
sudo ufw deny from 172.16.98.72 
```
pour ce faire il faut faire cette command
```
sudo ufw insert 1 deny from 172.16.98.72
```
afficher les regles avec les numéros 
```
sudo ufw status numbered
```
supprimer une règle 
```
sudo ufw delete [numéro de la règle]
```
activer la journalisation 
```
sudo ufw logging on
```
désactiver la journalisation
```
sudo ufw logging off
```
refuser une connexion sortante [règle] est à remplacer par un port ou un service ( 22 ou ssh par exemple )
```
sudo ufw deny out [règle]
```
