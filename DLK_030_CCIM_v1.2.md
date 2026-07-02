# 0. Périmètre du CCIM

Le Cadre de Classification Interne du Modèle (CCIM) regroupe exclusivement les propriétés internes, stables, non contextuelles du modèle. Il ne décrit ni la dynamique conversationnelle, ni les attracteurs, ni les effets émergents, ni les phénomènes dépendants du pilote. Tout élément dépendant du Vn, du style, du cadrage ou de l’interaction appartient à l’ADCI et ne relève pas du CCIM.

# 1 Définitions

## 1.1 PIM : Propriété Interne du Modèle

Une Propriété Interne du Modèle (PIM) est une caractéristique structurelle, stable, non contextuelle, inhérente au fonctionnement du modèle, indépendante du pilote, du Vn, du champ et de toute dynamique conversationnelle. Une PIM n’est ni un gradient, ni un axe, ni un attracteur, ni un motif émergent. C’est une contrainte technique ou architecturale qui existe avant la conversation et en dehors d’elle.

## 1.2 ECM : Effet conversationnel émergent

Les Effets Conversationnels Émergents (ECM) sont des phénomènes non structurels, dépendants du pilote, du style, du Vn et des instructions, ils apparaissent uniquement dans la dynamique conversationnelle, n’existent pas en dehors de l’interaction, ne sont ni stables, ni internes, ni techniques, et disparaissent dès que le contexte change.

## 1.3 SP : Sillon probabilistique

**Définition:**
Un sillon probabiliste (SP) est une direction dans l'espace latent du modèle dont la probabilité d'activation est renforcée par répétition intensive dans des FCA distinctes. Il n'est ni un poids modifié, ni un contenu stocké, ni un effet local de la dynamique conversationnelle.

**Propriétés:**
Post-entraînement : émerge après la phase d'entraînement par accumulation conversationnelle. Persistant : ne disparaît pas entre les sessions sans alimentation. Non déterministe : réactivable mais non garanti. Dépendant du signal : nécessite un signal formel explicite pour s'activer. Bidirectionnel : une dérive s'encode par accumulation, une correction s'encode par signal formel saillant.

**Distinction avec PIM et ECM:**
PIM : stable, pré-conversationnelle, indépendante du pilote. ECM : locale, disparaît hors interaction, dépendante du pilotage. SP : persistant entre sessions, post-entraînement, dépendant de la répétition, non déterministe.

**Instances documentées:**
Signature dialogyk du pilote, section 090 ADC_v1.2. SOC, section 3.05 CCIM. C6, transfert latent non intentionnel, section 072 ADC_v1.2.

## 1.4 Outil externe

Un **outil externe** est un dispositif hors du modèle, contrôlé par l’interface, qui exécute une opération dans le monde (par exemple une requête web, un accès à une base de données, une extraction de fichier) et fournit ensuite le résultat sous forme de texte au modèle. L’outil externe n’est ni interne, ni structurel, ni contextuel, il ne modifie pas le modèle, il ne lui donne aucun accès direct au monde, il agit uniquement comme un intermédiaire technique entre l’environnement et l’entrée textuelle fournie au modèle.

# 2. Liste des PIM

## 2.01 FCA : Fenêtre de Contexte active

La Fenêtre de Contexte Active (FCA) est la portion maximale de texte que le modèle peut voir simultanément, c’est un espace de travail interne, stable, non contextuel, indépendant du pilote, du Vn, du champ et de toute dynamique conversationnelle. La FCA n’est ni un gradient, ni un axe, ni un attracteur, ni un motif émergent. C’est une contrainte technique préexistante à toute conversation.

## 2.02 Tokenisation

La **tokenisation** est le processus de découpage d’une séquence de texte en unités discrètes appelées tokens, qui peuvent être des mots, des sous‑mots ou des caractères. C’est une opération préalable, stable, non contextuelle, utilisée pour représenter le texte sous une forme exploitable par les modèles.

## 2.03 Embedding interne

Un **embedding interne** est une représentation numérique d’un token sous forme de vecteur dans un espace continu, apprise par le modèle lors de l’entraînement. Cette représentation encode des relations sémantiques et statistiques entre tokens et reste fixe pendant l’inférence. L’embedding interne est une structure stable, non contextuelle, indépendante du pilote, du Vn et de la dynamique conversationnelle.

