# I ) Notions de bases
### 1) Grandeurs électriques

| Grandeur              | Unité       | Symbole | Appareil de mesure |
| --------------------- | ----------- | ------- | ------------------ |
| Tension électrique    | Volts (V)   | U       | Voltmètre          |
| Intensité  électrique | Ampères (A) | I       | Ampèremètre        |
| Résistance            | Ohm (Ω)     | R       | Ohmmètre           |
| Puissance             | Watt (W)    | P       | Wattmètre          |
### 2) Symboles électriques

Non donnable par ce médium...

### 3) Rappels

Un générateur ==fournit de l'énergie électrique== pour faire fonctionner des appareils électriques.

Un récepteur ==consomme de l'énergie électrique mais n'en produit pas==.

Un voltmètre se branche en **dérivation**

Un ampèremètre se branche en **série**

La puissance électrique se calcule par la formule ==P = U x I==

Pour les dipôles générateurs, on adopte la convention générateur

Pour les dipôles récepteurs, on adopte la convention récepteur

# II ) Les lois dans les circuit

1. ==Loi des noeuds== est égale à la somme des intensitées des courants arrivants à un noeud qui est égale à la somme des intensitées des courants sortant du noeud.

2. ==Loi des mailles==
	Une maille est un chemin fermé passant par les différents points d'un circuit électrique ==la somme des tension rencontrées dans une maille est nulle==

# III ) Caractéristiques des tensions périodiques

### 1 ) Défintions
- Une tension est **continue** si sa valeur ==ne varie pas au cours du temps==. 
- Une tension est **variable** si sa ==valeur varie au cours du temps==. 
- Une tension est **periodique** si elle ==se répète de manière identique à elle-même à intervalle de temps régulier==
De manière générale, une tension périodique (Kt) peut se décomposer en une somme d'une composante continue ``<u>`` et d'une composante alternative (t).

Une tension est donc ==uniquement alternative si sa composante continue est nulle==.

> [!note] REMARQUE 
> Cela fonctionne de la même façon pour les intensités periodiques

### 2 ) Période et fréquence

La période T correspond à la plus petite durée pour qu'un phénomène se reproduise, identique à lui même. C'est une grandeur qui se note T et qui s'exprime en seconde. Cela correspond à la durée d'un motif élémentaire.

La fréquence f est le nombre de périodes par seconde. Son unité est le Hertz (Hz).

On a la relation suivante : ==f = 1/T==

Avec f en Hertz et T en secondes

### 3 ) Les valeurs de tensions périodiques

Une tension périodique n'a pas constamment la même valeur de tension. Pour cela, on caractérise différente valeurs de tensions :

- **La valeur maximale (Umax)** d'une tension est la valeur la plus grande que la tension atteint lors de sa variation..

- **La valeur minimale (Umin)** d'une tension est la valeur la plus petite que la tension atteint lors de sa variation.

- **La valeur moyenne (``<u>``)** d'une tension correspond à la valeur moyenne du signal. Elle se mesure avec un voltmètre en mode DC.

- **La valeur efficace (Ueff)** d'une tension correspond à la valeur efficace du signal. Elle se mesure à l'aide d'un voltmètre en mode AC.

Pour une tension alternative alternative sinusoïdale, la valeur efficace se calcule ainsi :

==Ueff = Umax/√2==

## IV ) Conducteur ohmique

### 1 ) Définition

Un conducteur ohmique transforme l'énergie électrique en énergie thermique. La grandeur caractéristique d'un conducteur ohmique est sa résistance R qui s'exprime en Ohm (Ω)

### 2 ) Loi d'Ohm

La tension UR aux bornes d'un conducteur ohmique de résistance R est proportionné à l'intensité de courant I qui le traverse. On a donc la relation suivante : ==🔴UR = R x I==.

### 3 ) Effet Joule

Toute l'énergie reçue est dissipée sous la forme de chaleur (énergie thermique) : c'est l'effet Joule. Cet effet porte le nom du physicien Anglais James Prescott Joule qui l'a découvert en 1840.

==🔴P = *UR* x I ou *UR* = R x I donc P = R x I²

(avec P en Joules)

### 4 ) Proportionalité

Comme c'est proportionnel, la caractéristique d'un conducteur ohmique UR = f(IR)est une droite qui passe par l'origine. Le conducteur ohmique est un dipôle passif. Le coefficient directeur de la droite vaut R.

### 5 ) Energie perdue par effet Joule


> [!warning] Attention
> En régime variable, les valeurs des tensions et intensités sont les valeurs efficaces

Connaisant la relation entre l'énergie et la puissance, on peut en déduire que l'énergie dissipée d'un conducteur ohmique par effet Joule est : ==🔴EJ = R x I² x t== 