Fichiers
========
Les fichiers qui suivent sont à disposition sans aucune obligation de devoir les utiliser.

CLIENT
------
Fichier indexé des clients du magasin.

### CLIENTR ###

- `MATCLI`  - PIC X(5)  : Matricule du client
- `NOMCLI`  - PIC X(20) : Nom du client
- `PNOMCLI` - PIC X(15) : Prénom du client
- `ADRCLI`  - PIC X(30) : Adressen du client

Le matricule `MATCLI` est constitué de 2 caractères alphanumériques suivis de 3 caractères numériques formant le numéro d'ordre de 3 chiffres, à incrémenter pour tout nouveau client.

ARTICLE
-------
Fichier indexé des articles vendus par le magasin.

### ARTICLER ###

- `NOART`    - PIC X(5)    : Identifiant de l'article (unique)
- `LIBART`   - PIC X(20)   : Libellé de l'article
- `TVAART`   - PIC 99      : Taux de T.V.A pour cet article
- `MINNBART` - PIC 9(3)    : Quantité minimale pour obtenir une réduction de 8%
- `PRIXART`  - PIC 9(4)V99 : Prix unitaire de l'article

L'identifiant `NOART` suit la même règle que le `MATCLI` du fichier `CLIENT`.

STOCK
-----
Fichier indexé donnant la quantité en stock pour chaque article du magasin.

### STOCKR ###

- `NOART`  - PIC X(5) : Identifiant de l'article
- `QTEART` - PIC 9(5) : Quantité de l'article disponnible en magasin

FIDELITE
--------
Fichier indexé du programme de fidélisation du magasin.

> Toutes les 5 factures, les clients ont droit à une remise de 5% du total de leurs 5 dernières factures. À l'issue de chaque 5ème facture, il faudra donc remettre à 0 les champs `NBFACT` et `TOTFACT`.

### FIDELITER ###

- `MATCLI`  - PIC X(5)     : Matricule du client
- `NBFACT`  - PIC 9        : Nombre de factures
- `TOTFACT` - PIC 9(10)V99 : Total facturé pour les `NBFACT` dernières factures

ARCHIVES
--------
Fichier indexé reprenant le montant facturé pour chacune des factures du magasin depuis un certain temps, les précédents ayant été rangées dans un autre fichier non mentionné ici.

### ARCHIVESR ###

- `MATCLI`   - PIC X(5)    : Matricule du client
- `NOFACT`   - PIC 9(4)    : Numéro de facture
- `MONTFACT` - PIC9(10)V99 : Montant facturé

Dans ce fichier, la clé est composée de `MATCLI`-`NOFACT`.
