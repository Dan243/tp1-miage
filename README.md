<<<<<<< HEAD


<<<<<<< HEAD
Le nom de notre binome est : Dan MONUNU et Jean-Philippe N'GUESSAN


# Déroulement du TP
Nous fournissons trois projets Eclipse servant de base de travail aux exercices suivant. Cela permet un point de synchronisation de tous les étudiants à différents moments du TP. 
* Le projet ex1-ini est le code initial du TP et sert de base aux exercices 1 et 2. Une fois terminés, faire un push vers Github et fermer le projet Eclipse (ne pas le supprimer).
* Le projet ex3-ini sert de code de base aux exercices 3 et 4. Une fois terminés, faire un push vers Github et fermer le projet Eclipse (ne pas le supprimer).
* Le projet ex5-ini sert de code de base à l'exercice 5. Une fois terminé faire un push vers Github.
=======
MONUNU Dan et N'GUESSAN Jean-Philippe
>>>>>>> branch 'master' of https://github.com/Dan243/tp1-miage.git

# Exercice 1 - Refactoring
_Temps estimé : 20 mins_

__Travailler dans le projet fourni mailreader-ex1-ini__

1) Réusiner la classe `MailComparator`

Raccourcis clavier à connaître : 
* ALT-SHIFT-S : fonctions Eclipse de génération de sources (ex : constructeurs)
* ALT-SHIFT-T : fonctions de réusinage
* ALT-SHIFT-M : extraction de méthode (sur sélection)
* ALT-SHIFT-R : renommage (sur sélection)

# Exercice 2 - Découpage en couches
_Temps estimé : 20 mins_

1) Réorganiser le code dans les couches standards. 

Faire en sorte par exemple que divers frontends puisse récupérer les mails. Nous aurons dans ce TP un seul frontend : un CLI (ligne de commande) qui sera implémenté sous la forme d'une classe `ClientMail` avec `main()`. 
Cette méthode main attend deux arguments : un booleen `production` qui précise si le mail doit vraiment être envoyé (`true`) ou si nous sommes en environnement de recette (`false`). Le second argument est le sujet du mail.

Rappel : exemple de méthode main qui parse un boolean : 
```
public static void main(String[] args) {
   production = Boolean.parseBoolean(args[0]);
   ...		
```
Conception :

![diag sequence](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/bflorat/tp1-miage/master/diag1.puml&ttt=1)
![diag classe](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/bflorat/tp1-miage/master/diag2.puml&ttt=1)

Prévoir une cinquième couche `commun` pour les éléments communs à toutes les couches comme les exceptions. 

`MailSender` est une interface, le choix de l'implémentation est fait par l'application en fonction de la valeur du booléen `production`.
=======
# Le nom de notre binome est : Dan MONUNU et Jean-Philippe N'GUESSAN
>>>>>>> branch 'master' of https://github.com/Dan243/tp1-miage.git

# Exercice 3 - Injection de dépendances avec Guice

Voici notre arbre d'injection :

L'objet InterpreteurLigneCommande a besoin qu'on lui injecte un objet MailService. Et l'objet MailService a besoin qu'on lui injecte un objet MailSender.

# InterpreteurLigneCommande ---> MailService ---> MailSender


# Exercice 5 - BDD avec Cucumber-jvm
_Temps estimé : 40 mins_


  4) Ajouter des cas de test dans la feature `trier_mail.feature` : faut-il ecrire de nouvelles méthodes de test comme en tests unitaires ?
# Non pour ce cas, il ne faut plus écrire de nouvelles méthodes de test comme en tests unitaires mais juste rajouter les différents tests dans l'exemple en fonction de ce qu'on veut tester.

 5) Nous avons fait la question optionnelle. 

# Nous avons écrit une classe MailNulstep qui contient les step qui vérifie si un des deux mails est nul. Ensuite, nous avons ajouté les features en utilisant la méthode avec les phrases, enfin nous avons vérifié que les tests passent bien sur Cucumber. Donc vous pouvez aller voir la classe des steps et les features qu'on a rajouté. 



