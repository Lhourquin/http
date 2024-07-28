JSON
JSON est l’acronyme de JavaScript Obejct Notation, c’est un standard de structure de données basé sur la syntaxe d’objet JavaScript. JSON est très utilisé pour transmettre des données dans une application en utilisant HTTP, elle sera utiliser dans le body. 
Syntaxe JSON :

{
    "movie": [
        {
            "id":1,
            "genre": "Action",
            "title": "Iron Man",
            "director": "Jon Favreau",
        },
        {
             "id": 2,
             "genre": "Action",
             "title": "Batman Begins",
             "director": "Christopher Nolan"       
        }
    ]
}	
 	ou
[
    {
        "id":1,
        "genre": "Action",
        "title": "Iron Man",
        "director": "Jon Favreau",
    },
    {
         "id": 2,
         "genre": "Action",
         "title": "Batman Begins",
         "director": "Christopher Nolan"       
    }
]
C’est une manière très flexible de transmettre des données structurée « plain text », il est très simple de travailler avec ses données. Il peut aussi être utiliser pour des fichier de configuration, dans un fichier .json, et même dans des base de données NoSQL comme MongoDB, ElasticSearch ou Firestore.  ll peut être utiliser dans différent langage de programmation. C’est donc un format pour communiquer des données et les stockées.
Un autre format utiliser au même fin avant cela était le XML, encore utilisé mais beaucoup moins aujourd’hui.
exemple : 
XML :
<root>
    <id>1</id>
    <genre>Action</genre>
    <title>Iron Man</title>
    <director>Jon Favreau</director>
</root>

JSON : 
{
    "id": "1",
    "genre": "Action",
    "title": "Iron Man",
    "director": "Jon Favreau"
}


