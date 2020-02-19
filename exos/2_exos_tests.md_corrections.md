# ALGORITHME : EXOS TESTS CORRECTIONS

## Exo 1

Ecrire un algorithme qui demande un nombre à l’utilisateur, et l’informe ensuite si ce nombre est positif ou négatif (on laisse de côté le cas où le nombre vaut zéro).

    Variable nombre:entier
    Debut
        ecrire "Entrez un nombre :"
        nombre = lire reponse

        si nombre >= 0 alors
            ecrire "le nombre " & nombre & " est positif"
        sinon
            ecrire "le nombre <nombre> est negatif"
        finsi
    Fin

## Exo 2

Écrire un algorithme qui demande un nombre entre 10 et 20 à l'utilisateur et lui indique si sa saisie est correcte.

    Variable nombre:entier
    Debut
        ecrire "Entrez un nombre entre 10 et 20 :"
        nombre = lire reponse

        si nombre >= 10 ET nombre <= 20 alors
            ecrire "le nombre " & nombre & " est correct"
        sinon
            ecrire "le nombre " & nombre & " est incorrect"
        finsi
    Fin

## Exo 3

Reprendre l'exercice 1 en ajoutant cette fois le cas où le nombre vaut zéro.

    Variable nombre:entier
    Debut
        ecrire "Entrez un nombre :"
        nombre = lire reponse

        si nombre = 0 alors
            ecrire "le nombre est nul"
        sinon si nombre > 0 alors
            ecrire "le nombre " & nombre & " est positif"
        sinon
            ecrire "le nombre " & nombre & " est negatif"
        finsi
    Fin

## Exo 4

Ecrire un algorithme qui demande trois noms à l’utilisateur et l’informe ensuite s’ils sont rangés ou non dans l’ordre alphabétique.

    Variables a, b, c en Caractère
    Début
        Ecrire "Entrez successivement trois noms : "
        Lire a, b, c
        Si a < b ET b < c Alors
            Ecrire "Ces noms sont classés alphabétiquement"
        Sinon
            Ecrire "Ces noms ne sont pas classés"
        Finsi
    Fin

## Exo 5

Ecrire un algorithme qui demande deux nombres à l’utilisateur et l’informe ensuite si le produit est négatif ou positif (on inclut le traitement du cas où le produit peut être nul). Attention toutefois, on ne doit pas calculer le produit !

    Variables m, n en Entier
    Début
        Ecrire "Entrez deux nombres : "
        Lire m, n
        Si (m > 0 ET n > 0) OU (m < 0 ET n < 0) Alors
            Ecrire "Leur produit est positif"
        Sinon
            Ecrire "Leur produit est négatif"
        Finsi
    Fin

## Exo 6

 Écrire un algorithme qui détermine la catégorie sportive d’un utilisateur en fonction de son âge :<br/>
18 à 19 ans : junior<br/>
20 à 22 ans : espoir<br/>
23 à 39 ans : sénior<br/>
40 ans et plus : vétéran

    Variable age en Entier
    Début
        Ecrire "Entrez l’âge : "
        Lire age
        Si age >= 40 Alors
            Ecrire "Catégorie vétéran"
        SinonSi age >= 23 Alors
            Ecrire "Catégorie sénior"
        SinonSi age >= 20 Alors
            Ecrire "Catégorie espoir"
        SinonSi age >= 18 Alors
            Ecrire "Catégorie junior"
        Sinon
            Ecrire "Catégorie inconnue"
        Finsi
    Fin

## Exo 7

Un magasin de reprographie facture 0,10 € les dix premières photocopies, 0,09 € les vingt suivantes et 0,08 € au-delà.
Ecrivez un algorithme qui demande à l’utilisateur le nombre de photocopies effectuées et qui affiche la facture correspondante.

    Variables n, p en Numérique
    Début
        Ecrire "Nombre de photocopies : "
        Lire n
        Si n <= 10 Alors
            p ← n * 0,1
        SinonSi n <= 30 Alors
            p ← 10 * 0,1 + (n – 10) * 0,09
        Sinon
            p ← 10 * 0,1 + 20 * 0,09 + (n – 30) * 0,08
        FinSi
        Ecrire "Le prix total est: ", p
    Fin

## Exo 8

Cet algorithme est destiné à prédire l'avenir, et il doit être infaillible ! Il lira au clavier l’heure et les minutes, et il affichera l’heure qu’il sera une minute plus tard.
Par exemple, si l'utilisateur tape 21 puis 32, l'algorithme doit répondre : "Dans une minute, il sera 21 heure(s) 33".
Note : on suppose que l'utilisateur entre une heure valide. Pas besoin donc de la vérifier.

    Variables h, m en Numérique
    Début
        Ecrire "Entrez les heures, puis les minutes : "
        Lire h, m
        m ← m + 1
        Si m = 60 Alors
            m ← 0
            h ← h + 1
        FinSi
        Si h = 24 Alors
            h ← 0
        FinSi
        Ecrire "Dans une minute il sera ", h, "heure(s) ", m, "minute(s)"
    Fin

## Exo 9

Les habitants de Zorglub paient l’impôt selon les règles suivantes :

- les hommes de plus de 20 ans paient l’impôt
- les femmes paient l’impôt si elles ont entre 18 et 35 ans
- les autres ne paient pas d’impôt

Le programme demandera donc l’âge et le sexe du Zorglubien, et se prononcera donc ensuite sur le fait que l’habitant est imposable.

    Variable sex en Caractère
    Variable age en Numérique
    Variables C1, C2 en Booléen
    Début
        Ecrire "Entrez le sexe (M/F) : "
        Lire sex
        Ecrire "Entrez l’âge: "
        Lire age
        C1 ← sex = "M" ET age > 20
        C2 ← sex = "F" ET (age >= 18 ET age <= 35)
        Si C1 ou C2 Alors
            Ecrire "Imposable"
        Sinon
            Ecrire "Non Imposable"
        FinSi
    Fin

## Exo 10 : chatbot

    Variable prenom, reponse1, reponse2 en Caractère
    Début
        Ecrire "Votre prénom : "
        Lire prenom
        Ecrire "Etes-vous de bonne humeur ?"
        Lire reponse1
        Si reponse1="oui" Alors
            Ecrire "Voulez-vous faire des algorithmes ?"
            Lire reponse2
            Si reponse2="non" Alors
                Ecrire "Faites une pause !"
            Finsi
        Sinon
            Ecrire "Prenez un café !"
        FinSi
        Ecrire "L'algorithmie c'est super !"
    Fin
