---
title: HCQmeta.com
bookHidden: false
weight: 4
---

## **Pourquoi les résultats présentés sur la page hcqmeta.com ne sont-ils pas fiables?**

La page [hcqmeta.com](https://hcqmeta.com/) prétend rapporter les résultats d'une _méta-analyse_, càd une synthèse statistique d'un ensemble d'études scientifiques sur un sujet donné - en l'occurence, l'efficacité de l'HCQ comme traitement de la covid-19. Pour avoir un sens, un telle synthèse doit porter sur des études comparables, ce qui signifie avant tout[^def-metaan]:
 1. que les études incluses doivent être valides, càd ne pas présenter de biais importants; 
 2. qu'elles mesurent la même chose. 
 
[^def-metaan]: En réalité, une méta-analyse doit remplir de nombreux critères pour être qualifiée de telle, cf. notamment [cette vidéo](https://www.youtube.com/watch?v=hwE6HAg4o_8).
 
Ces deux critères ne sont pas remplis pour les analyses présentées sur hcqmeta.com, comme expliqué dans les deux [sections dédiées ci-dessous](hcqmeta/#1-les-biais-des-%c3%a9tudes-incluses).
Mais avant de développer ces critiques, il est utile de s'attarder sur une des premières affirmations (erronées) de la page, qui fournit l'occasion de rappeler les notions de statistiques nécessaires à la compréhension de la discussion. Dans [l'encadré en bleu](https://hcqmeta.com/), il est écrit:

> _Early treatment is most successful, with 100% of studies reporting a positive effect_

Cette affirmation fait référence aux figures 1A et 1B (dans la [version du 27/12/2020 de la page](https://archive.vn/SGefy)), qui semblent montrer que toutes les études portant sur un traitement "précoce" par HCQ concluent à un effet positif ("lower risk", en vert):

<figure>
  <img src="../hcqmeta1A1B.png" alt="Figure 1AB" style="width:95%">
  <figcaption> <it> Figures 1A et 1B (hcqmeta.com, 27/12/20). </figcaption>
</figure>


Cependant, ce qui est représenté (par un point en A, par un bâtonnet en B) est un effet moyen, qui n'a aucun sens à lui seul du point de vue statistique. En effet, si la dispersion des résultats autour de la moyenne est grande - ce qui se traduit, dans la [figure 5](https://archive.vn/SGefy/ee4763ee85d4afbfafe152f89df1fbcd15bb3ef6.svg) de hcqmeta.com, par le fait que l'intervalle de confiance autour du risque relatif moyen comprend la valeur 1 (ligne verticale en milieu de figure)-, cela signifie qu'on ne peut écarter la possibilité que l'effet positif observé en moyenne est dû au hasard: on dit que le résultat est _statistiquement non-significatif_ [^signifstat]. 

<figure>
  <img src="../hcqmeta5early.png" alt="Figure 5" style="width:99%">
  <figcaption> <it> Figure 5 - partie supérieure (hcqmeta.com, 27/12/20). </figcaption>
</figure>

Ainsi, les graphiques 1A et 1B ci-dessus (de même que toutes les figures similaires sur hcqmeta.com) n'ont aucun sens en eux-mêmes. Et si on examine les intervalles de confiance correspondants dans la [figure 5](https://archive.vn/SGefy/ee4763ee85d4afbfafe152f89df1fbcd15bb3ef6.svg), on voit que bon nombre des résultats montrés sont statistiquement non significatifs. Parler d'effet positif ou négatif de l'HCQ n'a donc pas de sens pour ces résultats... 

Hélas, bon nombre des résultats _en apparence_ statistiquement significatifs sur hcqmeta.com n'ont pas de sens non plus, comme nous l'expliquons maintenant.

[^signifstat]: Plus exactement, le résultat est statistiquement non significatif au seuil de 5% (seuil utilisé dans la plupart des études scientifiques), et l'intervalle de confiance correspondant contient la vraie valeur moyenne de l'effet avec une probabilité de 95% (...si les hypothèses sous-jacentes au test statistique sont respectées).

### **1. Les biais des études incluses**

Plusieurs des études incluses dans les analyses de hcqmeta.com présentent de graves problèmes méthodologiques. Un exemple flagrant est donné par l'[étude de Lagier et al.](https://www.sciencedirect.com/science/article/pii/S1477893920302817)  de l'équipe du professeur Raoult. En effet, celle-ci compare un groupe des patients ayant reçu le traitement HCQ+AZ durant au moins 3 jours (3119) à un groupe rassemblant des patients n'ayant reçu aucun des deux médicaments (162), ayant reçu HCQ seul (101), AZ seul (137), et... tous les patients ayant pris HCQ+AZ moins de 3 jours (218), comme le montre [cette figure originale de l'article](https://www.sciencedirect.com/science/article/pii/S1477893920302817#fig1):

<center><figure>
  <img src="../Lagier2020fig1.jpg" alt="Figure 1 Lagier" style="width:65%">
  <figcaption> <it> Figure 1, Lagier et al. 2020. </figcaption>
</figure></center>

Ainsi, non seulement le groupe "non traité"  porte très mal son nom, puisqu'il comporte des patients ayant reçu HCQ et/ou AZ, mais il inclut de plus tous les patients ayant supporté le traitement HCQ+AZ moins de 3 jours. Cela biaise les résultats en faveur du traitement HCQ+AZ.
En effet, c'est un peu comme si on comptabilisait les patients développant des effets secondaires graves à un vaccin dans le groupe n'ayant pas reçu le vaccin... Vous n'accepteriez certainement pas de vous faire vacciner sur base d'une telle étude.
Et si ce biais dit de "période d'immortalité" est le plus flagrant, il n'est pas le seul biais important qu'on peut identifier dans l'étude, comme expliqué [ici](https://www.clinicalmicrobiologyandinfection.com/article/S1198-743X(20)30613-3/fulltext).

D'autres études présentées comme significatives sur hcqmeta.com comportent des biais du même type (cf. [plus bas](hcqmeta/#fig-morta)). Et si toutes les études (en apparence) favorables à l'HCQ ne présentent pas des biais aussi flagrants, la plupart d'entre elles sont des études observationnelles (rétrospectives), qui sont nettement moins fiables en général que les essais contrôlés randomisés (ECR). Des détails à ce sujet sont donnés [ici](remedes_faq/#obs-bias), mais une des raisons est facile à comprendre: dans un ECR, on écarte _a priori_ de l'étude (càd du groupe traité ET du groupe non traité) les patients avec des contre-indications pour le traitement; dans les études observationnelles, les patients avec contre-indications se retrouvent généralement dans le groupe non traité. En effet, l'étude n'est tout simplement pas définie au moment de l'attribution du traitement - on analyse les données _a posteriori_. On peut identifier une partie des patients avec contre-indications sur base des données collectées (en particulier, des comorbidités répertoriées pour les patients), et faire des "ajustements" statistiques pour essayer de pallier aux déséquilibres entre les deux groupes comparés (cf. [ici](remedes_faq/#obs-bias)). Mais une zone d'ombre subsiste en général quant aux raisons qui ont conduit _in fine_ le médecin à donner ou non le traitement au patient. Dans les ECR, l'attribution du traitement se fait de manière aléatoire, de sorte que ce biais n'existe pas.

Les figures 6 et 7 de la page hcqmeta.com présentent bien des [résultats limités aux ECR](https://archive.vn/SGefy#rct) (RCT en anglais), mais ils n'ont aucun sens en raison de l'hétérogénéité des données utilisées, comme expliqué dans la section suivante. On peut également remarquer que même en faisant cet amalgame injustifié, l'effet global obtenu est statistiquement non signicatif ([Table 2](https://archive.vn/SGefy#table_positivestats2), dernière colonne, 1ere ligne) à moins d'exclure certaines études classées par les auteurs comme "traitement tardif" (2e ligne). Et les deux seules études (Huang *et al.* et Chen *et al.*) rapportant un effet statistiquement significatif parmi ces derniers ECR présentent de graves problèmes méthodologiques, comme expliqué [ici](https://www.sciencesetavenir.fr/sante/covid-19-quelle-est-la-meta-analyse-dont-parle-le-documentaire-mal-traites_150257).


### **2. L'hétérogénéité des effets comparés**

La plupart des figures (à l'exception de la figure 10, que nous discutons ci-après) amalgament des données relatives à des mesures différentes de l'efficacité du traitement: des risques relatifs (RR) de décès, de test PCR positif, d'hospitalisation,...
ce qui n'a aucun sens du point de vue quantitatif. C'est un peu comme si on disait que manger du chocolat améliore notre état général de 15% parce qu'en moyenne, il améliore l'humeur de 30% et augmente le poids de 10%. Sur quelle base pouvons-nous combiner ces deux informations, et quel poids est-il légitime de donner à chacune pour arriver à une mesure globale de l'effet? Les auteurs de la page ne répondent pas à ces questions fondamentales.

#### **Analyse de la figure présentant des données "homogènes"**

<a id="fig-morta"></a>
La figure 10 ([appendice 2](https://archive.vn/SGefy#appendix_mortality) de hcqmeta.com) rassemble des données de mortalité uniquement, donc ne souffre pas de problème d'hétérogénéité flagrant au niveau de l'effet du traitement considéré.
Cependant, les études rapportant un effet positif statistiquement significatif de l'HCQ dans cette figure sont hétérogènes à d'autres égards, et plusieurs présentent des sources de biais importants, comme nous le montrons maintenant pour un sous-ensemble de celles-ci. Penchons-nous en effet sur les études sensées étayer l'efficacité du traitement "précoce" par HCQ (partie supérieure de la  figure 10, reproduite ci-dessous). Cinq études semblent rapporter un résultat statistiquement significatif:

<figure>
  <img src="../fig10early.png" alt="Figure 10" style="width:99%">
  <figcaption> <it> Figure 10 - partie supérieure (hcqmeta.com, 27/12/20). </figcaption>
</figure>

Cependant:

* L'étude de [Lagier et al.](https://www.sciencedirect.com/science/article/pii/S1477893920302817) présente des biais importants, comme expliqué dans la [section 1](hcqmeta/#1-les-biais-des-%c3%a9tudes-incluses) (plus de détails sont donnés [ici](https://www.clinicalmicrobiologyandinfection.com/article/S1198-743X(20)30613-3/fulltext));
* L'étude de [Ly et al.](https://www.sciencedirect.com/science/article/pii/S0924857920304301) (également réalisée par l'équipe du professeur Raoult) porte uniquement sur des résidents en EPHAD à Marseille (moyenne d'âge: 83 ans), et le groupe "non traité" amalgame, comme la précédente, tous les patients n'ayant pas reçu HCQ+AZ au moins 3 jours. En particulier, un tiers de ces patients ont reçu AZ seul, et les auteurs ne spéficient pas la mortalité dans ce sous-groupe. 
* L'étude de [Heras et al.](https://link.springer.com/article/10.1007/s41999-020-00432-w) porte également sur des patients très âgés (moyenne d'âge: 85 ans) hébergés en institution d'accueil, atteints pour la plupart de démence (73 sur 100). Outre la présence du biais de période d'immortalité mentionné précédemment, les résultats présentés sont pour le moins... atypiques: un pourcentage de mortalité de 62% chez les sujets "non traités" (càd n'ayant pas pris HCQ+AZ plus de 5 jours), contre 11% dans le groupe HCQ+AZ; et, après ajustement (régression multivariée) pour certains facteurs de confusion, un OR (odds ratio, ou "rapport de cotes") de 38 pour le fait d'être de sexe masculin plutôt que de sexe féminin... Du jamais vu dans d'autres études sur la covid-19 (par comparaison, dans l'étude de Ly et al. portant sur une population similaire, ce rapport de cotes est de 4, tandis que le pourcentage de mortalité chez les patients "non traités" est de 26%, contre 15% dans le groupe HCQ+AZ). Il est aussi étonnant que le suivi s'arrête après 14 jours pour une étude portant sur la mortalité.
* L'étude (non publiée) de [Sulaiman et al.](https://www.medrxiv.org/content/10.1101/2020.09.09.20184143v1) a notamment été discutée [ici](https://rechercheindependante.blogspot.com/2020/05/les-etudes-sur-lhydroxychloroquine-hors.html#sulaiman). Le groupe traité par HCQ ne contient que 10 patients de plus de 65 ans (sur 1817), contre 154 (sur 3754) dans le groupe non traité. 
Cela fait douter certains de la pertinence de l'étude, dans la mesure où la covid-19 est beaucoup plus létale chez les personnes âgées (voir les commentaires en bas de page sur [medRxiv](https://www.medrxiv.org/content/10.1101/2020.09.09.20184143v1)). On peut également se demander pourquoi il y a proportionnellement beaucoup plus de perdus de vue dans le groupe HCQ (1503 sur 3320) que dans le groupe non traité (848 sur 4572).
Enfin, la table 4 de l'article, qui décrit les principaux résultats après ajustement par un modèle multivarié, est pour le moins déconcertante. En particulier, la variable expliquée (risque d'hospitalisation ou risque combiné d'admission aux soins intensifs/ de décès) est listée parmi les facteurs de confusion (en lieu et place de l'HCQ?). Aussi, les auteurs rapportent que les valeurs des OR obtenues pour TOUTES les variables de confusion (ainsi que leurs intervalles de confiance) sont identiques pour les deux choix de variable expliquée: fort étonnant.
* L'étude de [Guisado-Vasco et al.](https://www.sciencedirect.com/science/article/pii/S2589537020303357) ne montre pas d'effet statistiquement significatif du traitement par HCQ, même lorsqu'il est entamé avant admission à l'hôpital, une fois que les résultats sont ajustés pour les facteurs de confusion identifiés ([figure 2](https://www.sciencedirect.com/science/article/pii/S2589537020303357#fig0002) de l'article).

En conclusion, aucune des études rapportant un effet statistiquement significatif de l'HCQ en traitement précoce sur hcqmeta.com n'est fiable. Il est donc totalement injustifié d'en conclure à une amélioration globale de 77% de l'incidence de la mortalité comme le fait la figure ci-dessus. D'autant plus que... si les études examinées ne sont pas hétérogènes au niveau de l'effet examiné (la mortalité), elles le sont au niveau du traitement: les 3 premières portent sur le traitement HCQ+AZ, avec un groupe de contrôle incluant des patients traités par HCQ et/ou AZ seul, tandis que les 2 dernières portent sur un traitement avec HCQ seul (avec un groupe de contrôle traité ni par HCQ ni par AZ). Cette hétérogénéité de traitement rend à elle seule la méta-analyse invalide.

Nous laissons au lecteur intéressé le soin de répéter l'exercice pour les résultats relatifs aux autres modalités d'administration de l'HCQ - en gardant à l'esprit que la plupart des études présentées sur hcqmeta.com, même lorsqu'elles ne présentent _en apparence_ pas de biais grave, sont des études observationnelles dont la fiabilité est généralement très inférieure à celle d'un ECR (cf. [ici](remedes_faq/#obs-bias)  et [ici](remedes_faq/#ecr-vs-obs)). On peut d'ailleurs se demander pourquoi les auteurs n'ont pas réalisé le même type de "méta-analyse", considérant un seul indicateur d'efficacité du traitement à la fois, en se limitant aux résultats des seuls ECR. Peut-être parce qu'ils auraient alors obtenu la figure suivante (issue de [cette synthèse de tous les ECR publiés](https://public.tableau.com/profile/publichealth#!/vizhome/SynthsehydroxychloroquineetCOVID-19/Histoire1))?

[![Synthèse Fiolet](../syntheseECR-HCQ.png)](https://public.tableau.com/profile/publichealth#!/vizhome/SynthsehydroxychloroquineetCOVID-19/Histoire1)

Nous laissons enfin au lecteur le soin de conclure quant à la confiance à accorder aux pages soeurs de hcqmeta.com (https://hcqtrial.com, https://c19study.com,...), en particulier à [celle affirmant l'efficacité de l'ivermectine](https://c19ivermectin.com/) - molécule en passe de devenir [la nouvelle HCQ](https://rechercheindependante.blogspot.com/2020/12/livermectine-maintenant-contre-la-covid.html)...

