HTTP METHODS
Chaque fois que nous effectuons une requête HTTP nous devons obligatoirement spécifier une méthode, il y’en à plusieurs et chacune d’entre elles correspondent à un besoin, une action bien précise :
- GET
- POST
- PUT
- DELETE
- PATCH
- OPTIONS
- CONNECT
- etc etc..

Ces méthode nous permettent d’effectuer des opérations CRUD (Create Read Update Delete)

exemple: 
CREATE => POST
READ => GET
UPDATE => PUT, PATCH
DELETE => DELETE

Nous allons ici détailler quelques méthodes les plus couramment utiliser.
- GET : La méthode GET sert principalement à récupérer des données depuis le serveurs, elle n’as pas de body comme dans la méthode POST, ce qui la rend « plus safe », dans le sens ou rien ne va changer dans le serveur, on va juste récupérer des informations, leur « copie » depuis le serveur.
-  POST : La méthode POST permet d’envoyer des données, qu’on appelle « payload » ( charge utile ) dans un format JSON ou XML, celle ci sera dans le body de la requête, on peut très bien envoyer un body vide mais cela perd donc son intérêt, le but étant d’envoyer des informations, la création de nouvelle informations. Il est donc important de garder à l’esprit que la requête POST va donc « altérer » l’état de notre serveur, dans le sens ou de nouvelles informations ont était ajouter, donc de nouvelles informations sont stockées, pour être traiter à l’avenir, ou à l’instant ou les données vont être renvoyer pour effectuer des opérations etc, il faut donc faire attention à ce que l’on fait. Une bonne pratique et de détailler de type de contenu du payload dans le header de la requêtes
- , par exemple si le contenu du body et au format JSON:
headers: {
    'Content-Type': 'application/json'
}
body: JSON.stringify(data)
- PUT: Similaire POST et PATCH, elle créée de nouvelles ressources ou les remplaces/met à jours à la source avec le contenu du payload ( body ), il va créer si elle n’existe pas et mettre à jour si elle existe. La principales différence avec la requête POST sert à la création est que PUT elle peut créer/mettre à jour et est « idempotent » ( indenpotente) ce qui signifie que même si l’on a plusieurs fois la même requête PUT, elle auras le même effet sur le serveur, si le serveur reçois plusieurs fois la même requête identique il ne vas re effectuer l’opération, elle ne va pas re créer plusieurs ressources contrairement à la requête POST, qui va avoir différent effet secondaire en créant de multiples copies. On considère donc pour cela que PUT est plus « safe » que POST dans ce cas la. POST va créer de nouvelle ressource et donc générer de nouveaux id à chaque requête, la ou avec PUT nous allons utiliser par exemple l’ID pour directement cibler la ressource que nous souhaitons mettre à jour et c’est la seule choses qui va changer sur notre serveur, il n’y aura pas de nouvelles ressource créer à chaque requête.
- PATCH :Similaire à PUT, sauf que la ou PUT va modifier une ressource dans son entièreté, on va utiliser PATCH pour modifier une partie uniquement, mais PUT est plus populaire que PATCH pour ce genre de tâche.
- DELETE: Comme son nom l’indique, cette méthode sert à supprimer une ressource.

