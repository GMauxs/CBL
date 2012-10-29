Van den Branden Maxime - 3G12 - 2012

Projet Cobol
============
Sujet : gestion limitée d'un magasin.

Fichiers
--------
Les fichiers qui suivent sont à disposition sans aucune obligation de devoir les utiliser.

### CLIENT ###
Fichier indexé des clients du magasin.

**CLIENTR**

- `MATCLI`  - PIC X(5)  : Matricule du client
- `NOMCLI`  - PIC X(20) : Nom du client
- `PNOMCLI` - PIC X(15) : Prénom du client
- `ADRCLI`  - PIC X(30) : Adressen du client

Le matricule `MATCLI` est constitué de 2 caractères alphanumériques suivis de 3 caractères numériques formant le numéro d'ordre de 3 chiffres, à incrémenter pour tout nouveau client.

### ARTICLE ###
Fichier indexé des articles vendus par le magasin.

**ARTICLER**

- `NOART`    - PIC X(5)    : Identifiant de l'article (unique)
- `LIBART`   - PIC X(20)   : Libellé de l'article
- `TVAART`   - PIC 99      : Taux de T.V.A pour cet article
- `MINNBART` - PIC 9(3)    : Quantité minimale pour obtenir une réduction de 8%
- `PRIXART`  - PIC 9(4)V99 : Prix unitaire de l'article

L'identifiant `NOART` suit la même règle que le `MATCLI` du fichier `CLIENT`.
