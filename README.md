# TP1

## compte GitHub

créé sans pb, tout va bien .

## CLient UDP Python 

il faut récupérer le programme dans le chapitre du livre.

* récuperer de PDF
* chercher la page
* recuperer le programme dans un editeur
* exécuter 

Nous avons tout d'abord essayer de modifier les programmes à l'aide du prof puis à verifier si ça marche .
VOICI LE PROGRAMME OBTENU APRES LA VERIFICATION :
PREMIER PROGRAMME:

````python

from socket import * 

serverPort = 12000

serverSocket = socket(AF_INET, SOCK_DGRAM)

serverSocket.bind(('', serverPort))
print "The server is ready to receive"


while 1:
	message, clientAddress = serverSocket.recvfrom(2048)
	modifiedMessage = message.upper()
	serverSocket.sendto(modifiedMessage, clientAddress)
  
```

-Voici le programme1 : 

from socket import *
serverPort = 12000
serverSocket = socket(AF_INET, SOCK_DGRAM)
serverSocket.bind((
’’
, serverPort))
print
”The server is ready to receive”
while 1:
message, clientAddress = serverSocket.recvfrom(2048)
modifiedMessage = message.upper()
serverSocket.sendto(modifiedMessage, clientAddress) 



-Voici le Ééme programme :

from socket import *
serverName = "localhost"
serverPort = 12000
clientSocket = socket(AF_INET, SOCK_DGRAM)
message = raw_input("Input lowercase sentence:")
clientSocket.sendto(message,(serverName, serverPort))
modifiedMessage, serverAddress = clientSocket.recvfrom(2048)
print modifiedMessage
clientSocket.close()


A l’aide de ces deux programmes on va essayer d’utiliser le NC ,






NC ou netcat est un utilitaire permettant d'ouvrir des connexions réseau, que ce soit UDP ou TCP 

Voici la formule qu’on va utiliser pour le nc :

« nc hote port » (Par exemple pour se connecter sur le serveur exemple.local au port 12000)

Etant donné que hote : c’est le nom du serveur , et le port c’est le port du serveur utilisé 
dans les programmes suivants le nom du serveur est: « 10,98,2,98 » on l’a trouver on tapant « IFCONFIG » dans le terminal comme on peux le voir dans la photo ci dessous  
 
Le port est « 12000 »

On va sur le terminal puis on tape :
« nc 10,98,2,98 12000 »

On va bien voir que ça ne va pas marcher 
tout simplement parce que le nc est en TCP donc pour le rendre on UDP faut ajouter un  « -u » juste devant le nc comme cela :
« nc -u 10,98,2,98 12000 » 

On tapant cette commande dans le terminal on va bien voir que cava marcher comme on peut le voir dans la photo ci dessous :
