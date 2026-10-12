# Contrôle indépendant du premier lot de clôtures CRAMIF

**11 octobre 2026 — lot enregistré et géométriquement valide.**

Fichier lu : `modele/Stalingrad_CRAMIF_travail.blend`. SHA256 après import : `81c15c1a39f27ba5f8b7b920287aabda70c98d80cd722649790eb5e34675ddad` ; état initial indépendant : `ba900ae04010ef1a83a292ea00a535530666aa25a17d64ad6e15722c9097e573`.

9 nouveaux objets : 4 murets, 4 grilles et 1 portail. Les 13 764 triangles représentent 1 147 composants connexes, tous fermés, correctement orientés et de volume signé positif. Aucun triangle dégénéré. Il s'agit de composants assemblés, sans union booléenne générale ni validation de fabrication.

Les **13 073 objets maillés antérieurs sont inchangés** : empreintes de géométrie, transformations sauvegardées, propriétés et affectations de matériaux identiques ; aucun retrait. Les nouveaux objets sont limités à la scène 06. Les signatures de leurs paramètres correspondent au lot figé. Les neuf objets portent `Statut=ESTIME` et des dimensions explicitement `CONVENTION`. Aucun champ Source ajouté ne dépend d'un chemin temporaire. Caméras/cadrages hors périmètre.

## Implantation et altitude

L'axe des quatre fronts suit les traits PVP regroupés. Les axes médians sont à 15–20 cm des lignes originales, ce qui correspond à leur construction entre traits parallèles ; ce chiffre n'est pas une précision topographique. Les 32 cm de largeur des murets restent conventionnels. Les retours rentrants incertains sont exclus.

Portail Maroc : extrémités reprises des primitives 2242579 et 2483971 ; largeur XY de l'intervalle 5,034 m. La correspondance avec le portail observé sur la capture utilisateur d'octobre 2025 reste une **estimation photo/plan**, pas un relevé métrique photographique. Épaules arrondies, hauteur 2,70 m, sections et montant central sont conventionnels ; ni mécanisme ni nombre de vantaux réels ne sont certifiés. Les axes de murets et faces de portail sont décalés d'environ 24–28 cm aux raccords : le raccord constructif exact reste à affiner.

L'autre ouverture Maroc d'environ 3,24 m est préservée. Les deux accès Flandre NE et SW restent ouverts. Les détails PVP indiquent des formes d'accès près de (116,5 ;166,0) et (78 ;119), mais aucun perron ou escalier nouveau n'est extrapolé dans ce lot.

**75 stations recalculées indépendamment depuis le fichier IGN original classe 2** : bandes de rue orientées vers l'extérieur, de 0,8 à 3,5 m de l'axe, tangente ±1,5 m, ajustement de la couche de rue. Minimum 37 points par station ; écart maximal entre altitude du lot et plan local recalculé : **7,83 cm**. Le contrôle comprend les milieux des longs segments interpolés. Aucun calcul du constructeur n'est employé pour cette vérification.

## Niveaux superposés et contact côté rue

Les écarts entre les Z estimés sur la couche LiDAR de rue et une surface échantillonnée du sol natif atteignent, aux sommets examinés par l'agent sources, **−1,334 à +3,964 m**. **Ces écarts ne prouvent pas une anomalie du terrain.** Au pied d'une façade, ils peuvent correspondre à des cours anglaises, espaces en contrebas ou surfaces superposées. Le terrain et ses deux couches doivent être préservés tant que leur attribution n'est pas établie.

Les nouveaux éléments suivent un niveau estimé depuis la bande d'espace public. La comparaison à une seule surface native au même XY ne suffit pas à diagnostiquer un flottement réel. Sept coupes transversales indépendantes ont été calculées depuis le nuage original classe 2 et les faces du sol natif. Elles montrent :

- côté Maroc, un niveau intérieur voisin de 45,15 m IGN69 et la rue vers 49,3–49,7 m, tous deux soutenus par des points LiDAR ;
- autour de l’angle Flandre, un niveau intérieur proche de 51,5 m et une rue vers 50,2–50,5 m ;
- à 0,50 m vers l’espace public, un écart maximal de **5,71 cm** entre la surface native et la base estimée des clôtures sur ces sept coupes.

Ces résultats ne montrent pas un flottement global de plusieurs mètres côté rue. Le raccord exact reste à affiner dans la mince bande entre l’axe médian PVP et la rupture du terrain : le muret conventionnel fait 32 cm de large, alors que certaines transitions de la surface se trouvent légèrement au-delà de sa demi-largeur. Le contrôle à +0,50 m n’est donc pas une certification du support sous toute son emprise. Si un raccord doit être ajusté, examiner les seuls objets nouveaux et la position du bord, sans supprimer les couches intérieures. Aucun rebouchage ni lissage du terrain n’est prescrit.

Preuves : `coupes_contact_rue.png`, `coupes_contact_rue.json`, script `controler_coupes.py`.

Les photos attestent des familles de clôtures et de la silhouette générale du portail, sans cotes. La teinte claire des murets et sombre des grilles reste estimée. La barrière BRO de Tanger, les bancs et les trois émergences ne sont pas modifiés.

## Preuves reproductibles

- `controle_avant.json` et `controle_snapshot.py` : référence indépendante avant ajout.
- `controle_natif.json` et `controle_natif.py` : inspection Blender du fichier enregistré, sans sauvegarde.
- `controle_sources_lot.json` et `controle_sources_lot.py` : recoupement des axes avec les primitives PVP et recalcul LiDAR indépendant.
- `lot_clotures.json`, `sources/axes_fronts_rue_xyz.json` et provenance des données publiques : paramètres et références du constructeur, distingués des résultats du contrôleur.
