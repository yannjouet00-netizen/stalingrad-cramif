# Contrôle indépendant — abords CRAMIF, 10 octobre 2026

## État du fichier natif lu

La dernière lecture de `Stalingrad_CRAMIF_travail.blend`, SHA256 `6706f87456e3745edb26ff46453a31d1d832e28f4df6406bb107b7e360e30667`, retrouve **13 048 objets maillés : 12 991 objets préexistants et 57 nouveaux composants de barrière.** Les 3 420 triangles ajoutés forment des composants fermés, orientés de façon cohérente et de volume signé positif. Tous portent le statut CONVENTION ; un seul ID source est utilisé. Les bornes ambiguës et la rampe sont absentes des ajouts. Le lot est bien enregistré dans cet état disque.

Les empreintes géométriques, propriétés et affectations de matériaux des 12 991 objets précédemment contrôlés sont identiques. Les anciennes scènes n'ont aucun ajout ni retrait ; les transformations sauvegardées des objets originaux sont identiques à `Stalingrad.blend`. Caméras/cadrages hors périmètre.

Résultats machine : `controle_natif_barriere.json`. Contrôle Blender strictement en lecture seule, aucune sauvegarde.

## Lot source et altitudes

Un seul objet source `PVP_BARRIERE_5004955`, composé de 24 primitives PVP et dédoublonné en un axe de 12,0005 m. Ce chiffre mesure l'axe du symbole, sans certification de longueur physique. Coordonnées locales Lambert93 E−653700, N−6865100 ; altitude IGN69. Extrémités XY : (−8,254 ; 158,189) et (−15,295 ; 148,472), rue de Tanger au contact CRAMIF.

L'axe est densifié en **26 stations / 25 segments**, pas 25 stations. Z du lot : 49,4400 à 49,5109 m, interpolé sur le sol natif et donc ESTIMÉ. Recalcul indépendant depuis le fichier original IGN classe2, rayon horizontal 1 m et couche ±0,50 m : au moins 30 points par station, écart absolu maximal à la médiane locale 0,0518 m. Ce test valide la cohérence avec le sol observé, pas une précision altimétrique absolue. Voir `controle_independant_z.json` et `controler_altitudes.py`.

Le lot paramétrique décrit 57 composants, 7 poteaux, 2 lisses, hauteur 1 m, rayons 25/22 mm et entraxe maximal 2,1 m. **Ces paramètres et la matière métallique sont CONVENTIONNELS**, non relevés. La fermeture de chaque composant a été vérifiée dans le natif. Les intersections intentionnelles entre lisses et poteaux ne constituent pas une union booléenne étanche globale.

## Alerte d'interprétation du symbole

La charte officielle PVP du 16 juin 2017, page PDF 26 / B-23, représente **BRO — barrière roulante** par un trait avec dents alternées. Les 24 primitives de notre groupe correspondent visuellement à ce symbole. Le symbole **GCO — garde-corps** est différent (épaississements sur le trait). L'export ne fournit toutefois aucun champ de sous-type : conserver `BARRIERE` comme classe attestée et `BRO probable, interprétation morphologique` comme estimation. Aucune fonction de sécurité, mécanisme précis ou roulette particulière ne peut être déclarée mesurée. Le lot ne doit pas être décrit comme un garde-corps relevé. Comparaison vérifiable dans `charte-026.png` et `plan_mobilier_pvp.png`.

Sources primaires :
- [Jeu PVP Ville de Paris](https://opendata.paris.fr/explore/dataset/plan-de-voirie-mobiliers-urbains-bornes-barrieres-potelets/), enregistrements horodatés le 12 septembre 2026. Cet horodatage n'est pas une date de relevé terrain.
- [Charte des symboles PVP, 16 juin 2017](https://opendata.paris.fr/api/datasets/1.0/plan-de-voirie-mobiliers-urbains-bornes-barrieres-potelets/attachments/plan_voirie_paris_cahier_des_normes_partiea_20170616_pdf), p26/B-23.

## Exclusions et données complémentaires

Les 45 groupes BORNE restent exclus de la représentation 3D : le niveau PVP rassemble des objets différents. Les dix symboles allongés devant l'avenue de Flandre évoquent des arceaux de deux-roues ; les traiter comme des potelets serait injustifié. Les carrés au nord restent sans identification sûre. Les dimensions des symboles ne suffisent pas à construire les objets physiques.

La rampe de la cour sud possède un profil altimétrique documenté par l'agent sources (environ 46,3 → 43,42 m sous le niveau voisin de 50 m), mais ni contour complet ni largeur suffisamment établis : aucun solide ni remplacement de sol autorisé par cette seule preuve.

Le [compte rendu de marche exploratoire Tanger du 21 novembre 2023](https://cdn.paris.fr/paris/2024/03/25/cr-marche-explo-2111-FTMe.pdf), p18–19, atteste une double rangée de barrières devant l'école rue de Tanger (entre le 17 et la rue du Département). Il ne fournit pas une implantation métrique. Il distingue ces constats des propositions de végétalisation. L'absence de bancs déplorée ne permet pas d'ajouter des bancs.

Les captures utilisateur 22.46.25/32/44 illustrent le comportement de l'ancien modèle ; elles ne constituent pas un relevé de mobilier. Aucun escalier, muret, banc ou garde-corps supplémentaire n'est implanté sur cette base.

## Second lot documenté, en préparation

Le [jeu PVP jardinières, bancs et corbeilles](https://opendata.paris.fr/explore/dataset/plan-de-voirie-mobiliers-urbains-jardinieres-bancs-corbeilles-de-rue/) contient 41 primitives à proximité immédiate, regroupées en 16 éléments. Cinq groupes de six traits correspondent visuellement au symbole **BA2 — banc double** du cahier officiel p60/B57 : rectangle et deux lignes parallèles internes. Les empreintes symboliques sont proches de 2,30 × 0,80 m. L'identification morphologique et les dimensions XY restent ESTIMÉES, aucune hauteur, section ni matière n'est relevée. L'horodatage des enregistrements est le 14 septembre 2026, sans garantie de date terrain.

Implantations locales des cinq candidats : (96,512 ; 131,991), (105,710 ; 133,605), (119,038 ; 158,646), (128,027 ; 160,113), (70,924 ; 91,969). IDs et axes dans `bancs_pvp_xy.json`, preuve graphique `cinq_bancs_symboles.png` et `charte-060.png`. Les onze autres groupes, circulaires, demeurent non attribués : l'export ne conserve pas les lettres du symbole permettant d'identifier une poubelle. Aucun banc ni corbeille supplémentaire n'a été certifié dans le natif à ce stade.
