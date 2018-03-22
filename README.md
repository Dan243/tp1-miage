

Le nom de notre binome est : Dan MONUNU et Jean-Philippe N'GUESSAN

# Exercice 3 - Injection de dépendances avec Guice
_Temps estimé : 20 mins_

Point de synchro : repartir du projet fourni `mailreader-ex3-ini`

Guice est le framework d'injection de dépendance en Java de Google. Il est léger et la configuration se fait en java (et non par fichier XML ou par annotations). Ses concurrents en Java sont principalement Spring Core et CDI dans le monde JEE. Ce pattern est également présent dans la plupart des languages, comme dans Symphony en PHP ou AngularJS en JavaScript.

La méthode `configure()` de la classe `MailReaderModule` contient la configuration de Guice. C'est ici qu'on associe une interface à la classe contrète qui sera injectée. Exemple :
```
bind(MonInterface.class).to(MaClasseConcrete.class)
```
Il est bien sûr également possible d'injecter des classes concrètes (comme ici le `MailService`).

1) Compléter la méthode `configure()`
Observer la méthode `ClientMail.main()` : elle charge la configuration et créé l'objet de haut niveau de l'arbre d'injection : un `InterpreteurLigneCommande`.

2) L'objet `InterpreteurLigneCommande` a besoin d'un `MailService`. Lui injecter (injection par constructeur) via l’annotation (standard java) `@Inject`.

3) Faire de même pour l'injection du `MailSender` dans le `MailService`.

Noter l'arbre d'injection que forme les objets injectés depuis  `InterpreteurLigneCommande`.

Voici notre arbre d'injection :

L'objet InterpreteurLigneCommande a besoin qu'on lui injecte un objet MailService. Et l'objet MailService a besoin qu'on lui injecte un objet MailSender.

InterpreteurLigneCommande ---> MailService ---> MailSender

# Exercice 4 - TU
_Temps estimé : 30 mins_

1) Compléter les tests unitaires ou en écrire de nouveaux dans les test cases `MailTest` et `MailComparatorTest`. Enlever les annotations `@Ignore` s'il y en a.

2) Exécuter vos tests si besoin (automatique si vous pratiquez le test continu avec infinitest).

# Exercice 5 - BDD avec Cucumber-jvm
_Temps estimé : 40 mins_

Point de synchro : repartir du projet fourni `mailreader-ex5-ini`

cucumber-jvm est l'implémentation java de cucumber, un framework de BDD (Behavioral Driven Development) très populaire. Il est existe d'autres : JBehave (l'original, très similaire), Concordion, JGiven ...

Pour les besoins du TP, nous utilisons ici les notions de Scenario Outline, de Data Table et de Transformer permettant l'utilisation de données tabulaires et de formats custom.

1) Compléter la classe `MailComparaisonStep`
2) Lancer le test `CucumberRunnerTest` en junit
3) Ouvrir dans un navigateur `target/cucumber/index.html`
4) Ajouter des cas de test dans la feature `trier_mail.feature` : faut-il ecrire de nouvelles méthodes de test comme en tests unitaires ?

5) optionnel :
Ecrire un scenario simple au format textuel et les steps correspondants.

# Cleanup
Si vous le désirez, vous pourrez supprimer votre projet github mais pas avant fin juin (noté)

