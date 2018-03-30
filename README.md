

# Le nom de notre binome est : Dan MONUNU et Jean-Philippe N'GUESSAN

# Exercice 3 - Injection de dépendances avec Guice

Voici notre arbre d'injection :

L'objet InterpreteurLigneCommande a besoin qu'on lui injecte un objet MailService. Et l'objet MailService a besoin qu'on lui injecte un objet MailSender.

# InterpreteurLigneCommande ---> MailService ---> MailSender


# Exercice 5 - BDD avec Cucumber-jvm
_Temps estimé : 40 mins_


  4) Ajouter des cas de test dans la feature `trier_mail.feature` : faut-il ecrire de nouvelles méthodes de test comme en tests unitaires ?
# Non pour ce cas, il ne faut plus écrire de nouvelles méthodes de test comme en tests unitaires mais juste rajouter les différents tests dans l'exemple en fonction de ce qu'on veut tester.

 5) Nous avons fait la question optionnelle. 

# Nous avons écrit un scénario mailNulstep qui vérifie si un des deux mails est nul, ensuite nous l'avons ajouté dans le feature et nous avons testé et le test passe bien sur Cucumber. Donc vous pouvez aller voir la classe et les features qu'on a rajouté. 



