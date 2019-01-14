*** Detail sur l'application ***
     *******************

<h2>nom et prenom des binomes</h2>

<p>Assim Mahamat Abderahim Malick</p>

</p>Younouss Haroun Moursal</p>

<h2>Architecture globale de l'application</h2>

<p>
L'environnement client–serveur désigne un mode de communication à travers un réseau entre plusieurs programmes : l'un, qualifié de client, envoie des requêtes ; l'autre  qualifié de serveurs dans ce cas notre application de conversion, attendent les requêtes des clients et y répondent. Le client envoie des requetes http pour demander à l'application de faire la conversion d'un document word vers pdf et vise-versa,le client a un delai d'attente de 10 secondes pour telecharger le fichier sinon le document sera supprimer.
</p>

<h2>Architecture de la couche de donnée</h2>

<p>
notre application contiendra une base de donnée sur lequelle seront enregistré les identifiants des utilisateurs et le chemins de documents convertie;
l'application contiendra egalement un dossier qui va contenir tout les documents convertie.
quand un utilisateur convertie un document on va pouvoir stockée le document dans ce dossier ensuite on lui propose de telecharger son document qu'il vient de convertir. 
Une solution pour gerer la couche de donnée c'est d'utiliser le pattern DAO 
justification : L'utilisation de DAO permet de s'abstraire de la façon dont les données sont stockées au niveau des objets métier. Ainsi, le changement du mode 
de stockage ne remet pas en cause le reste de l'application. En effet, seules ces classes dites "techniques" seront à modifier (et donc à re-tester). 
Cette souplesse implique cependant un coût additionnel, dû à une plus grande complexité de mise en œuvre.
</p>

<h2>Gestion des clients</h2>

<p>

Les clients seront gerer comme Thread
une fois q'un client arrive a la plateforme il doit s'authentifier grace a son PID on pourra gerer ce client parraport au autre. 
au cas ou il y'aura une activité en cours d'execution (conversion) alors le client sera mis en attente cette activité (la conversion) constituera 
notre Section critiqueet tout les clients seront gerées en fonction de l'etat de la section  critique qui sera libre ou occupé et les clients seront mis 
dans l'etat demandeur ou en attente ou en execution
Justification : le Thread represente des processus leger, l'utilisation de plusieurs threads permet de paralléliser le traitement
et de l'executer rapidement.
</p>

<p>
Le site utilise le pattern MVC qui permet de bien organiser le code source. Il va nous aider à savoir quels fichiers créer, mais surtout à définir leur rôle. Le but de MVC est justement de séparer la logique du code en trois parties que l'on retrouve dans des fichiers distincts.

Modèle : cette partie gère les données de votre site. Son rôle est d'aller récupérer les informations « brutes » dans la base de données, de les organiser et de les assembler pour qu'elles puissent ensuite être traitées par le contrôleur. On y trouve donc entre autres les requêtes SQL.

Vue : cette partie se concentre sur l'affichage. Elle ne fait presque aucun calcul et se contente de récupérer des variables pour savoir ce qu'elle doit afficher. On y trouve essentiellement du code HTML mais aussi quelques boucles et conditions PHP très simples, pour afficher par exemple une liste de messages.

Contrôleur : cette partie gère la logique du code qui prend des décisions. C'est en quelque sorte l'intermédiaire entre le modèle et la vue : le contrôleur va demander au modèle les données, les analyser, prendre des décisions et renvoyer le texte à afficher à la vue. Le contrôleur contient exclusivement du PHP. C'est notamment lui qui détermine si le visiteur a le droit de voir la page ou non (gestion des droits d'accès).
</p>

<h2>Technologie choisie pour le développement</h2>

<p>
langage java, plateforme (netbeans ou j2ee), github pour le dépot git, OpenShift pour le deploiement de l'application sur le cloud.
    Un ou une servlet est une classe Java qui permet de créer dynamiquement des données au sein d'un serveur HTTP. Ces données sont le plus généralement présentées au format HTML, mais elles peuvent également l'être au format XML ou tout autre format destiné aux navigateurs web. Les servlets utilisent l'API Java Servlet (package javax.servlet).
    L'utilisation de servlets se fait par le biais d'un conteneur de servlets (framework) côté serveur. Celui-ci constitue l'environnement d'exécution de la servlet et lui permet de persister entre les requêtes des clients. L'API définit les relations entre le conteneur et le/la servlet. Le conteneur reçoit la requête du client, et sélectionne le/la servlet qui aura à la traiter. Le conteneur fournit également tout un ensemble de services standards pour simplifier la gestion des requêtes et des sessions.
</p>

<img src="usecase.PNG" /><br/>
<img src="class.PNG" />
