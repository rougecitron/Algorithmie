# ALGORITHME : EXOS VARIABLES CORRECTIONS

## Exo 1

Quelles seront les valeurs des variables A et B après chaque ligne du code suivant ?

    Variables A,B:entiers
    DEBUT
        A ← 3           A=3
        B ← A + 3       A=3 B=6
        A ← 4           A=4 B=6
    FIN

## Exo 2

Qu’affiche l’algorithme suivant ?

    Variables A,B,C:entier
    DEBUT
        A ← 9               A=9
        B ← A               A=9 B=9
        C ← A + B - 2       A=9 B=9 C=16
    FIN

## Exo 3

Quelles seront les valeurs des variables A, B et C après chaque ligne du code suivant ?

    Variables A,B,C:entiers
    DEBUT
        A ← 3
        B ← 5
        C ← A + B   A=3 B=5 C=8
        A ← 2       A=2 B=5 C=8
        C ← B - A   A=3 B=5 C=2
    FIN

## Exo 4

Quelles seront les valeurs des variables A, B et C après chaque ligne du code suivant ?

    Variables A,B:entiers
    DEBUT
        A ← 3
        B ← A + 4   A=3 B=7
        A ← A + 2   A=5 B=7
        B ← A - 4   A=5 B=1
    FIN

## Exo 5

Quelles seront les valeurs des variables A, B et C après chaque ligne du code suivant ?

    Variables A,B,C:entiers
    DEBUT
        A ← 5
        B ← 10
        C ← A + B   A=5  B=10 C=15
        B ← A + B   A=5  B=15 C=15
        A ← C       A=15 B=15 C=15
    FIN

## Exo 6

Qu’affiche l’algorithme suivant ?

    Variables A,B:entiers
    DEBUT
        A ← "123"
        B ← "456"
        Afficher A + B  => 579 car A et B sont entiers
    FIN

## Exo 7

Qu’affiche l’algorithme suivant ?

    Variables A,B:réels C:entier
    DEBUT
        A ← 2.3         A=2.3
        B ← 3.5         A=2.3 B=3.5
        C ← A + B       A=2.3 B=3.5 C=6
        Afficher C
    FIN

## Exo 8

Que produit l’algorithme suivant ?

    Variables A,B:chaînes
    DEBUT
        A ← "123"
        B ← "456"
        Afficher A + B  => erreur ! car A et B sont des chaines
    FIN

## Exo 9

Que produit l’algorithme suivant ?

    Variables A,B:chaînes
    DEBUT
        A ← "123"
        B ← "456"
        Afficher A & B  => "123456" (concaténation)
    FIN

## Exo 10

Quelles sont les valeurs de A et B à la fin du code suivant ? Adaptez l’algorithme pour échanger les valeurs de A et B.

Solution 1, on utilise une variable tampon :

    Variables A,B :entiers
    DEBUT
        A ← 3   A =3
        B ← 5   A=3 B=5
        C ← A   A=3 B=5 C=3
        A = B   A=5 B=5 C=3
        B = C   A=5 B=3 C=3
    FIN

Solution 2, pour des nombres seulement :

    Variables A,B :entiers
    DEBUT
        A ← 3       A =3
        B ← 5       A=3 B=5
        A = B + A   A=8 B=5
        B = A - B   A=8 B=3
        A = A - B   A=5 B=3
    FIN
