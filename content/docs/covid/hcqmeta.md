---
title: HCQ et al.
bookHidden: true
weight: 10
---

## **Pourquoi les résultats présentés sur la page hcqmeta.com ne sont-ils pas fiables?**

La page [hcqmeta.com](https://hcqmeta.com/) prétend rapporter les résultats d'une _méta-analyse_, càd une synthèse statistique d'un ensemble d'études scientifiques sur un sujet donné - ici, l'efficacité de l'HCQ comme traitement de la covid-19. Pour avoir un sens, un telle synthèse doit porter sur des études comparables, ce qui signifie avant tout[^def-metaan]:
 1. que les études incluses doivent être valides, càd ne pas présenter de biais graves; 
 2. qu'elles mesurent la même chose. 
 
[^def-metaan]: En réalité, une méta-analyse doit remplir de nombreux critères pour être qualifiée comme telle, cf. notamment [cette vidéo](https://www.youtube.com/watch?v=hwE6HAg4o_8).
 
Ces deux critères ne sont pas remplis pour les analyses présentées sur la page hcqmeta, comme expliqué dans les deux [sections dédiées ci-dessous](hcqmeta/#1-les-biais-des-%c3%a9tudes-incluses).
Mais avant de développer ces critiques, il est utile de s'attarder sur une des premières affirmations (erronées) de la page, qui fournit l'occasion de rappeler les notions de statistiques nécessaires à la compréhension de la discussion qui suit. Dans l'encadré en bleu, il est écrit:

> _Early treatment is most successful, with 100% of studies reporting a positive effect_

Cette affirmation fait référence aux figures [1A](https://hcqmeta.com/plot/spae.svg) et [1B](https://hcqmeta.com/plot/metaearly.svg), qui semblent montrer que toutes les études portant sur un traitement "précoce" par HCQ concluent à un effet positif ("lower risk", en vert sur les figures). Or, cet effet moyen n'a aucun sens à lui seul du point de vue statistique. En effet, si la dispersion des résultats autour de la moyenne est importante - ce qui se traduit, dans la [figure 5](https://hcqmeta.com/plot/fp.svg), par le fait que l'intervalle de confiance autour du risque relatif moyen (symbole carré) comprend la valeur 1 - cela signifie qu'on ne peut écarter la possibilité que l'effet positif observé en moyenne est du au hasard: on dit que le résultat est _statistiquement non-significatif_. 
Ainsi, les résultats présentés dans la figure 1 (de même que dans les figures 3, 4, 6, 7, 8) n'ont aucun sens à eux seuls. Et si on examine les intervalles de confiance dans la [figure 5](https://hcqmeta.com/plot/fp.svg), on voit que bon nombre des résultats rapportés sont statistiquement non significatifs. Parler d'effet positif ou négatif n'a donc pas de sens pour ces résultats. Hélas, bon nombre des résultats en apparence statistiquement significatifs n'ont pas de sens non plus, pour la raison suivante.


### **1. Les biais des études incluses**

Plusieurs des études incluses dans les analyses de hcqmeta.com présentent de graves biais. Un exemple flagrant est l'étude de Lagier et al.  de l'équipe du professeur Raoult. En effet, celle-ci compare un groupe des patients ayant reçu le traitement HCQ+AZ durant au moins 3 jours (3119) à un groupe rassemblant des patients n'ayant reçu aucun des deux médicaments (162), ayant reçu HCQ seul (101), AZ seul (131), et... tous les patients ayant pris HCQ+AZ moins de 3 jours (218), comme le montre [cette figure originale de l'article](https://www.sciencedirect.com/science/article/pii/S1477893920302817#fig1).
Ainsi, non seulement le groupe "non traité"  est hétérogène, mais il inclut tous les patients ayant supporté le traitement moins de 3 jours, ce qui fait augmenter [indûment le pourcentage de mortalité dans ce groupe](https://www.clinicalmicrobiologyandinfection.com/article/S1198-743X(20)30613-3/fulltext).
Ce biais dit de "période d'immortalité" rend les résultats de l'étude invalides. En effet, accepteriez-vous de prendre un vaccin si les études concluant à son efficacité avait écarté des résultats tous les patients présentant des effets secondaires graves? Ici, c'est encore pire, puisque les patients ayant mal supporté le traitement, non seulement ne sont pas compatibilisés dans le groupe traité, mais sont comptabilisés dans le groupe contrôle... C'est comme si on avait comptabilisé les patients développant des effets secondaires graves suite à une vaccination dans le groupe n'ayant pas reçu le vaccin!

Toutes les études incluses ne présentent pas des biais aussi graves, mais la plupart d'entre elles sont des études observationnelles qui, contrairement aux essais contrôlés randomisés (ECR, ou RCT en anglais), présentent des biais intrinsèques auxquels on ne peut jamais remédier que partiellement par traitement des données a posteriori (voir par exemple [ici](remedes_faq/#obs-bias) pour plus de détails).

Les figures 6 et 7 présentent des [résultats limités aux ECR](https://hcqmeta.com/#rct), mais ils n'ont aucun sens en raison de l'hétérogénéité des données utilisées, comme expliqué ci-après. On peut également remarquer que même en faisant cet amalgame injustifié, l'effet global obtenu est statistiquement non signicatif ([Table 2](https://hcqmeta.com/#table_positivestats2), dernière colonne, 1ere ligne) à moins d'exclure certaines études classées par les auteurs comme "traitement tardif" (2e ligne). 


### **2. L'hétérogénéité des effets comparés**

La plupart des figures (à l'excepté de la figure 10, que nous discutons ci-après) amalgament des données relatives à des mesures différentes de l'état des patients: des risques relatifs (RR) de décès, de test PCR positif, d'hospitalisation,...
ce qui n'a aucun sens du point de vue quantitatif. C'est un peu comme si on disait que manger du chocolat améliore notre état général de 15% parce qu'en moyenne, il améliore l'humeur de 30% et augmente le poids de 10%. Sur quelle base pouvons-nous combiner ces deux informations, et quel poids est-il légitime de donner à chacune pour arriver à une mesure globale de l'effet? Les auteurs de la page ne répondent pas à ces questions fondamentales.

La [figure 10](https://hcqmeta.com/plot/fpd.svg) (appendice 2) rassemble des données de mortalité uniquement, mais les études rapportant un effet positif statistiquement significatif de l'HCQ sont en majorité gravement biaisées. Montrons cela pour les résultats relatifs à un traitement "précoce" par HCQ (sous-titrés "early" en haut de la  figure 10), traitement dont l'efficacité est présentée comme la plus importante. On y voit 5 études (dans la [version 44](https://archive.vn/SGefy) de la page) associées à un résultat statistiquement significatif: Lagier, Ly, Heras, Sulaiman, et Guisado-Vasco.
* Nous avons expliqué ci-dessus pourquoi l'étude de Lagier et al. est invalide (plus de détails sont donnés [ici](https://www.clinicalmicrobiologyandinfection.com/article/S1198-743X(20)30613-3/fulltext)).
* L'étude de [Ly et al.](https://www.sciencedirect.com/science/article/pii/S0924857920304301) (également réalisée par l'équipe du professeur Raoult) porte uniquement sur des résidents en EPHAD à Marseille (moyenne d'âge: 83 ans), et présente le même biais critique de "période d'immortalité" que l'étude de Lagier et al.
* L'étude de [Heras et al.](https://link.springer.com/article/10.1007/s41999-020-00432-w) porte également sur des patients très âgés (moyenne: 85 ans) hébergés en institution d'accueil, atteints pour la plupart de démence (73%). Outre la présence du biais de période d'immortalité mentionné précédemment, les résultats présentés sont pour le moins... surpenants: un pourcentage de mortalité de 62% chez les sujets "non traités" (càd n'ayant pas pris HCQ+AZ plus de 5 jours) et, après ajustement (régression multivariée) pour certains facteurs de confusion, un OR (odds ratio, ou "rapport de cotes") de 38 pour le fait d'être de sexe masculin plutôt que de sexe féminin... Un résultat jamais vu dans d'autres études sur la covid-19 (par comparaison, dans l'étude de Ly et al. portant sur une population similaire, ce rapport de cotes est de 4, tandis que le pourcentage de mortalité chez les patients "non traités" est de 26%).
* L'étude (non publiée) de [Sulaiman et al.](https://www.medrxiv.org/content/10.1101/2020.09.09.20184143v1) a été discutée [ici](https://rechercheindependante.blogspot.com/2020/05/les-etudes-sur-lhydroxychloroquine-hors.html). Le groupe traité par HCQ ne contient que 10 patients de plus de 65 ans (sur 1817), contre 154 (sur 3754) dans le groupe traité, soit proportionnellement 8 fois moins dans le groupe traité. Cela fait douter certains de la pertinence de l'étude (voir les commentaires en bas de l'article sur [medRxiv](https://www.medrxiv.org/content/10.1101/2020.09.09.20184143v1)). On notera également (table 4 de l'article) des résultats étonnants après ajustement pour plusieurs facteurs de confusion (dont l'âge), tels qu'un OR significativement inférieur à 1 pour le fait d'avoir plus de 65 ans (comparé à... avoir moins de 18 ans), et aucun OR significatif pour les comorbidités généralement identifiées comme facteurs de risque pour la covid-19.
* L'étude de [Guisado-Vasco et al.](https://www.sciencedirect.com/science/article/pii/S2589537020303357) ne montre pas d'effet statistiquement significatif du traitement par HCQ, même lorsqu'il est entamé avant admission à l'hôpital, une fois que les résultats sont ajustés pour les facteurs de confusion identifiés ([figure 2](https://www.sciencedirect.com/science/article/pii/S2589537020303357#fig0002) de l'article).

En conclusion, aucune des études rapportant un effet statistiquement significatif de l'HCQ en traitement précoce n'est fiable. Il est donc totalement injustifié d'en conclure à une amélioration globale de 77% (résultat affiché le [27/12/2020](https://archive.vn/SGefy)) de l'incidence de mortalité par l'HCQ.