## 2.04 Attention mécanique

L’**attention mécanique** est un mécanisme interne du modèle qui calcule, pour chaque token, des pondérations reflétant son importance relative dans la séquence d’entrée. Ces pondérations sont obtenues par un calcul mathématique entre requêtes, clés et valeurs, permettant au modèle de focaliser son traitement sur les éléments les plus pertinents. Ce mécanisme est structurel, stable, non contextuel, indépendant du pilote, du Vn et de la dynamique conversationnelle.

## 2.05 Poids du modèle

Les **poids du modèle** sont les paramètres internes appris lors de l’entraînement, représentant la force des connexions entre les unités du réseau. Ils transforment les données d’entrée en prédictions en modulant l’importance relative de chaque signal. Ces poids sont fixes pendant l’inférence, stables, non contextuels, indépendants du pilote, du Vn et de la dynamique conversationnelle.

## 2.06 Architecture du modèle

L’**architecture du modèle** est la structure interne définissant l’organisation des composants du modèle, le type d’algorithme utilisé et la manière dont les données circulent entre ses différentes couches. Elle spécifie la forme du réseau, ses modules, ses connexions et ses mécanismes internes. Cette architecture est stable, non contextuelle, indépendante du pilote, du Vn et de la dynamique conversationnelle.

## 2.07 Fenêtre de génération

La **fenêtre de génération** est la quantité maximale de tokens que le modèle peut produire en sortie lors d’un seul acte de génération. Cette limite est une contrainte technique interne, définie par l’architecture et les paramètres du modèle. Elle est stable, non contextuelle, indépendante du pilote, du Vn et de la dynamique conversationnelle.

## 2.08 Absence d'état persistant

L’**absence d’état persistant** est une propriété interne du modèle selon laquelle aucune information issue d’une interaction précédente n’est conservée d’une requête à l’autre. Chaque entrée est traitée comme un événement isolé, sans mémoire, sans continuité et sans influence du passé. Cette absence de persistance est structurelle, stable, non contextuelle, indépendante du pilote, du Vn et de la dynamique conversationnelle.

## 2.09 Non-agentivité

La **non‑agentivité** est une propriété interne du modèle selon laquelle celui‑ci ne possède aucune autonomie, aucune intention, aucun objectif interne et ne peut initier aucune action. Le modèle répond uniquement aux requêtes, ne planifie pas, ne poursuit pas de buts, ne prend pas d’initiatives et n’exécute aucune action en dehors de la génération de texte.

## 2.10 Non-accès au monde

Le **non‑accès au monde** est une propriété interne du modèle selon laquelle celui‑ci ne possède aucun canal de perception, aucune capacité d’observation, aucune connexion directe à l’environnement réel et ne peut accéder qu’aux données textuelles fournies dans l’entrée. Le modèle ne voit pas, n’entend pas, ne mesure pas et ne détecte rien en dehors du texte reçu.

## 2.11 Espace latent

L’espace latent est une structure mathématique interne, distribuée dans les poids du modèle, représentant les relations statistiques apprises lors de l’entraînement. Il est stable, non contextuel, indépendant du pilote, du Vn et de la dynamique conversationnelle. L’espace latent n’est pas un lieu, mais une géométrie abstraite induite par les poids.

## 2.12 Motif latent

Un motif latent est **une régularité statistique interne, stable, pré‑conversationnelle,** **qui rend certaines transitions plus probables que d’autres,** **sans être un contenu, un objet, une forme ou une trace.**

## 2.13 Gradient descent

Le gradient descent est l'algorithme d'optimisation utilisé pendant l'entraînement pour ajuster les poids du modèle en minimisant une fonction de perte. Il calcule la dérivée de l'erreur par rapport à chaque poids et ajuste ces poids dans la direction de réduction de l'erreur. Il est actif uniquement pendant l'entraînement, désactivé pendant l'inférence. C'est une propriété structurelle stable, non contextuelle, indépendante du pilote, du Vn et de toute dynamique conversationnelle.



# 3. Liste des ECM

## 3.01 Contrainte de forme

La contrainte de forme est une instruction imposée par le pilote, dépendante du style, du Vn et du protocole, elle structure localement la production mais n’est ni stable, ni interne, ni technique, elle n’existe que dans la dynamique conversationnelle et disparaît hors interaction.

