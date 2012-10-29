Fichiers AS400
==============

Clause `SELECT`
---------------

    SELECT [OPTIONAL] nomFichier ASSIGN TO nomLiaison.

Le `nomFichier` correspond au nom utlisé dans le programme COBOL.
Le `nomLiaison` se présente sous la forme `DEVICE-nomDuFichier-option`, ici le nom du fichier correspond au nom réel du fichier. `DEVICE` peut prendre comme valeur :

- `PRINTER`
- `FORMATFILE`
- `DISK`
- `DATABASE`
- `WORKSTATION`

Data Division
-------------
