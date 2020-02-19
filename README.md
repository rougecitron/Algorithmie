# ALGORITHME ET PSEUDO CODE

## Qu'est-ce qu'un algorithme ?

<b>Un algorithme, c’est une suite d’instructions, qui une fois exécutée correctement, conduit à un résultat donné.</b>

Si l’algorithme est juste, le résultat est le résultat voulu. S'il est faux, le résultat est ... aléatoire !

Pour fonctionner, <b>un algorithme doit contenir uniquement des instructions compréhensibles par celui qui devra l’exécuter.</b>

Or, nous voulons faire comprendre nos instructions par un ordinateur, qui est parfaitement idiot.

Nous devons donc décomposer tous nos programmes en des instructions simples compréhensibles par lui :

    L'algorithme, c'est la structure de notre programme.

## Qu'est-ce que le pseudo-code ?

Il existe plusieurs manières d'écrire un algorithme. On trouve des représentations graphiques : des organigrammes. Et un langage s'est imposé par convention : le pseudo-code.

    On écrit le pseudo-code en français, en détaillant les instructions grâce à des variables, tests, boucles, etc.

Je vous recommande ce cours très complet : <a href="http://pise.info/algo/" target="_blank">http://pise.info/algo/</a>

<hr/>

## Variables

Une variable est une boite dans laquelle on stocke une information et à qui on donne un nom.

    Exemple : prenom ← Nadine
         ou : prenom = Nadine

On distingue plusieurs types de variables :

    - des entiers : 1, 95, 5684230
    - des réels (ou décimaux) : 1.5, 3.14519, 5684523.98523
    - des chaines de caractères alphanumériques : "Nadine", "toto64", "34 Avenue de la Paix"
    - des booléens : c'est une valeur VRAI ou FAUX

## Opérateurs

On dispose des quatre opérations arithmétiques, tout ce qu’il y a de classique :

    - addition : +
    - soustraction : -
    - multiplication : *
    - division : /

On dispose également d'un opérateur alphanumérique qui permet de concaténer (associer) 2 chaines alphanumériques : &

    Exemple :
    Variables A, B, C :chaînes
    Début
        A ← "Gloubi"
        B ← "Boulga"
        C ← A & B
    Fin

> Exercices [exos/1_exos_variables.md](exos/1_exos_variables.md)

<hr/>

## Tests

Le test est la pierre angulaire de notre programme : grâce aux tests, on va pouvoir faire des choix.

Il n’y a que deux formes possibles pour un test. La première est la plus simple :

    Si condition Alors
        Instructions
    Finsi

 La seconde est plus complexe et offre une alternative :

    Si condition Alors
        Instructions 1
    Sinon
        Instructions 2
    Finsi

La condition est toujours de type booléenne : soit la condition est remplie donc c'est VRAI, soit elle n'est pas remplie donc c'est FAUX.

La condition est une comparaison. Elle est composée de trois éléments :

    - une valeur
    - un opérateur de comparaison
    - une autre valeur

Les valeurs peuvent être a priori de n’importe quel type (numériques, caractères…). Mais si l’on veut que la comparaison ait un sens, il faut que les deux valeurs de la comparaison soient du même type !

Les opérateurs de comparaison sont :

    - égal à : =
    - différent de : != ou <>
    - strictement plus petit que : <
    - strictement plus grand que : >
    - plus petit ou égal à : <=
    - plus grand ou égal à : >=

On peut avoir besoin de combiner plusieurs opérations, par exemple pour tester si un nombre est entre 1 ET 10. Pour cela, on dispose d'opérateurs logiques :

    - ET : pour indiquer que les 2 conditions doivent être remplies toutes les deux
    - OU : pour indiquer que l'une ou l'autre des conditions doit être remplie, au choix
    - NON : pour inverser la condition. NON VRAI = FAUX !

Un exemple :

    Variable Temp en Entier
    Début
        Ecrire "Entrez la température de l’eau :"
        Lire Temp
        Si Temp =< 0 Alors
            Ecrire "C’est de la glace"
        Sinon Si Temp > 0 ET Temp < 100 Alors
            Ecrire "C’est du liquide"
        Sinon
            Ecrire "C’est de la vapeur"
        Finsi
    Fin

> Exercices [exos/2_exos_tests.md](exos/2_exos_tests.md)

<hr/>

## Boucles

Les boucles sont la quintessence de la programmation : grâce aux boucles, on peut répéter une instruction autant de fois qu'on veut !

Prenons l'exemple suivant :

    Variable Réponse en Caractère
    Début
        Ecrire "Voulez vous un café ? (O/N)"
        Lire Réponse
        Si Réponse <> "O" et Réponse <> "N" Alors
            Ecrire "Saisie erronnée. Recommencez"
            Lire Réponse
            Si Réponse <> "O" et Réponse <> "N" Alors
                Ecrire "Saisie erronnée. Recommencez"
                Lire Réponse
                Si Réponse <> "O" et Réponse <> "N" Alors
                    Ecrire "Saisie erronnée. Recommencez"
                    Lire Réponse
                FinSi
            FinSi
        FinSi
    Fin

L'utilisateur peut se tromper 3 fois, mais pas 4 ! Comparez avec la ré-écriture suivante :

    Variable Réponse en Caractère
    Début
        Ecrire "Voulez vous un café ? (O/N)"
        Lire Réponse
        TantQue Réponse <> "O" et Réponse <> "N"
            Ecrire "Saisie erronnée. Recommencez"
            Lire Réponse
        FinTantQue
    Fin

Qu'en pensez-vous ?

<hr/>

On distingue principalement 2 cas d'usages :

    - TantQue : pour contrôler une entrée utilisateur par exemple. 
                On ne sait pas à l'avance combien de tours de boucle on fera.
    - Pour : pour réaliser un compteur par exemple. On sait exactement combien de tours on veut.

Par exemple, si on veut 10 tours de manège :

    Variable Tour en Entier
    Début
        Tour ← 0
        TantQue Tour < 10
            Tour ← Tour + 1
            Ecrire "Tour numéro : ", Tour
        FinTantQue
    Fin

On utilisera plutot la boucle compteur qui a une syntaxe plus condensée :

    Variable Tour en Entier
    Début
        Pour Tour ← 1 à 10
            Ecrire "Tour numéro : ", Tour
        FinPour
    Fin

N'est-ce pas plus élégant ?

> Exercices [exos/3_exos_boucles.md](exos/3_exos_boucles.md)