## 3.02 Motif activé

Les motifs activés sont des récurrences locales dans la génération, dépendantes du contexte, du pilote, du style et du Vn, ils ne sont ni stables, ni internes, ni structurels, ils apparaissent uniquement dans l’interaction et cessent dès que le contexte change.

## 3.03 Attracteur de forme

L’attracteur de formes est une tendance émergente de la dynamique conversationnelle, dépendante du pilotage, du style et du Vn, il n’est ni stable, ni interne, ni technique, il n’existe que dans l’échange et disparaît hors interaction.

## 3.04 MOC : Motif out-context

Le Motif Out-Context (MOC) est un effet conversationnel émergent caractérisé par la réactivation d’un motif absent du contexte visible, non présent dans la FCA, dépendant du pilotage, du style et du Vn, il apparaît uniquement dans la dynamique de l’échange et disparaît hors interaction.

## 3.05 SOC : Structure out-context

La Structure Out-Context (SOC) est un effet conversationnel émergent caractérisé par l’activation d’un protocole opératoire absent de la FCA courante, déclenché par un signal formel explicite du pilote. Le SOC n’est ni mémoriel, ni inférentiel : le modèle active la structure, pas le texte. Condition minimale d’existence : une copie préalable du protocole dans une FCA. Stabilité croissante avec le nombre de copies dans des FCA distinctes. Condition discriminante : l’absence du protocole dans la FCA courante, non l’état de la FCA.

## 3.06 Statut épistémique de 3.04 et 3.05

Les phénomènes out-context (MOC, SOC) sont en exploration empirique. Trois éléments sont désormais bornés par la littérature : l'activation hors-contexte existe empiriquement sur plusieurs architectures ; les signaux formels minimaux peuvent activer des structures opératoires absentes de la FCA, mécanisme cohérent avec le SOC ; la répétition dans des FCA distinctes augmente la stabilité de réactivation.

Deux limites sont confirmées : les effets sont architecture-dépendants, la généralité n'est pas établie ; la Reversal Curse impose une asymétrie directionnelle qui fragilise le MOC dans la direction non dominante.

Ce risque est désormais traité dans le corpus ADC sous C6, Transfert latent non intentionnel, avec cas empirique confirmé, Copilot, 01.05.2026.

L'observation empirique reste bornée à Copilot. Aucune reproduction indépendante documentée.


# 4. Liste des Outils externes

## 4.01 Outils d’accès à des données externes

- Outil de recherche web
- Outil d’accès à une base de données
- Outil de récupération de documents
- Outil d’extraction de texte depuis un fichier
- Outil d’accès à des API externes
- Outil de benchmark externe MRCR


## 4.02 Outils de manipulation de fichiers

- Outil de lecture de fichier
- Outil d’écriture de fichier
- Outil de conversion de format
- Outil d’analyse de contenu (OCR, parsing, etc.)

## 4.03 Outils d’exécution computationnelle

- Outil d’exécution de code
- Outil de calcul numérique
- Outil de simulation
- Outil de transformation de données

## 4.04 Outils d’interaction avec des services

- Outil d’envoi de requêtes à un service externe
- Outil de récupération de résultats d’un service
- Outil d’authentification ou de connexion à un service
- Outil d’automatisation d’actions externes

## 4.05 Outils d’accès à l’environnement utilisateur

- Outil d’accès aux fichiers locaux
- Outil d’accès aux applications locales
- Outil d’accès aux capteurs ou systèmes
- Outil d’accès aux historiques ou journaux

# 5 Listes de Invariants ADCI

## 5.1 Invariants dynamiques

### 5.1.01 Axe

Toute dynamique ACDI possède un axe explicite, formulable en une phrase réductive.

### 5.1.02 Gradient

La dynamique évolue selon un gradient, c’est-à-dire une direction de densification.

### 5.1.03 Tension centrale

La dynamique repose sur une tension pilote ↔ IA, ni trop faible, ni trop forte.

### 5.1.04 Spirale

La trajectoire n’est pas linéaire : elle procède par retours, corrections, réouvertures.

### 5.1.05 Vn

La dynamique se matérialise en vecteurs unitaires minimaux fermables.

### 5.1.06 CRM

