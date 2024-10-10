# Tache 2

Noms:
* Joey Fanor (20228416)
* Xinning Xu (20213497)

## Projet

[JSoup](https://github.com/haskaalo/jsoup)

## Documentation

Test 1
Public void testReadIndexOut() teste la méthode public int read(byte[] dest, int offset, int desiredLen) de la classe SimpleBufferedInput du package Internal. 

On a choisi de teste cette méthode en raison de son importance sur la lecture des input streams par les buffers. La méthoide read(byte[] dest, int offset, int desiredLen) assure le transfert des inputs streams dans les tableaux, ce qui est essentiel pour les opérations futures de performer.

Test 2 
Public void testRead() teste la méthode public int read() de la classe SimpleBufferedInput du package Internal.

On a choisi cette méthode pour ajouter un test puisqu’il est nécessaire d’assurer que, dans le cas où les données extraites du buffer qui dépasse la longueur du buffer, il ne causera pas un bug, et que le processus de la lecture est géré correctement malgré la situation. Je trouve qu’il est critique de tester ce méthode puisque la lecture incorrecte des données causera des problèmes pour les opérations futures.

Test 3 
Public void testReadLimit() teste la méthode public void mark(int readLimit) de la classe SimpleBufferedInput du package Internal, spécifiquement sur le cas où la limite de la lecture dépasse la taille du buffer. 

On a choisi de tester de méthode puisqu’en assurant que la lecture du système ne va pas dépasser la taille du buffer, on empêche des erreurs telles que le dépassement de mémoire ou des comportements inattendus lors de la lecture de grandes quantités de données. Le test vérifie également qu'une exception IllegalArgumentException est lancée correctement lorsque la limite de lecture dépasse la taille du buffer, et évite des bugs lors des cas limites (edge cases).

Test 4 
Public void testReset() teste la méthode public void reset() de la classe SimpleBufferedInput du package Internal, en se concentrant sur le cas limite où la position du marqueur est négative. 

On a choisi cette méthode puisque si la méthode ne lance pas correctement l'exception IOException lorsqu'il y a un marqueur invalide, cela pourrait entraîner une mauvaise gestion des positions lors de la lecture des streams d'entrée. reset() est nécessaire pour revenir à une position marquée dans un stream. Si ce comportement échoue, cela pourrait causer des incohérences dans la gestion des données, avec des conséquences comme la perte ou la duplication de données lues. 

Test 5 
Public void testMap() teste la méthode public Connection data(Map<String, String> data) de la classe HttpConnection du package helper. 

On a choisi cette méthode à tester puisqu’en testant cette méthode, on assure que les données sont correctement validées et ajoutées. Si la méthode ne fonctionne pas correctement, les requêtes HTTP pourraient être mal formées ou manquer des paramètres critiques, ce qui nuira à l'intégrité des communications entre le client et le serveur. Le test vérifie aussi qu'une ValidationException est lancée lorsqu’il y a des données invalides, garantissant ainsi que la méthode continuera à rouler lors des entrées incorrectes.

## Taux de couverture

### Avant

<img width="994" alt="image" src="https://github.com/user-attachments/assets/8bb29bfe-9a80-4b66-b158-2095b7472984">


### Après

<img width="1025" alt="image" src="https://github.com/user-attachments/assets/8deb79fe-b5c7-4a59-b92a-dd10919f860b">
