---
epoch: 1790854192991
mode: agent
backendId: opencode
sessionId: "ses_f08e21770ffeoWP7r3g20o6fLi"
agentLabel: "Comprendre les liaisons mécaniques"
usage: '{"usedTokens":16964,"contextWindow":200000,"updatedAt":1790854435948}'
tags:
  - copilot-conversation
---

**user**: Aide moi s'il te plait, je comprend que dalle
[Timestamp: 2026/10/01 13:29:52]

**ai**: La section "Modélisation des mécanismes" est en fait un cours de **cinématique** — voici ce que ça veut dire, simplement.

## 1. Le principe : un solide = 6 degrés de liberté (DDL)

En 3D, un corps solide libre peut bouger de **6 façons indépendantes**, ni plus ni moins. Le tableau que tu as est exactement la liste :

| Axe de l'espace | Rotation autour de cet axe | Glissement le long de cet axe |
| --- | --- | --- |
| **X** | RX (rotation suivant X) | TX (translation suivant X) |
| **Y** | RY | TY |
| **Z** | RZ | TZ |

Donc **3 rotations + 3 translations = 6 DDL**. C'est le point de départ absolu de toute mécanique : on s'intéresse à *combien* de mouvements restent possibles.

Quand on ajoute une **liaison** entre deux pièces (une articulation, un contact, un glissement), on **bloque un ou plusieurs DDL**. C'est ça, le tableau que ton prof a commencé à remplir.

## 2. Les surfaces élémentaires

Ce sont les 3 façons "de base" dont deux pièces peuvent se toucher/gripper l'une sur l'autre. Why ces 3 ? Parce que ce sont les seuls moyens de faire un contact *durable* entre deux solides :

- **Le plan** — surface plate (ex. un piston qui glisse dans un cylindre, deux pièces qui se plaquent)
- **Le cylindre** — surface ronde (ex. un axe dans un palier)
- **La sphère** — surface ronde multidirectionnelle (ex. une rotule)

## 3. Les liaisons élémentaires

C'est le tableau final : **ligne = la surface de la pièce 1, colonne = la surface de la pièce 2**, et à l'intersection tu lis **ce qui est autorisé / ce qui est bloqué**.

Cases déjà remplies dans ta note :

- **Plan / Plan → TZ, TX, T** : deux plans en contact qui peuvent glisser → c'est la **liaison de glissement** (le coulisseau). Tous les R sont bloqués.
- **Cylindre / Plan → liaison linéaire rectiligne** : un axe qui peut **tourner et glisser** dans un plan → la **liaison pivot/glissement**.
- **Sphère / Plan → liaison sphérique** (et ligne "Lia..." coupée) : une rotule → liaison sphérique.

## Ce qu'il te reste à comprendre

Le tableau complet fait3×3 cases. La logique est toujours la même : **une surface ne peut接触 contact qu'avec une surface compatible, et le contact bloque les DDL qui ne sont pas compatibles avec la liberté de glissement/rotation de la surface.**

La question que tu dois te poser pour chaque case : *si je mets ces deux surfaces l'une sur l'autre, qu'est-ce qui peut encore bouger ?*

- Deux plans plaqués → ça glisse dans le plan, c'est tout → 2 DDL (TX, TY)
- Un cylindre dans un plan → ça tourne sur l'axe et ça glisse le long → 2 DDL
- Une sphère dans un plan → ça pivote partout → 3 DDL (TS)
- Deux cylindres → ça tourne autour d'un seul axe → 1 DDL
- Cylindre + cylindre, Plan + plan…

---

Si tu veux, je peux remplir tout le tableau proprement dans ta note avec les liaisons nommées et leur nombre de DDL, en suivant la logique ci-dessus. Tu me dis.
[Timestamp: 2026/10/01 13:29:53]

**user**: peut tu completer le tableau presque vide s'il te plait
[Timestamp: 2026/10/01 13:30:56]

**ai**: Tableau rempli dans `I2D (müller).md`, avec la lecture de chaque case, une règle mnémotechnique, et un callout qui rattache ça à la 2CV.

Le principe à retenir :

- **Plan/Plan** → glissement rectiligne, 2 DDL (2 translations)
- **Cylindre/Plan** → rotation + translation sur l'axe, 2 DDL
- **Cylindre/Cylindre** → pivot, 1 DDL (l'axe ne fait que tourner)
- **Cylindre/Sphère** → rotoïde, 2 DDL (rotation + inclinaison)
- **Sphère/Plan** et **Sphère/Sphère** → sphérique, 3 DDL (3 rotations)

Deux points sur lesquels j'ai tranché, à vérifier avec ton prof si le corrigé diffère :

- **Plan/Plan** : j'ai mis 2 translations dans le plan, pas 3. Un plan posé sur un autre plan peut glisser dans X et Y, mais pas en Z (sinon il se décolle), et pas en rotation. Si ton tableau attendait 3 DDL c'est qu'il compte une rotationAround la normale.
- **Plan/Cylindre** : c'est la même chose que Cylindre/Plan, la ligne et la colonne du tableau donnent la même liaison, c'est juste la même situation vue dans l'autre sens.

Une notion qui manque dans ta note et qui sert souvent juste après : le **nombre de DDL d'un mécanisme complet** = 6 × (nombre de pièces) − (somme des DDL bloqués par les liaisons). Si on te demande ça plus tard, dis-le moi et je te le détaille.
[Timestamp: 2026/10/01 13:30:56]

**user**: Pourrait tu expliquer dans le document dans une note en thermes généraux
[Timestamp: 2026/10/01 13:33:27]

**ai**: J'ai ajouté une section **« En termes généraux »** au début de [[I2D (müller).md]], juste avant le tableau des DDL. Elle explique le chapitre sans aucune notion de cours préalable :

- **Pourquoi** on fait ça : on ne garde que ce qui bouge, on jette le superflu
- **Un solide** : une pièce, seule dans le vide, qui peut aller partout
- **Une liaison** : le contact entre deux pièces, et la question à se poser dessus
- **Un DDL** : une direction de mouvement possible, l'unité de compte du chapitre
- **L'idée clé** : 6 DDL au départ, moins de DDL à chaque liaison

Et une phrase sur l'intérêt pratique, pour que tu aies une raison de t'y intéresser : on vérifie qu'un mécanisme marche en comptant des directions sur un croquis, sans mesurer la moindre vis.

J'ai fait de `1. Notion de repérage` un titre de niveau2 (`##`) pour que la section générale et les titres du plan de cours se基层党组织 au même niveau dans l'outline. Tu peux me dire si tu préfères garder la numérotation d'origine à plat.
[Timestamp: 2026/10/01 13:33:27]