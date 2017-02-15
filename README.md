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
eT
