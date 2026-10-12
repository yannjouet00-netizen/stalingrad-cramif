# CRAMIF — vérification de la première étape enregistrée

Copie relue : `/Users/yannjouet/Documents/01_VLAU/Stalingrad/modele/Stalingrad_CRAMIF_travail.blend`, enregistrement du 10 octobre 2026 vers 22 h 45. Lecture indépendante, sans sauvegarde ni modification du fichier.

**Cette étape est vérifiée pour les trois ajouts de toiture retenus. Cela ne certifie ni les façades complètes de CRAMIF ni une livraison Enscape.**

- Exactement trois objets ajoutés : `CRAMIF_TOIT_2505947_1`, `CRAMIF_TOIT_2505950_4`, `CRAMIF_TOIT_2505950_5`. Les candidats 2 et 3 réservés au contrôle ne sont pas présents.
- 48 sommets, 30 faces natives et 84 triangles : trois solides fermés, zéro arête ouverte ou non-manifold, orientations appariées et volumes signés positifs.
- Les trois emprises restent dans les corps porteurs de la parcelle source `750065209`. Raccord volontaire de 20 mm sous les toits porteurs.
- Écarts recalculés entre triangles natifs et classe 6, à 0,5 m des bords : médianes 1,5 / 1,1 / 1,8 cm ; p95 6,0 / 3,7 / 5,1 cm. Cela caractérise l'accord au nuage, pas une précision absolue. Le test plus proche des bords par cases de 0,5 m donne des p95 de 12,7 / 3,7 / 10,8 cm.
- Propriétés présentes : source et date, parent, plan supérieur mesuré, emprise estimée, incertitude horizontale non qualifiée, raccord documenté. Les fonctions techniques ne sont pas inventées. Matériau uniforme, aucune texture ajoutée à ces objets.
- **Anciennes scènes 00–05 inchangées** pour géométrie, transformations sauvegardées, propriétés et matériaux. **Tout le contexte V3 et les huit corps CRAMIF antérieurs inchangés**, mêmes critères. Aucune suppression d'objet. V3 passe de 10 242 à 10 245 objets maillés.
- Le SHA256 du fichier original `Stalingrad.blend` est identique à l'état initial. La copie est distincte.

Les matrices monde des objets d'une scène inactive ne sont pas toujours calculées par Blender à l'ouverture : une première comparaison brute a donc produit des faux écarts. Le contrôle final compare directement les transformations enregistrées, parentage compris : **zéro modification sur les 12 988 objets antérieurs**. Le rapport faisant foi est `final/verification_finale.json`, avec `final/transformations_sauvegardees.json` et `final/audit.json`.

## Interface — contrôle du code préparé

`/private/tmp/cramif_suivi/pro.html` : `exa=1` constant, `scale.z=1`, curseur d'exagération absent ; shaders de fenêtres/étages/meneaux absents ; bâti et sol uniformes. La route `/pro` du serveur temporaire lit ce fichier. Les détails de façade manquants sont indiqués dans l'interface. Des rides procédurales de l'eau et textures génériques de feuillage subsistent : ne pas affirmer que toutes les textures du rendu ont disparu. Contrôle statique effectué ; validation visuelle navigateur prise en charge par l'intégrateur.

## Limites conservées

Les bases anciennes enterrées restent une convention de prisme, non des sous-sols mesurés. Les deux émergences moins sûres sont exclues ; les fenêtres ne sont pas relevées. Le passage Château-Landon n'a pas fait l'objet d'un contrôle de gabarit ici. Arbres fidèles/Enscape : aucune recette nouvelle effectuée dans ce paquet. Aucun export Revit, SketchUp ou IFC réalisé par le contrôleur.
