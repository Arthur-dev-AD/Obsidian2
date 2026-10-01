---
epoch: 1790854192991
mode: agent
backendId: opencode
sessionId: "ses_f08e21770ffeoWP7r3g20o6fLi"
agentLabel: "Comprendre les liaisons mécaniques"
usage: '{"usedTokens":12245,"contextWindow":200000,"updatedAt":1790854218515}'
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

**ai**: 
[Timestamp: 2026/10/01 13:30:56]