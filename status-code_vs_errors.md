STATUS CODE vs Errors

La différence entre une erreur et le status code, et que si un client ne parvient pas à communiquer avec le serveurs, à cause d’une erreur dans le nom de domaine utilisé, ou bien il n’y a plus de connexion internet, alors ceci est une erreur.
Le status code lui est un réponse que le serveur fournit au client l’informant le status de la réponse au client, la communication est donc bien établis entre le serveur et le client, le serveur peut donc donner des réponse approprier au client concernant la demande du client, tel que error 403 dans le cas ou le client effectue une requête pour une ressource dont il ne doit pas avoir accès, le serveur à compris la demande mais ne donnera pas accès aux ressources.

Status Codes :
100-199 : Réponse d’informations, plutôt rare.
200-299: Réponse « successful » signifiant que la demande à été traiter avec succès par le serveur.
300-399: Messages de redirection, par exemple une ressource à changer d’emplacement et nous somme rediriger vers la nouvelles, on à des fois pas le temps de la voir car le client va automatiquement vers le lien de redirection.
400-499: Erreur du client, très fréquente, surtout quand vous essayer de débugger une application client (front end dans le navigateur etc ), ou quand le client souhaite accéder à des ressource non disponible, ou que la manière dont il souhaite y accéder n’est pas dans dans la manière attendu.
500-599: Erreur du serveur, ont les vois de temps en temps, habituellement c’est lorsqu’il y’a un bug sur le serveur, comme une base de données déconnecter et que le serveur ne peut plus interroger.

Ces différent message nous informe donc que les requête on bien été reçus, et ils apporte une réponse approprié en fonction du résultat au traitement ( 200 => succes, 500 => error server, 403 => unauthorized, 301 => Moved permanently etc ) 
