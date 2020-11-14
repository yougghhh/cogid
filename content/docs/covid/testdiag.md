---
title: Fiabilité des tests
weight: 3
bookhidden: true
---


## **Introduction**

Vous avez peut-être vu passer sur le web des articles et/ou vidéos mettant en garde contre la "fiabilité" des tests utilisés pour le diagnostic du covid-19. Ces mises en garde sont de deux types:
 1. Celles attirant l'attention sur le fait que la confiance qu'on peut accorder au résultat d'un test dépend de la _prévalence_ de la maladie, çàd de la proportion de personnes malades dans la population considérée (voir par exemple [Klein2020](https://tracts.gallimard.fr/fr/products/tracts-de-crise-n-25-je-ne-suis-pas-medecin-mais), [Yungster2020](https://medium.com/@niryungster/where-you-live-affects-what-your-covid-19-test-means-a9cd798fcd10));
 2. Celles concernant "l'hypersensibilité" des tests PCR, qui conduirait à considérer comme contagieux des individus "sains" (voir par exemple [cet article](https://www.lemonde.fr/les-decodeurs/article/2020/09/09/covid-19-l-hypersensibilite-des-tests-pcr-entre-intox-et-vrai-debat_6051528_4355770.html)).

Cette page fait le point sur la première problématique. Elle est en grande partie basée sur cet [excellent article](https://www.zeterinaires.fr/nofakemed/2020/04/29/tests-diagnostiques-comment-pas-fiables/), mais explicite également les raisonnements "bayésiens" qui sous-tendent les résultats mentionnés, afin qu'elle puisse être utilisée dans un cadre pédagogique comme exemple d'application du calcul des probabilités.


La seconde polémique est abordée dans un article distinct.


## **Concepts préalables**

Tout d'abord, il faut clarifier ce qu'on entend par "fiabilité" d'un test diagnostic. En réalité, cette notion n'est pas quantifiable par un seul nombre, mais repose sur deux caractéristiques complémentaires d'un test diagnostic:

 * la _sensibilité_, c'est-à-dire la capacité du test à détecter la maladie lorsqu'elle est présente (ne pas "passer à côté"). La sensibilité est liée à la notion de _faux négatif_: plus la sensibilité est grande, moins il y a de faux négatifs, càd de malades non détectés par le test ("l'alarme sonne toujours" quand l'individu est malade).
 * la _spécificité_, c'est-à-dire la capacité du test à ne détecter _que_ cette maladie (ne pas la confondre avec une autre affection).  La spécificité est liée à la notion de _faux positif_: plus la spécificité est grande,  moins il y a de faux positifs, càd d'individus sains identifiés erronnément comme malades ("l'alarme ne sonne que" lorsque l'individu est malade).


En utilisant le langage des probabilités, on peut résumer ces informations de la manière suivante: 
\begin{align*}
\text{Sensibilité}&=\mathbb{P}(\oplus\vert malade) = 1- \mathbb{P}(\ominus \vert malade)   \\\\
\text{Spécificité}&=\mathbb{P}(\ominus\vert sain) = 1- \mathbb{P}(\oplus \vert sain) 
\end{align*}
où la notation  \\(\mathbb{P}(A \vert B)\\) représente la probabilité de l'événément A étant donné l'événement B (on parle de _probabilité conditionnelle_). Le symbole \\(\oplus\\) signifie que le résultat du test est positif et le symbole \\(\ominus\\) signifie que le résultat du test est négatif.


## **Exemples**

Considérons le cas d'un test diagnostic dont la sensibilité est de 70\% et la spécificité de 99\%, qui sont les ordres de grandeur des valeurs pour les tests PCR utilisés pour le diagnostic du covid-19 (voir par exemple [ref]). 

Etant donné ces valeurs et les définitions ci-dessus, on est généralement enclin à penser que
 * si le résultat du test est positif, on a 70\% de chances d'avoir effectivement la maladie, et 30\% de chances d'ête un ``faux positif'';
 * si le résultat du test est négatif, on a 99\% de chances de n'être effectivement pas malade, et 1\% de chances d'être un ``faux négatif''.


En réalité, ce raisonnement est incorrect, comme on peut le comprendre facilement sur l'exemple chiffré que voici.

Supposons que la prévalence de la maladie dans la population générale est de 1\%, et que l'individu est testé dans le cadre d'un dépistage massif, çàd sans suspicion particulière qu'il soit malade. Supposons également que la population en question compte 10000 individus (ce nombre n'a pas d'importance, il est choisi pour la commodité des calculs). Dans cette population, il y a donc 10000/100=100 individus malades. Etant donné la sensibilité du test, 70 des 100 individus malades seront testés positifs et 30 d'entre eux seront testés négatifs. Avec une spécifité de 99\%, on peut aussi déduire que parmi les 9900 individus non-malades, il y aura 0,99 x 9900 = 9801 individus seront testés négatifs et 0,01 x 9900 = 99 individus qui seront testés positifs.

Examinons tout d'abord ce que cela implique pour la probabilité d'être malade lorsqu'on est testé positif. Pour calculer cette probabilité, il faut rapporter le nombre d'individus malades et testés positifs (70) au nombre total d'individus testés positifs (70+99). Ainsi, la probabilité d'être malade en étant testé positif (qu'on appelle la _valeur prédictive positive_, abbréviée VPP) vaut 70/(169)=0,41, càd 41\% et non 70\% (valeur de la sensibilité). Il y a donc réciproquement 59\% (et non 30\%) de faux positifs.

Les articles/vidéos à "sensation" s'arrêtent souvent à ce résultat et en concluent qu'un tel test est inutile, voire contre-productif: en effet, dans le cas d'une maladie contagieuse comme le covid-19, il nous conduirait à mettre en quarantaine beaucoup trop d'individus en réalité non porteurs de la maladie.
Cette conclusion est trop hâtive pour plusieurs raisons. 

Tout d'abord, il faut également examiner la probabilité d'être malade lorsqu'on est testé négatif. Le nombre d'invididus malades et négatifs étant égal à 30, et le nombre total d'individus testés négatifs étant 30+9801, on obtient une probabilité de 30/9831= 0,003. Ainsi, la proportion de faux négatifs est extrêmement faible: 0,3\% (et la valeur prédictive négative, ou VPN, est de 99,7\%). Autrement dit, le risque de considérer comme sains des individus en réalité infectés (beaucoup plus grave que le risque de faux positif, dans le cas d'une maladie contagieuse)  est quasi nul.

Ensuite, et c'est là le plus important, ces conclusions sont considérablement différentes si la prévalence de la maladie dans la population est plus grande, ou si le test n'est pas effectué dans le cadre d'un dépistage massif. Par exemple, si on refait le raisonnement précédent en supposant une prévalence de 5\%, on se rend compte que la VPP passe de 0,41 à 0,79 (elle devient donc supérieure à la sensibilité, qui vaut 0,7). Mais surtout, ce raisonnement ne tient pas compte du fait que la plupart des tests diagnostics ne sont pas effectués "au hasard" (c'est le cas seulement pour les campagnes de dépistage massif), mais sur base d'une suspicion préalable de de contamination (soit parce que l'individu présente des symptômes, soit parce qu'il a été en contact avec une personne contaminée). Or, le calcul effectué sur base de la prévalence de la maladie dans la population générale n'est pas valable dans ce cas. La manière la plus commode de calculer les probabilités dans le cas général est présenté ci-dessous.


## **Formalisation du raisonnement**

On peut montrer que le raisonnement informel présenté dans la section précédente est équivalent à appliquer la _formule de Bayes_:

$$\mathbb{P}(A \vert B)= \frac{\mathbb{P}(\text{A et B})} {\mathbb{P}(B) } = \frac{\mathbb{P}(B \vert A)\mathbb{P}(A)} {\mathbb{P}(B) } $$

(pour une présentation intuitive de ce résultat, voir par exemple 
[cette vidéo](https://youtu.be/X0gYOzxua64?t=33) en français et [cette vidéo](https://www.youtube.com/watch?v=HZGCoVF3YvM) en anglais).

Dans le cas des tests diagnostics considéré ici, on a donc notamment:

\begin{align*}
\mathbb{P}(sain \vert \oplus) & =  \frac{ \mathbb{P}(\oplus \text{ et sain})} {\mathbb{P}(\oplus) } = \frac{\mathbb{P}(\oplus \vert sain)\mathbb{P}(sain)} {\mathbb{P}(\oplus) }  \\\\
\mathbb{P}(malade\vert \ominus) & = \frac{\mathbb{P}(\ominus \text{ et malade})} {\mathbb{P}(\ominus) }= \frac{\mathbb{P}(\ominus \vert malade)\mathbb{P}(malade)} {\mathbb{P}(\ominus) }  
\end{align*}
qui donnent, respectivement, les probabilités de faux positif et de faux négatif.
En utilisant les propriétés que
$$ \mathbb{P}(\oplus) = \mathbb{P}(\oplus \vert sain)\mathbb{P}(sain) + \mathbb{P}(\oplus \vert malade)\mathbb{P}(malade), $$
$$ \mathbb{P}(\ominus) = \mathbb{P}(\ominus \vert malade)\mathbb{P}(malade) + \mathbb{P}(\ominus \vert sain)\mathbb{P}(sain),$$ 
$$\mathbb{P}(sain)=1 - \mathbb{P}(malade)$$

et l'abbréviation $P_m=\mathbb{P}(malade)$, on peut encore écrire:


\begin{align*}
P_{pFP} & = \frac{(1-Sp)\;(1 -P_m )} {(1-Sp)\;(1 -P_m ) + Se\;P_m } = 1 - \text{VPP}\\\\
P_{pFN} & = \frac{(1-Se)\;P_m} {(1-Se)\;P_m+ Sp\;(1 -P_m )}  
= 1 - \text{VPN}
\end{align*}

où $Se$ est la sensibilité et $Sp$ la spécificité du test telles que définies plus haut. 

On peut vérifier que ces formules permettent de retrouver les résultats obtenus dans la section précédente (sans devoir spécifier la taille de la population) à condition de remplacer 
\\(\mathbb{P}(malade)\\) par la prévalence de la maladie dans la population.
Cependant, cette probabilité *a priori* d'être malade, \\(\mathbb{P}(malade)\\), n'est égale à la prévalence de la maladie que dans le cas d'un dépistage massif, où l'individu est testé sans indication particulière qu'il soit infecté. Lorsque l'individu est testé sur base d'une suspicion de contamination, il faut remplacer la prévalence par la probabilité estimée *a priori* qu'il a été contaminé. Bien sûr, cette probabilité n'est pas facile à estimer - elle va dépendre des informations à disposition du médecin, et peut-être aussi de son expérience préalable de la maladie (identification correcte des symptômes,...). C'est pourquoi on dit parfois que l'approche bayésienne du calcul des probabilités est "subjective". L'estimation dépend en tout cas crucialement des informations à disposition pour effectuer les calculs.

Pour fixer les idées, si on estime à 50\% la probabilité a priori de l'individu d'être malade, avec les mêmes valeurs de sensibilité et de spécificité que dans la section précédente, la probabilité de faux positif  \\(\mathbb{P}(sain\vert \oplus) \\)
ne vaut plus que 1\%, tandis que la probabilité de faux négatif 
\\(\mathbb{P}(malade \vert \ominus) \\)  vaut alors 23\%.

Le graphique [ici](/docs/covid/plot_fct_diag.html) illustre cette dépendance très forte des probabilités de faux positif et faux négatif à la probabilité a priori d'être malade.

## **Conclusions**

 * Le dépistage massif d'une maladie dans une population ne peut se faire qu'avec des tests de sensibilité et de spécificité très grandes. Le même raisonnement s'applique à l'évaluation du niveau d'immunité au sein d'une population. C'est pour cette raison qu'il est actuellement inutile d'effectuer des tests sérologiques à large échelle pour l'immunité vis-à-vis du covid-19: la sensibilité et la spécificité des tests disponibles actuellement est insuffisante pour cela \citep{zete0420}.
 *  Si notre intuition est mise à mal par les raisonnements bayésiens lorsque les probabilités a priori des événements sont faibles, ces probabilités sont en réalité importantes en pratique dans le cas de tests diagnostics. En effet, ce type de test est rarement effectué ``au hasard'', mais sur base d'un faisceau d'indications _a priori_ que l'individu est porteur de la maladie. Il n'y a donc souvent pas lieu en pratique de s'inquiéter de ces résultats contre-intuitifs... et de nombreux vulgarisateurs feraient mieux de pousser le raisonnement jusqu'au bout plutôt que d'alerter la population inutilement.