# TP 7 : Activer le 2nd-level cache, mesurer avant/après, supprimer N+1 via JOIN FETCH et entity graph 
## Description :
#### Ce tp démontre l’optimisation des performances d’une application utilisant JPA avec Hibernate comme implémentation.Il met en pratique :
#### - L’activation et l’utilisation du cache de second niveau
#### - La mesure des performances avant/après optimisation
#### - L’identification et la résolution du problème N+1
#### - L’utilisation de JOIN FETCH
#### - L’utilisation des Entity Graphs
#### - L’analyse des statistiques Hibernate
#### Base de données utilisée : H2 (en mémoire)
#### Implémentation du cache : Ehcache
## Objectifs :
#### - Comprendre le fonctionnement du cache de second niveau dans Hibernate
#### - Activer et configurer le cache avec Ehcache
#### - Mesurer les performances via les statistiques Hibernate
#### - Identifier un problème N+1
#### - Corriger le problème N+1 avec : JOIN FETCH , Entity Graph
#### - Comparer les performances avec et sans cache
## Structure du projet : 

<img width="1097" height="851" alt="image" src="https://github.com/user-attachments/assets/cc84c265-5c99-4276-abb4-8af632e74395" />

## Console ( quelques captures ) :

<img width="1853" height="913" alt="Capture d’écran 2026-03-04 194932" src="https://github.com/user-attachments/assets/fcc46c0f-3958-41a3-9672-78437f52fc9a" />

<img width="1840" height="828" alt="Capture d’écran 2026-03-04 195037" src="https://github.com/user-attachments/assets/f7ca11cb-9dfb-4a35-bcc1-e9429bcd47d6" />

<img width="1857" height="912" alt="Capture d’écran 2026-03-04 195121" src="https://github.com/user-attachments/assets/72d7ac54-e983-461b-873b-0c67eb8d44f3" />

<img width="1857" height="913" alt="Capture d’écran 2026-03-04 195202" src="https://github.com/user-attachments/assets/b3c0be9f-3483-4f05-bfe8-c62df8914422" />

<img width="1857" height="918" alt="Capture d’écran 2026-03-04 195222" src="https://github.com/user-attachments/assets/dd7b5cf7-9e58-4eaf-a43c-b8fb71749f49" />

<img width="1857" height="905" alt="Capture d’écran 2026-03-04 195245" src="https://github.com/user-attachments/assets/4cf64aa7-9b12-489b-bd87-722d9ee00736" />

<img width="1847" height="907" alt="Capture d’écran 2026-03-04 195314" src="https://github.com/user-attachments/assets/75632ce3-f4b4-4901-865a-75e0dde89369" />

<img width="1852" height="908" alt="Capture d’écran 2026-03-04 195346" src="https://github.com/user-attachments/assets/8c3da90a-fbfd-4f1a-9c07-3724f922e78e" />

<img width="1865" height="923" alt="Capture d’écran 2026-03-04 195404" src="https://github.com/user-attachments/assets/42020b3b-cff3-474d-b4a1-297456b92088" />

<img width="1846" height="907" alt="Capture d’écran 2026-03-04 195543" src="https://github.com/user-attachments/assets/79f0315c-2890-46f4-bab4-292f9dfc1e00" />

<img width="1855" height="911" alt="Capture d’écran 2026-03-04 195604" src="https://github.com/user-attachments/assets/b241b0ab-943e-47d8-9ce1-afb949671897" />

<img width="1853" height="918" alt="Capture d’écran 2026-03-04 195625" src="https://github.com/user-attachments/assets/ecf8b51a-0394-4627-8740-3d6dcf048ff1" />

<img width="1851" height="932" alt="Capture d’écran 2026-03-04 195645" src="https://github.com/user-attachments/assets/08c32853-b5e9-448b-9ce5-1a7a943966bc" />

<img width="1856" height="932" alt="Capture d’écran 2026-03-04 195811" src="https://github.com/user-attachments/assets/698f7456-aa5f-4b10-b449-eb505605484f" />

<img width="1852" height="927" alt="Capture d’écran 2026-03-04 195837" src="https://github.com/user-attachments/assets/e2fafca6-ad80-431f-b91f-2ee82bc7d0f6" />

<img width="1860" height="922" alt="Capture d’écran 2026-03-04 195857" src="https://github.com/user-attachments/assets/c825ca43-fb9d-4be4-920e-5ea551aabceb" />

<img width="1851" height="927" alt="Capture d’écran 2026-03-04 195918" src="https://github.com/user-attachments/assets/5b7ff31c-5912-4617-a612-faf5ac151593" />

<img width="1850" height="908" alt="Capture d’écran 2026-03-04 195941" src="https://github.com/user-attachments/assets/9d58f707-0262-4d32-9a76-1cc6125c4795" />

<img width="1847" height="896" alt="Capture d’écran 2026-03-04 200000" src="https://github.com/user-attachments/assets/c2864169-b79c-44ec-b012-a4a33809736d" />

<img width="1847" height="907" alt="Capture d’écran 2026-03-04 200021" src="https://github.com/user-attachments/assets/dbf8a15a-696e-42cc-9bc1-8f48d02c9f95" />

<img width="1845" height="907" alt="Capture d’écran 2026-03-04 200044" src="https://github.com/user-attachments/assets/aceb3ce5-6c8e-4165-bc4e-1a2e7529664b" />

<img width="1845" height="926" alt="Capture d’écran 2026-03-04 200106" src="https://github.com/user-attachments/assets/6ad99a9a-af03-4194-9136-5590ee7bf5d1" />

<img width="1855" height="903" alt="Capture d’écran 2026-03-04 200126" src="https://github.com/user-attachments/assets/89f12636-c8ea-43f0-b54e-f0a8207ef3f6" />

## Conclusion : 
#### Ce TP démontre clairement l’impact des optimisations JPA/Hibernate sur les performances.
#### Les points clés retenus :
#### - Le problème N+1 peut gravement dégrader les performances.
#### - JOIN FETCH et Entity Graph permettent un chargement optimisé des relations.
#### - Le cache de second niveau réduit les accès répétés à la base de données.
#### - Les statistiques Hibernate sont essentielles pour analyser les performances.
#### Ces techniques sont indispensables pour toute application professionnelle utilisant JPA/Hibernate avec des relations complexes et un volume de données important.


