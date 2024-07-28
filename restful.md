RESTful APIs
« Respresentational State Transfert », ou REST est une convention que beaucoup de serveurs HTTP utilisent. 
Les api RESTful suivent un ensemble de règles/standards et de conventions rendant plus facile le développement d’api. Un des objectifs et de permettre au client interagissant avec l’api de savoir qu’est-ce qu’il doit attendre comme réponse du serveur, facilitant ainsi l’expérience de développement. 

Separate and Agnostic

La grande idée derrière les api’s REST c’est que l’on sais à quoi s’attendre comme réponse/résultat de cette requête,
sans prendre en compte le language ou la techno pour  l’implémentation du client et du serveurs, ils sont fait indépendamment de l’autre, le front et le back sont séparer. La seule chose qui importera seront des les routes pour accéder à celle ci et le format des données transférer ( JSON? XML? )

Stateless

Une architecture RESTful est dite « stateless » ( sans état ), cela signifie que le serveurs n’as pas besoin de connaitre l’état du client, et le client n’as pas besoin de connaitre l’état du serveur, dans le sens ou l’interaction entre le client et le serveur sont par les « ressources » au lieu des « commande ». Il faut garder en tête que cela ne signifie pas que l’application et « stateless  » sans état, car nous pouvons par exemple mettre à jours nos jours nos ressources. Donc notre client et notre serveur ont bel est bien un état, mais ils n’utilise pas cet état pour établir la communication entre eux, il ne sauvegarde pas de trace des requêtes précédentes, chaque requêtes effectuer plusieurs fois est enfaite considérer comme si c’était la première fois.

Path in REST

Un autre concept clé, est que les api REST utilisent les chemins dans les URL pour accéder à une ressources, précisément la dernière section de l’url précise ce que nous souhaitons obtenir. On peut aussi ajouter des « query parametter » comme vu dans les URLs, généralement utiliser dans les requête GET, pour récupérer des données filtrer/trier, limiter le nombre de résultat etc.. Pour utiliser correctement l’api afin d’accéder au ressource, nous auront besoins d’une documentation, celle ci nous fournira les endpoint approprier à nos besoins, avec les chemins correspondant (URL, query parameters etc )



Conclusion : Les serveurs RESTful communique donc l’état des ressources, il n’expose pas d’accès à des commandes arbitraire?
