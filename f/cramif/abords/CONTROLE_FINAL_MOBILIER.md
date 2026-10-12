# Contrôle final du mobilier CRAMIF — 10 octobre 2026

**Lot final présent dans le natif et contrôlé.** Fichier lu : `modele/Stalingrad_CRAMIF_travail.blend`, SHA256 `7a3453df765eebf0fdf144b8947a0d383a8500ef1d8525fb9b2275b134987fdc`.

13 073 objets maillés au total : 12 991 préexistants, 57 composants de barrière et 25 composants pour cinq bancs doubles. Les 3 720 triangles ajoutés (3 420 + 300) appartiennent à des solides fermés, de volume signé positif, avec orientations cohérentes. Aucun ajout de borne ambiguë, de rampe ni de corbeille.

Les empreintes des maillages, propriétés et affectations de matériaux des 12 991 objets antérieurs sont identiques à l'état contrôlé après les trois émergences de toiture. Matériaux existants inchangés. Scènes 00–05 : aucun ajout/retrait ; ajouts limités à la scène 06. Transformations sauvegardées des objets originaux inchangées par rapport à `Stalingrad.blend`. Cadrages et caméras hors périmètre.

Les 82 composants portent le statut `CONVENTION`. `Type_element` distingue 57 `barriere` et 25 `banc_double`. La barrière porte désormais `Type_interprete` précisant BRO probable d'après le symbole PVP et l'absence de fonction de garde-corps certifiée. Les bancs portent BA2 probable / identification morphologique estimée. Les dimensions, sections, formes détaillées et matériaux sont explicitement conventionnels. Aucun champ Source des ajouts ne pointe encore vers `/private/tmp` ; les altitudes renvoient aux chemins persistants relatifs du projet.

Contrôle altimétrique **recalculé indépendamment depuis le nuage original IGN classe 2**, sans employer les mesures du générateur :

| Lot | Stations | Points locaux minimum | Écart absolu maximal à la médiane locale |
|---|---:|---:|---:|
| Barrière | 26, soit 25 segments | 30 | 5,18 cm |
| Cinq bancs, centres et extrémités | 15 | 21 | 10,99 cm |

Méthode : disque horizontal de 1 m et couche verticale ±0,50 m autour du sol prévu. Les Z sont estimés par interpolation du terrain natif ; ces écarts vérifient une cohérence locale et ne certifient pas une exactitude absolue. Les bancs ont des assises horizontales, appuis à des Z interpolés sur l'axe ; le contact surfacique aux quatre coins n'est pas contrôlé. Les composants se recouvrent aux assemblages et ne constituent pas une union booléenne unique prête à fabriquer.

La datation PVP indique un horodatage de publication/enregistrement (12 septembre 2026 barrière, 14 septembre bancs), pas une date de relevé terrain. L'identification BRO/BA2 est issue de la comparaison des primitives à la charte PVP du 16 juin 2017, p26/B23 et p60/B57. Les longueurs/empreintes des symboles servent de base de représentation sans certification des dimensions physiques.

Preuves machine : `controle_natif_barriere.json` (contient désormais le lot final complet), `controle_independant_z.json`, `controle_independant_z_bancs.json`. Scripts reproductibles : `controler_barriere_native.py` sous le dossier de contrôle, `controler_altitudes.py`, `controler_altitudes_bancs.py`. Audit du fichier sur disque en lecture seule ; aucun enregistrement Blender effectué par le contrôleur.