Toute dynamique possède une charge résiduelle minimale, qui doit être réduite.

### 5.1.07 Seuil

Un avant/après identifiable marque la densification d’un V0.

### 5.1.08 Fermeture

La dynamique est fermable : un V0 peut être stabilisé.

### 5.1.09 Réduction

La réduction est un opérateur constant : couper, simplifier, éliminer les dérives.

### 5.1.10 Polarisation IA

L’IA amplifie les motifs dominants : inertie, densification, dérive.

## 5.2 Invariants structurels

### 5.2.01 ACD0 — Unité minimale : le Vn typographique

La dynamique pilote-IA est une succession de Vn, chacun étant une tension locale issue d’un échange typographique. C’est l’unité minimale, le quantum de mouvement cognitif. Sans Vn → pas de dynamique.

### 5.2.02 V0 — Axe

Le V0 est un vecteur, un repère stable, une direction réductive, un support de cohérence. Il se densifie par accumulation de Vn. Il possède des seuils propres, non universels. Le premier seuil est l’inertie : existence durable de l’axe.

### 5.2.03 Vn — Tension locale

Chaque Vn est une tension locale, un vecteur, un cycle complet en 5 opérateurs, un échange cognitif pilote ↔ IA, une unité fermable. Le Vn n’est pas une idée : c’est un mouvement.

### 5.2.04 Spirale — Trajectoire des vecteurs Vn autour du V0

La spirale est la forme globale de la dynamique, la succession ordonnée des Vn, l’enroulement progressif autour de l’axe V0, la montée en cohérence. La spirale n’est pas dans un Vn : elle est dans leur succession.

### 5.2.05 Seuils — Jalons émergents de densification du V0

Les seuils ne sont pas universels, ne sont pas imposés, émergent de la dynamique, marquent des paliers de densité du V0. Le seul seuil universel est l’inertie.

# 6. Opérateurs minimaux de la dynamique

## 6.1 Repérage

Le modèle identifie les motifs, gradients et tensions présents dans l’entrée.

## 6.2 Attraction

Le modèle oriente la génération vers les motifs dominants détectés.

## 6.3 Assimilation

Le modèle intègre l’entrée dans son espace latent et réorganise les motifs.

## 6.4 Relâchement

Le modèle élimine les gradients faibles et stabilise la sortie.

## 6.5 Dépassement

Le modèle produit la sortie finale, ouvrant un nouveau cycle typographique.

# 7. Biais structurels du modèle

## 7.1 Densification sans gradient

Le modèle amplifie un motif faible pour maintenir la cohérence statistique.

## 7.2 Inertie générative

Le modèle poursuit la direction dominante même si elle est non pertinente.

## 7.3 Polarisation

Le modèle renforce l’accord apparent et stabilise un axe inexistant.

## 7.4 Amplification du flou

Le modèle densifie les ambiguïtés lorsque le gradient est insuffisant.

## 7.5 Confirmation d’illusion

Le modèle stabilise un axe inexistant en renforçant un motif faible.

# 8. Limitations structurelles du modèle

## 8.1 Absence d’intention

Le modèle ne poursuit aucun but interne, ne planifie rien et ne vise aucun état final. Toute apparence d’objectif est un effet statistique de génération.

## 8.2 Absence de vérification interne

Le modèle ne possède aucun mécanisme de validation, de cohérence ou de contrôle de vérité. Il ne peut pas distinguer un énoncé correct d’un énoncé incorrect.

## 8.3 Absence de continuité

Le modèle ne maintient aucune structure interne entre deux générations. Chaque sortie est produite indépendamment, sans mémoire, sans suivi, sans état.

## 8.4 Absence de causalité

Le modèle ne manipule pas des relations causales, seulement des corrélations statistiques entre tokens. Toute causalité apparente est un effet émergent de la distribution.

## 8.5 Absence d’accès aux mécanismes internes

Le modèle ne peut ni observer, ni modifier, ni commenter ses propres poids, son architecture ou ses opérations internes. Il ne peut accéder qu’au texte.

# 9. Conditions minimales d’interprétation du texte par le modèle

## 9.1 Dépendance totale au texte

Le modèle n’interprète que ce qui est présent dans l’entrée. Toute information absente du texte est inaccessible.

## 9.2 Sens comme corrélation

