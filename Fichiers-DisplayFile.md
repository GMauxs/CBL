## Les Fichiers DisplayFile DSPF ###
Fichiers écran:
  
- non subfile
- subfile

### Les sous-fichiers (non SUBFILE) ###

Un display file ou fichier écran (type DSPF) est constitué d’un ou plusieurs écrans
(panels), chacun d’eux étant décrit par un format d’enregistrement dans le code DDS
du fichier.

L’organisation d’un fichier DSPF est obligatoirement TRANSACTION et une
CONTROL-AREA peut y être associée pour permettre une utilisation simplifiée des
PF’s keys. Le paragraphe FILE-CONTROL peut donc avoir l’aspect suivant pour un
display file :
	
	SELECT monEcran ASSIGN TO WORKSTATION-ECRAN
		ORGANIZATION IS TRANSACTION
		CONTROL-AREA IS F-KEYS.
		
Pour cet exemple, monecran est le nom du fichier écran dans le programme Cobol et
ECRAN est le nom de l’objet ECRAN de type *FILE et d’attribut DSPF. F-KEYS est
le nom d’une zone déclarée en working-storage section.

Pour une utilisation plus sécurisée de vos fichiers écrans:
	- Dans INPUT-OUTPUT SECTION de la DATA DIVISION, déclarer un masque assez
	grand pour contenir le plus grand format d'enregistrement du fichier DSPF.
	(~$ DSPFD nomFichier pour voir taille minimale à prévoir)
	
	FILE SECTION.
	FD monEcran.
	01 masque		PIC X(100).
	
La CONTROL-AREA est à déclarer en WORKING-STORAGE SECTION.
Deux types de formats: variable (INPUT, OUTPUT, I-O) et non variable (pas de DDS).

Pour les variables:
	COPY DDS par format et type de variable (I, O, I-O)