*A M.**Chevalier**, M.**Lhoste**,*

*Nous avons précédemment porté votre Base de donnée dans un gestionnaire de base de données relationnelle SQL, en l'occurence PostGres. Vous désirez maintenant étudier la possibilité de porter votre base de données dans un gestionaire NoSQL tel que MongoDB. Cela nous sied, étant partisans d'outils Open Source. Cette fois-çi, je serai votre référent unique, et je prendrai seul la responsabilité de vous faire découvrir les enjeux de votre demande, et sa faisabilité au travers d'une Preuve de Concept (POC).*

___

# **SOMMAIRE** #

**I** - *Tuto Mongo Shell*  
    **1)** *Fichiers installés et ouverture*  
    **2)** *Commandes de création de base, insertion des données et vérification*  

**II** - *CSV to MongoDB with Python*  
    **1)** *Fonction d'insertion*  
    **2)** *Insertion Movies*  
    **3)** *Vérification Mongo Compass*  
    
___


## **Introduction** ##

*Clés primaires ? Etrangères ? Associations ? Multiplicités ? Tables ? Oublions tout ça. Passer de SQL au NoSQL, c'est changer de paradigme. C'est de prime abord passer de relationnel à non relationnel (ou distribué). C'est passer de bases de données basées sur des "tables" à des bases de données basées sur des paires clé-valeur et documents dans une "collection".*

*La base de données NoSQL convient mieux au stockage de données hiérarchique car elle suit la méthode de la paire clé-valeur pour stocker des données similaires aux données JSON. Les bases de données NoSQL sont hautement préférées pour les ensembles de données volumineux avec des requêtes peu complexes*

*Comme vous le verrez, nous n'aurons pas besoin de convertir nos fichiers csv en json pour l'insertion. En insérant notre csv movies dans une variable de type liste, la méthode d'insertion de pymongo ajoutera les documents (paires clé-valeur) au format json, ou plutot bson (conversion binaire) pour être exact.*