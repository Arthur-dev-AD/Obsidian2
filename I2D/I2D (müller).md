# LA 2CV

1. Cycle de vie d'un produit :
		Etapes du cycle de vie
			-  1 : Conception
				- phase de mise au point et développement
				- phase de lancement
				- phase de maturité
				- phase de croissance
				- phase de déclin
	Sur une feuille papier , retrouver les différentes phases pour la citroën 2CV il faut retrouver les dates, les quantitées de productions ainsi que les propriétées techniques
		- La puissance en CV din au Watt (1CV = 735 W)
		- Cylindré en cm^3 : 375 cm^3
		- La vitesse en Km/h
		- La consomation en L
		- Couple
## Liens externes par phase

### Phase de développement / Conception
- [Cycle de vie produit : définition et phases — Qualtrics](https://www.qualtrics.com/fr/articles/strategy-research/cycle-vie-produit/) — Article complet détaillant l'idée, le développement et les 6 étapes du cycle
- [Cycle de vie d'un produit : définition et étapes — Portices](https://www.portices.fr/cycle-de-vie-produit-definition-etapes/) — Détaille la phase de création, les prototypes et les tests de performance

### Phase de lancement
- [Cycle de vie d'un produit : ses phases et comment les respecter — Finom](https://finom.co/fr-fr/blog/cycle-de-vie-dun-produit/) — Explique la stratégie de lancement, les "early adopters" et l'éducation du marché
- [Cycle de vie d'un produit : définition et étapes — HubSpot](https://blog.hubspot.fr/marketing/cycle-de-vie-produit) — Décrit le lancement, la politique de prix (écrémage vs pénétration) et les coûts marketing

### Phase de croissance
- [Cycle de vie du produit — Sciencesdegestion.fr](https://sciencesdegestion.fr/strategie/cycle-de-vie-du-produit/) — Analyse la croissance rapide des ventes, l'apparition de la concurrence et les stratégies de différenciation
- [Cycle de vie produit : les 5 phases clés — L'Agence](https://lagence-communication.fr/cycle-vie-produit-5-phases/) — Détaille les indicateurs de croissance et la priorité d'accélérer la distribution

### Phase de maturité
- [Cycle de vie produit : les 5 phases clés — L'Agence](https://lagence-communication.fr/cycle-vie-produit-5-phases/) — Explique la saturation du marché, la pression sur les marges et les stratégies de fidélisation
- [Cycle de vie d'un produit : définition et étapes — HubSpot](https://blog.hubspot.fr/marketing/cycle-de-vie-produit) — Décrit les actions pour prolonger la phase de maturité (variantes, programmes de fidélité)

### Phase de déclin
- [Cycle de vie d'un produit : ses phases et comment les respecter — Finom](https://finom.co/fr-fr/blog/cycle-de-vie-dun-produit/) — Présente les options face au déclin : retrait, repositionnement, relance par l'innovation
- [Cycle de vie d'un produit : définition et étapes — HubSpot](https://blog.hubspot.fr/marketing/cycle-de-vie-produit) — Détaille les stratégies de fin de vie et la préparation du remplacement

---

# Notice de calcul sur la 2CV

%%
PS = Puissance de sortie
PE = Puissance d'entrée
PI = Puissance intermédiaire 
%%

## Données de 1948
- Puissance : 9 CV ( 6615 W (9x735))
- Rendement : 30 %
- PS = 1984,5W

## Calculs

calcul de puissance d'entrée ; PE = 9CV
PE = 9x735 = 6615 W
		   = 6,615kW

- Calcul de la puissance de sortie : ==PS = PE x Rendement== 
	- PS = 6615 x 0,3 = 1984,5 W

- Calcul  rendement global : ==Rendement global = PS / PE==
	- Rendement global = 1984,5 / 6615 = 0,3

- Calcul des pertes : ==Pertes = PE - PS==
	-  Pertes = 6615 - 1984,5 = 4630, 5

- Rendement des composants individuels
	1. Moteur thermique : 0,45
	2. Boite de vitesse : 0,9
	3. Roues et cardon  : A CALCULER 



- Calculs moteur thermique
	- Calcul de PI1 : PE x Rendement moteur thermique = 6615 x 0,45 = 2 976,75 W
	- Calcul des pertes : PE - PI1 = 6615 - 2976,75 = 3 638,25 W

- Calcul boîte de vitesse
	- PI2 = PI1 x Rendement de la boîte de vitesse = 2976 x 0,9 = 2 679,075 W
	- Pertes = PI1 - PI2 = 2976,75 - 2679,075 = 297,675 W

- Calcul du rendement des roues + cardon
	- Rendement = PS / PI2 = 1984,5 / 2679,07 = 0,74
	- Pertes = PI2 - PS = 2679,07 - 1984,5 = 694,57 W

![[Diagramme PEPS.svg]]
(Voir "Diagramme PEPS.svg" si vu sur github)

- Interpretation :
	Le moteur n'est pas optimisé, son rendement est très faible. Nous pouvons le remplacer par un moteur électrique.
	Le cardant et la roue ont un mauvais rendement car le pneu date de 1948. Actuellement, les pneus ont de nouvelles caractéristique

___
## Formules additionnelles

Couple : ==P =  C x Ω==
Pour P en Watt (W), C en Newtown x mètre (N.m) et Ω en vitesse angulaire (radiant/s)

