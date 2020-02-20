# ALGORITHME : EXOS BOUCLES

## Exo 1

Ecrire un algorithme qui demande à l’utilisateur un nombre compris entre 10 et 20 jusqu’à ce que la réponse convienne.

    Variable N en Entier
    Debut
        Ecrire "Entrez un nombre entre 1 et 20"
        Lire N
        TantQue N < 10 ou N > 20
            Ecrire "Saisie erronée. Recommencez"
            Lire N
        FinTantQue
    Fin

## Exo 2

Ecrire un algorithme qui demande à l’utilisateur un nombre compris entre 10 et 20 jusqu’à ce que la réponse convienne.

En cas de réponse supérieure à 20, on fera apparaître un message : « Plus petit ! », et inversement, « Plus grand ! » si le nombre est inférieur à 10.

    Variable N en Entier
    Debut
        Ecrire "Entrez un nombre entre 1 et 20"
        Lire N
        TantQue N < 10 ou N > 20
            Si N < 10 alors
                Ecrire "Plus grand !"
            Sinon si N > 20 alors
                Ecrire "Plus petit !"
            Finsi
            Lire N
        FinTantQue
    Fin

## Exo 3

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite affiche les dix nombres suivants.

Par exemple, si l'utilisateur entre le nombre 17, le programme affichera les nombres de 18 à 27.

    Variables N, N10 en Entier
    Debut
        Ecrire "Entrez un nombre : "
        Lire N
        N10 ← N+10
        Ecrire "Les 10 nombres suivants sont : "
        TantQue N < N10
            N ← N+1
            Ecrire N
        FinTantQue
    Fin

## Exo 4

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite écrit la table de multiplication de ce nombre, présentée comme suit (cas où l'utilisateur entre le nombre 7) :<br/>
Table de 7 :<br/>
7 x 1 = 7<br/>
7 x 2 = 14<br/>
7 x 3 = 21<br/>
…<br/>
7 x 10 = 70

    Variables N, i en Entier
    Debut
        Ecrire "Entrez un nombre : "
        Lire N
        Ecrire "La table de multiplication de ce nombre est : "
        Pour i = 1 à 10
            Ecrire N, " x ", i, " = ", n*i
        FinPour
    Fin

## Exo 5

Ecrire un algorithme qui demande un nombre de départ, et qui calcule la somme des entiers jusqu’à ce nombre.

Par exemple, si l’on entre 5, le programme doit calculer : 1 + 2 + 3 + 4 + 5 = 15

    Variables N, i, Somme en Entier
    Debut
        Ecrire "Entrez un nombre : "
        Lire N
        Somme ← 0
        Pour i ← 1 à N
            Somme ← Somme + i
        FinPour
        Ecrire "La somme est : ", Somme
    Fin

## Exo 6

Ecrire un algorithme qui affiche les nombres pairs entre 1 et 10 (Connaissez-vous le modulo ?)

    Variables i en Entier
    Debut
        Pour i = 1 à 10

            Si (i%2) = 0 Alors
                Ecrire i
            FinSi

        FinPour        
    Fin


## Exo 7

Ecrire un algorithme qui demande successivement 20 nombres à l’utilisateur, et qui lui dise ensuite quel était le plus grand parmi ces 20 nombres :<br/>
Entrez le nombre numéro 1 : 12<br/>
Entrez le nombre numéro 2 : 14<br/>
...<br/>
Entrez le nombre numéro 20 : 6<br/>
Le plus grand de ces nombres est  : 14

Modifiez ensuite l’algorithme pour que le programme affiche de surcroît en quelle position avait été saisie ce nombre : C’était le nombre numéro 2

    Variables nombre, i, plusGrand, position en Entier
    Debut
        plusGrand ← 0
        Pour i ← 1 à 20
            Ecrire "Entrez un nombre : "
            Lire nombre
            Si i = 1 ou nombre > plusGrand Alors
                plusGrand ← nombre
                position ← i
            FinSi
        FinPour
        Ecrire "Le nombre le plus grand était : ", plusGrand
        Ecrire "Il a été saisi en position numéro ", position
    Fin

## Exo 8

Réécrire l’algorithme précédent, mais cette fois-ci on ne connaît pas d’avance combien l’utilisateur souhaite saisir de nombres. La saisie des nombres s’arrête lorsque l’utilisateur entre un zéro.

    Variables nombre, i, plusGrand, position en Entier
    Debut
        nombre ← 1
        i ← 0
        plusGrand ← 0
        TantQue N <> 0
            Ecrire "Entrez le nombre ",i," : "
            Lire nombre
            i ← i + 1
            Si i = 1 ou nombre > plusGrand Alors
                plusGrand ← nombre
                position ← i
            FinSi
        FinTantQue
        Ecrire "Le nombre le plus grand était : ", plusGrand
        Ecrire "C’était le nombre numéro ", IPpositionG
    Fin

## Exo 9

Lire la suite des prix (en euros entiers et terminée par zéro) des achats d’un client. Calculer la somme qu’il doit, lire la somme qu’il paye, et simuler la remise de la monnaie en affichant les textes "10 Euros", "5 Euros" et "1 Euro" autant de fois qu’il y a de coupures de chaque sorte à rendre.

    Variables montant, somdue, paye, Reste, Nb10E, Nb5E En Entier
    Debut
        montant ← 1
        somdue ← 0
        TantQue montant <> 0
            Ecrire "Entrez le montant : "
            Lire montant
            somdue ← somdue + montant
        FinTantQue

        Ecrire "Vous devez :", somdue, " euros"
        Ecrire "Montant versé :"
        Lire paye

        Reste ← paye - somdue

        Nb10E = 0
        TantQue Reste >= 10
            Nb10E = Nb10E + 1
            Reste = Reste – 10
        FinTantQue

        Nb5E = 0
        Si Reste >= 5
            Nb5E = 1
            Reste = Reste – 5
        FinSi

        Ecrire "Rendu de la monnaie :"
        Ecrire "Billets de 10 E : ", Nb10E
        Ecrire "Billets de  5 E : ", Nb5E
        Ecrire "Pièces de 1 E : ", reste
    Fin

## Exo 10

Le nombre mystère !

Ecrire un algorithme qui demande à l’utilisateur de retrouver un nombre compris entre 1 et 100 (choisi aléatoirement par l'ordinateur), en lui indiquant si le nombre est trop petit, trop grand, ou s'il a gagné.

Testez votre algorithme sur Scratch.

    Variable NombrePC, NombreJoueur en Entier
    Debut
        NombrePC = entier aleatoire
        Ecrire "Entrez un nombre entre 1 et 100"
        Lire NombreJoueur
        TantQue NombreJoueur <> NombrePC
            
            Si NombreJoueur < NombrePC
                Ecrire "Trop petit !"
            Si NombreJoueur > NombrePC
                Ecrire "Trop grand !"
            FinSi

            Lire NombreJoueur
        FinTantQue

        Ecrire "Bravo, vous avez trouvé !"
    Fin