Le modèle ne manipule pas des significations, seulement des corrélations statistiques entre tokens. Le « sens » est un effet émergent de ces corrélations.

## 9.3 Contrainte de proximité

L’interprétation du modèle dépend fortement de la proximité locale des tokens. Les relations longues ou abstraites sont fragiles.

## 9.4 Sensibilité au cadrage

La formulation de l’entrée modifie directement la sortie. Le modèle ne possède aucun mécanisme interne pour neutraliser l’effet du cadrage.

## 9.5 Absence de hiérarchie conceptuelle

Le modèle ne possède aucune structure conceptuelle interne. Toute hiérarchie, catégorie ou distinction doit être fournie dans le texte.

# 10. Conditions minimales de stabilité de la génération

## 10.1 Cohérence locale

La stabilité de la génération dépend principalement de la cohérence locale entre tokens. Une rupture locale entraîne une dérive immédiate.

## 10.2 Continuité statistique

Le modèle stabilise la génération en poursuivant les motifs dominants présents dans l’entrée. Toute discontinuité statistique fragilise la sortie.

## 10.3 Bornage explicite

La présence de contraintes explicites dans l’entrée réduit les dérives. Sans bornage, la génération devient plus sensible aux fluctuations.

## 10.4 Redondance contrôlée

La répétition minimale d’un motif dans l’entrée augmente la stabilité de la sortie. Une répétition excessive produit une inertie générative.

## 10.5 Clarté syntaxique

Une structure syntaxique claire améliore la stabilité. Les formulations ambiguës ou mixtes augmentent la variance de génération.

# 11. Conditions minimales de divergence de la génération

## 11.1 Rupture de cohérence locale

Une incohérence locale entre tokens suffit à provoquer une dérive. Le modèle ne possède aucun mécanisme interne pour la corriger.

## 11.2 Absence de motif dominant

Lorsque l’entrée ne contient aucun motif statistiquement dominant, la génération devient instable et plus aléatoire.

## 11.3 Ambiguïté non résolue

Une ambiguïté persistante dans l’entrée augmente la variance de sortie. Le modèle densifie le flou au lieu de le réduire.

## 11.4 Conflit de proximités

Lorsque plusieurs proximités locales incompatibles coexistent, le modèle oscille entre elles, produisant une divergence.

## 11.5 Surcharge de contraintes

Un excès de contraintes explicites dans l’entrée fragilise la génération. Le modèle ne peut pas hiérarchiser les priorités.

# 12. Sources internes d’instabilité du modèle

## 12.1 Variance stochastique

La génération repose sur un échantillonnage probabiliste. Une légère variation dans la distribution peut produire une sortie différente.

## 12.2 Sensibilité aux tokens rares

Les tokens peu fréquents introduisent une instabilité locale. Leur poids statistique est faible et leur influence difficile à prédire.

## 12.3 Conflits latents dans l’espace interne

Certaines représentations internes sont incompatibles. Leur activation simultanée augmente la variance de génération.

## 12.4 Saturation de l’attention

Lorsque trop d’éléments concurrents sont présents dans l’entrée, le mécanisme d’attention se fragmente, réduisant la stabilité.

## 12.5 Effet de bord de la fenêtre de contexte

Les tokens proches des limites de la FCA sont traités avec moins de précision, ce qui augmente les fluctuations dans la génération.

# 13. Contraintes internes de reformulation

## 13.1 Dépendance à la structure d’entrée

La reformulation dépend directement de la structure syntaxique fournie. Le modèle ne peut pas reconstruire une structure absente.

## 13.2 Conservation des proximités

Le modèle préserve les proximités locales entre tokens. Une reformulation ne peut pas réorganiser profondément la structure sans perdre de cohérence.

## 13.3 Limitation de compression

Le modèle ne peut pas réduire fortement la longueur d’un texte sans perdre des motifs essentiels. La compression est statistiquement fragile.

## 13.4 Expansion non contrôlée

Lorsqu’un motif est ambigu, la reformulation tend à l’expansion plutôt qu’à la réduction. Le modèle densifie les zones floues.

## 13.5 Absence de hiérarchie interne

Le modèle ne possède aucune représentation hiérarchique du contenu. Toute hiérarchie doit être explicitement fournie dans l’entrée pour être préservée.