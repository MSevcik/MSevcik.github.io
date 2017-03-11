---
layout: post
title:  "Webové Publikovanie Zadanie 1"
date:   2017-03-11 09:19:00 +0100
categories: jekyll update
img: /img/wp1.png
toc: true
---
# Intro

Ako prvé zadanie na Webové Publikovanie sme mali vytvoriť statické webové sídlo pomocou Jekyll a nahodiť to na internet pomocou Github Pages. V rámci zadania sme mali splniť nasledujúce body:

- Sídlo musí obsahovať aspoň 5 podstránok, pri využití aspoň 3 rôznych rozložení (layout-ov)
- V rámci šablón musí byť použité:
	- aspoň 5 premenných
	- kolekcie alebo dátové súbory 
	- aspoň 5 filtrov alebo tagov
	- aspoň 1 plugin (okrem pagination)

V tomto článku postupne prejdem všetkými bodmi a popíšem kde sa čo nachádza. Ešte na úvod by som chcel povedať, že na vizuálnu stránku bol využitý Bootstrap.

# 5 Podstránok a 3 layouty

<figure>
  <img src="/img/pages.png">
  <center><figcaption>Obrázok 1. - 5 podstránok na navigačnej lište</figcaption></center>
</figure>

Ako je vidno na Obrázku 1. na stránke je rovno v navigácií 5 podstránok. Na stránke sa používajú nasledujúce layouty:

- Home - layout pre domovskú stránku, tu som sa vyhral s bootstrapom, pretože som vždy chcel vyskúšať použit ich Carousel,
- default - layout obsahujúci navigačnú lištu a základné prvky stránky,
- post - layout pre blog posty,
- profile - layout pre profil,
- projects - layout pre projekty.

# 5 Premenných

Na stránke sa využíva veľa premenných napríklad aj v tomto poste sa využívajú hneď 4 sú to:
- title,
- date,
- img,
- categories.

Stránka projektov tiež obsahuje niekoľko premenných ako title, sub, desc, dataanchor ktoré slúžia na naplnenie layoutu a na naplnenie stránky danými projektami. Profil rovnako obsahuje premené, ktoré tvoria základ profilovej stránky.

# Dátové súbory

Na stránke som použil dátový súbor. Momentálne by sa mohol zdať veľmi umelý ale ak by som chcel vytvoriť viacej stránok s viacerímy projektami rýchlo by sa stal veľmi šikovným.

Vyzerá nasledovne:

{% highlight yaml %}
wp:
  - name: Zadanie 1. Osobná webová prezentácia na GitHub pages
    link: /wp/first
    desc: Vytvorit statické webové sídlo pomocou Jekyll a Github pages. Vnútri je opísané ako som pri vytváraní postupoval.
{% endhighlight %}

Ak by som napríklad chcel pridať projekt do webového publikovania pridal by som tam dalšiu položku - name: ... link: ... a desc: ... . Ak by som však chcel pridať napríklad projekt z iného predmetu vytvoril by som si nový záznam napríklad java: a do tohoto záznamu by som mohol písať nejaké jeho vlastnosti. Z tohoto data file-u sa napĺňa layout projects, kďe sa záznam vyberá na základe premennej dataanchor.

# Filtre a tagy

Tento bod sa mi podarilo splniť pomerne rýchlo. Na domovskej stránke je pomocou bootstrapu vytvorený carousel ktorý sa plní troma najnovšími blog postmi. Toto sa da nájsť v layoute home. Samozrejme to nieje jediné miesto kde sú tagy a filtre použité. Používajú sa takmer vo všetkých stránkach.

# Plugin

Na stránke sú použité dva pluginy. Jeden pridáva špecialny filter ktorý vyráta ako dlho trvá prečítanie článku na základe počtu slov. To sa vypisuje na podstránke blog. Druhý pridáva do blog postov obsah. Je to vidno aj priamo v tomto poste.

# Záver

Na záver by som chcel povedať, že som sa celkom bavil pri vytváraní tejto stránky. Na cssko som využil bootstrap a snažil som sa zachovať čo najjednoduchší dizajn. Celý projekt sa nachádza na mojom [Githube](https://github.com/MSevcik/MSevcik.github.io).