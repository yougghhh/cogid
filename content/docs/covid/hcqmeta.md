---
title: HCQmeta
bookHidden: true
weight: 10
---

## **Pourquoi les résultats présentés sur la page hcqmeta.com ne sont-ils pas fiables?**

La page [hcqmeta.com](https://hcqmeta.com/) prétend rapporter les résultats d'une _méta-analyse_, càd une synthèse statistique d'un ensemble d'études scientifiques sur un sujet donné - en l'occurence, l'efficacité de l'HCQ comme traitement de la covid-19. Pour avoir un sens, un telle synthèse doit porter sur des études comparables, ce qui signifie avant tout[^def-metaan]:
 1. que les études incluses doivent être valides, càd ne pas présenter de biais graves; 
 2. qu'elles mesurent la même chose. 
 
[^def-metaan]: En réalité, une méta-analyse doit remplir de nombreux critères pour être qualifiée de telle, cf. notamment [cette vidéo](https://www.youtube.com/watch?v=hwE6HAg4o_8).
 
Ces deux critères ne sont pas remplis pour les analyses présentées sur hcqmeta.com, comme expliqué dans les deux [sections dédiées ci-dessous](hcqmeta/#1-les-biais-des-%c3%a9tudes-incluses).
Mais avant de développer ces critiques, il est utile de s'attarder sur une des premières affirmations (erronées) de la page, qui fournit l'occasion de rappeler les notions de statistiques nécessaires à la compréhension de la discussion. Dans [l'encadré en bleu](https://hcqmeta.com/), il est écrit:

> _Early treatment is most successful, with 100% of studies reporting a positive effect_

Cette affirmation fait référence aux figures ci-dessous (figures 1A et 1B dans la [version du 27/12/2020 de la page](https://archive.vn/SGefy)), qui semblent montrer que toutes les études portant sur un traitement "précoce" par HCQ concluent à un effet positif ("lower risk", en vert):

![Figure 1A](../hcqmeta1A.svg)
![Figure 1B](../hcqmeta1B.svg)


Or, un effet moyen n'a aucun sens à lui seul du point de vue statistique. En effet, si la dispersion des résultats autour de la moyenne est grande - ce qui se traduit, dans la [figure 5](https://archive.vn/SGefy/ee4763ee85d4afbfafe152f89df1fbcd15bb3ef6.svg) (trop grande pour être reproduite ici), par le fait que l'intervalle de confiance autour du risque relatif moyen (symbole carré) comprend la valeur 1 -, cela signifie qu'on ne peut écarter la possibilité que l'effet positif observé en moyenne est du au hasard: on dit que le résultat est _statistiquement non-significatif_ [^signifstat]. 
Ainsi, les graphiques ci-dessus (de même que ceux montrés dans les figures similaires de la page) n'ont aucun sens en eux-mêmes. Et si on examine les intervalles de confiance correspondants dans la [figure 5](https://archive.vn/SGefy/ee4763ee85d4afbfafe152f89df1fbcd15bb3ef6.svg), on voit que bon nombre des résultats montrés sont statistiquement non significatifs. Parler d'effet positif ou négatif de l'HCQ n'a donc pas de sens pour ces résultats... 

Hélas, bon nombre des résultats _en apparence_ statistiquement significatifs dans la figure 5 de hcqmeta.com n'ont pas de sens non plus, comme nous l'expliquons maintenant.

[^signifstat]: Plus exactement, le résultat est statistiquement non significatif au seuil de 5% (seuil utilisé dans la plupart des études scientifiques), et l'intervalle de confiance correspondant contient la vraie valeur moyenne de l'effet avec une probabilité de 95% (...si les hypothèses sous-jacentes au test statistique sont respectées).

### **1. Les biais des études incluses**

Plusieurs des études incluses dans les analyses de hcqmeta.com présentent de graves biais. Un exemple flagrant est l'[étude de Lagier et al.](https://www.sciencedirect.com/science/article/pii/S1477893920302817)  de l'équipe du professeur Raoult. En effet, celle-ci compare un groupe des patients ayant reçu le traitement HCQ+AZ durant au moins 3 jours (3119) à un groupe rassemblant des patients n'ayant reçu aucun des deux médicaments (162), ayant reçu HCQ seul (101), AZ seul (137), et... tous les patients ayant pris HCQ+AZ moins de 3 jours (218), comme le montre [cette figure originale de l'article](https://www.sciencedirect.com/science/article/pii/S1477893920302817#fig1):
![Figure 1 Lagier](../Lagier2020fig1.jpg)

Ainsi, non seulement le groupe "non traité"  est hétérogène, mais il inclut tous les patients ayant supporté le traitement moins de 3 jours, ce qui fait augmenter [indûment le pourcentage de mortalité dans ce groupe](https://www.clinicalmicrobiologyandinfection.com/article/S1198-743X(20)30613-3/fulltext).
Ce biais dit de "période d'immortalité" rend les résultats de l'étude invalides. En effet, accepteriez-vous de prendre un vaccin si les études concluant à son efficacité avait écarté des résultats tous les patients présentant des effets secondaires graves? Ici, c'est encore pire, puisque les patients ayant mal supporté le traitement, non seulement ne sont pas compatibilisés dans le groupe traité, mais sont comptabilisés dans le groupe contrôle... C'est comme si on avait comptabilisé les patients développant des effets secondaires graves suite à une vaccination dans le groupe n'ayant pas reçu le vaccin!

D'autres études présentées comme significatives sur hcqmeta.com présentent des biais similaires (cf. [plus bas](hcqmeta/#fig-morta)). Et si toutes les études (en apparence) favorables à l'HCQ ne présentent pas des biais aussi graves, la plupart d'entre elles sont des études observationnelles qui, contrairement aux essais contrôlés randomisés (ECR), présentent des biais intrinsèques auxquels on ne peut jamais remédier que partiellement par traitement des données a posteriori (voir [ici](remedes_faq/#obs-bias) pour plus de détails).

Les figures 6 et 7 de la page hcqmeta.com présentent bien des [résultats limités aux ECR](https://archive.vn/SGefy#rct) (RCT en anglais), mais ils n'ont aucun sens en raison de l'hétérogénéité des données utilisées (cf. section suivante). On peut également remarquer que même en faisant cet amalgame injustifié, l'effet global obtenu est statistiquement non signicatif ([Table 2](https://archive.vn/SGefy#table_positivestats2), dernière colonne, 1ere ligne) à moins d'exclure certaines études classées par les auteurs comme "traitement tardif" (2e ligne). 


### **2. L'hétérogénéité des effets comparés**

La plupart des figures (à l'exception de la figure 10, que nous discutons ci-après) amalgament des données relatives à des mesures différentes de l'état des patients: des risques relatifs (RR) de décès, de test PCR positif, d'hospitalisation,...
ce qui n'a aucun sens du point de vue quantitatif. C'est un peu comme si on disait que manger du chocolat améliore notre état général de 15% parce qu'en moyenne, il améliore l'humeur de 30% et augmente le poids de 10%. Sur quelle base pouvons-nous combiner ces deux informations, et quel poids est-il légitime de donner à chacune pour arriver à une mesure globale de l'effet? Les auteurs de la page ne répondent pas à ces questions fondamentales.

#### **Analyse de la figure présentant des données "homogènes"**

<a id="fig-morta"></a>
La [figure 10](https://archive.vn/SGefy/73f68e887ba3dce3f65db97f0c2364ed3201b762.svg) (appendice 2 de hcqmeta.com) rassemble des données de mortalité uniquement, donc ne souffre pas de problème d'hétérogénéité flagrant.
Cependant, les études rapportant un effet positif statistiquement significatif de l'HCQ dans cette figure sont en majorité gravement biaisées, comme un examen détaillé permet de le montrer. Penchons-nous en particulier sur les études sensées étayer l'efficacité du traitement "précoce" par HCQ (partie supérieure de la  figure 10, reproduite ci-dessous). Cinq études semblent rapporter un résultat statistiquement significatif:

![Figure mortalité](../fig10early.png)

Or:

* L'étude de [Lagier et al.](https://www.sciencedirect.com/science/article/pii/S1477893920302817) est gravement biaisée, comme expliqué dans la [section 1](hcqmeta/#1-les-biais-des-%c3%a9tudes-incluses) (plus de détails sont donnés [ici](https://www.clinicalmicrobiologyandinfection.com/article/S1198-743X(20)30613-3/fulltext));
* L'étude de [Ly et al.](https://www.sciencedirect.com/science/article/pii/S0924857920304301) (également réalisée par l'équipe du professeur Raoult) porte uniquement sur des résidents en EPHAD à Marseille (moyenne d'âge: 83 ans), et présente le même biais critique de "période d'immortalité" que l'étude de Lagier et al.
* L'étude de [Heras et al.](https://link.springer.com/article/10.1007/s41999-020-00432-w) porte également sur des patients très âgés (moyenne d'âge: 85 ans) hébergés en institution d'accueil, atteints pour la plupart de démence (73%). Outre la présence du biais de période d'immortalité mentionné précédemment, les résultats présentés sont pour le moins... surpenants: un pourcentage de mortalité de 62% chez les sujets "non traités" (càd n'ayant pas pris HCQ+AZ plus de 5 jours) et, après ajustement (régression multivariée) pour certains facteurs de confusion, un OR (odds ratio, ou "rapport de cotes") de 38 pour le fait d'être de sexe masculin plutôt que de sexe féminin... Un résultat jamais vu dans d'autres études sur la covid-19 (par comparaison, dans l'étude de Ly et al. portant sur une population similaire, ce rapport de cotes est de 4, tandis que le pourcentage de mortalité chez les patients "non traités" est de 26%...).
* L'étude (non publiée) de [Sulaiman et al.](https://www.medrxiv.org/content/10.1101/2020.09.09.20184143v1) a été discutée [ici](https://rechercheindependante.blogspot.com/2020/05/les-etudes-sur-lhydroxychloroquine-hors.html). Le groupe traité par HCQ ne contient que 10 patients de plus de 65 ans (sur 1817), contre 154 (sur 3754) dans le groupe traité, soit proportionnellement 8 fois moins dans le groupe traité. Cela fait douter certains de la pertinence de l'étude (voir les commentaires en bas de l'article sur [medRxiv](https://www.medrxiv.org/content/10.1101/2020.09.09.20184143v1)). On notera également (table 4 de l'article) des résultats étonnants après ajustement pour plusieurs facteurs de confusion (dont l'âge), tels qu'un OR significativement inférieur à 1 pour le fait d'avoir plus de 65 ans (comparé à... avoir moins de 18 ans), et aucun OR significatif pour les comorbidités généralement identifiées comme facteurs de risque pour la covid-19.
* L'étude de [Guisado-Vasco et al.](https://www.sciencedirect.com/science/article/pii/S2589537020303357) ne montre pas d'effet statistiquement significatif du traitement par HCQ, même lorsqu'il est entamé avant admission à l'hôpital, une fois que les résultats sont ajustés pour les facteurs de confusion identifiés ([figure 2](https://www.sciencedirect.com/science/article/pii/S2589537020303357#fig0002) de l'article).

En conclusion, aucune des études rapportant un effet statistiquement significatif de l'HCQ en traitement précoce n'est fiable. Il est donc totalement injustifié d'en conclure à une amélioration globale de 77% de l'incidence de la mortalité comme le fait la figure ci-dessus (qui plus est, sans spécifier le poids accordé aux différentes études pour parvenir à ce résultat global).

Nous laissons au lecteur intéressé le soin de répéter l'exercice pour les résultats relatifs aux autres modalités d'administration de l'HCQ - en gardant à l'esprit que la plupart des études présentées sur hcqmeta.com, même lorsqu'elles ne présentent _en apparence_ pas de biais grave, sont des études observationnelles dont la fiabilité est généralement très inférieure à celle d'un ECR (cf. plus haut et [ici](remedes_faq/#ecr-vs-obs)).

Nous laissons également au lecteur le soin de conclure quant à la confiance à accorder aux pages soeurs de hcqmeta.com (https://hcqtrial.com, https://c19study.com,...), en particulier à [celle affirmant l'efficacité de l'ivermectine](https://c19ivermectin.com/) - molécule en passe de devenir [la nouvelle HCQ](https://rechercheindependante.blogspot.com/2020/12/livermectine-maintenant-contre-la-covid.html)...

