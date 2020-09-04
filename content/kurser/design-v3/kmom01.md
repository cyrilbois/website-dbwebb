---
author:
  - nik
  - efo
  - mbn
# views:
#     flash:
#         region: flash
#         template: default/image
#         data:
#             src: "image/snapht18/design-kmom01-me.png?w=1100&h=360&a=12,10,40,2&f1=pixelate,8,2&cf&nc&f2=colorize,0,30,0,0"
revision:
    "2020-08-25": (A, nik) Mall för kursmoment
...
Kmom01: Ramverk, innehåll, style
====================================

Vi ska ta oss en titt på den mjukare delen av webbprogrammering, webbdesign och användbarhet. Det handlar också om snabba sidomladdningar, sökmotoroptimering, att skriva för webben och hur vi väljer att organisera webbplatsens material. Vi ska även kolla över de tekniker som används för att uppnå detta.

<!--more-->

Denna kurs erbjuder möjligheten att dyka in i CSS-kodande och att med hjälp utav SASS strukturera upp och optimera sin CSS-kod. Den ger också insyn till vad som är grundstenarna för "god design". Genom kursen försöker vi finna tekniska sätt, för en programmerare, att jobba och implementera "god design" i en webbplats. Vi studerar också vissa aspekter av begreppet användbarhet som påverkar användarens upplevelse av webbplatsen.

För att komma igång snabbt så använder vi en befintlig webbplats som grund till vår portfolio. Webbplatsen bygger på ett PHP-ramverk som heter [Pico](http://picocms.org/). Det är ett tunt ramverk som tillåter oss att lägga upp sidor skrivna i Markdown och hantera vår layout med hjälp utav Twig, som är en påbyggnation av HTML.

I första kursmomentet inleder vi med att installera labbmiljön, läsa lite kring teknikerna vi ska använda samt skapa en portfolio och ge den style med hjälp av CSS. I slutet av kursmomentet ska portfolion publiceras till studentservern och till Github.

Under kursens gång så kommer du att introduceras till ett par tekniker som är bra att ha för en webbprogrammerare. En av de är versionshantering med Git och Github.

<small><i>(Detta är instruktionen för kursmomentet och omfattar det som skall göras inom ramen för kursmomentet. Momentet omfattar cirka **20 studietimmar** inklusive läsning, arbete med övningar och uppgifter, felsökning, problemlösning, redovisning och eftertanke. Läs igenom hela kursmomentet innan du börjar jobba. Om möjligt -- planera och prioritera var du vill lägga tiden.)</i></small>



Labbmiljön  {#labbmiljo}
---------------------------------

*(ca: 2-4 studietimmar)*

Det finns en [längre beskrivning om kursens labbmiljö](./../installera-labbmiljo). Läs den om du är osäker på vad som skall göras, eller om detta är din första dbwebb-kurs.

Den korta varianten är att du behöver [installera labbmiljön](./../labbmiljo), uppdatera [dbwebb-cli](dbwebb-cli) samt klona och initiera kursrepot.

```text
# Gå till din katalog för dbwebb-kurser
dbwebb selfupdate
dbwebb clone design
cd design
dbwebb init
```



Läs & Studera  {#lasanvisningar}
---------------------------------

*(ca: 8-10 studietimmar)*



### Kurslitteratur  {#kurslitteratur}

TBA



### Design med HTML5 och CSS3  {#guide}

1. Läs igenom följande sektion i guiden "[Design med HTML5 och CSS3](guide/design-med-html5-och-css3)".
    * [Grunderna](guide/design-med-html5-och-css3/grunderna)

I guiden tittar vi på hur vi kan använda CSS tillsammans med HTML för att implementera designprinciper. I sektionen [Grunderna](guide/design-med-html5-och-css3/grunderna) tittar vi på grundläggande struktur för HTML och på vilka sätt vi kan applicera styling med CSS.



### Markdown {#markdown}

Läs följande för att lära dig grunderna i textformatet Markdown. Markdown är ett populärt format för att låta användaren skriva text som är läsbar för ögat men ändå enkel att konvertera till HTML med en parser. I kursen kommer du att skriva dina webbsidor med Markdown.

1. Kika på vad Markdown innebär genom att läsa [John Grubers introduktion till Markdown](https://daringfireball.net/projects/markdown/basics). För att testa själv så öppnar du en [Gist](https://gist.github.com/) och skriver i Markdown, det gör att du kan testa olika konstruktioner under tiden som du läser om dem.


### Git & GitHub {#git}

I kursen introduceras Git och GitHub. Git är ett versionshanteringssystem för kod och GitHub är en webbplats där man kan ladda upp sitt Git-repo och använda extra tjänster.

1. Bekanta dig kort med [dokumentation på Gits hemsida](https://git-scm.com/doc). Där finner du referensinformation, en onlinebok om Git och ett antal korta videor som ger dig grunderna till vad Git och versionshantering handlar om.

1. Skaffa dig ett konto på [GitHub](https://github.com/). Du behöver det för att ladda upp och publicera ditt Git-repo. Det är gratis med konto och att ladda upp publika repon.

1. Ägna en stund åt att bekanta dig med webbplatser för GitHub. Du kan även kort och översiktligt kika på de guider och videor som finns för GitHub. Notera att de täcker så mycket mer än vad vi kommer jobba med i kursen så det kan räcka att du endast noterar att det existerar [guider för hur man jobbar med GitHub](https://guides.github.com/).



### CSS {#css}

I detta kursmomentet jobbar vi med CSS. Läs följande.

1. I online boken "[SMACSS Scalable and Modular Architecture for CSS](http://smacss.com/book/)" läser du följande korta kapitel för inspiration av en variant till hur man kan tänka när man skriver CSS i större sammanhang.
    * Introduction
    * Categorizing CSS Rules
    * Base Rules
    * Layout Rules



Övningar & Uppgifter  {#ovningar_uppgifter}
-------------------------------------------

*(ca: 8-10 studietimmar)*



### Uppgifter {#uppgifter}

Följande uppgift skall utföras och redovisas.

1. Lös uppgiften "[Bygg en portfolio sida](uppgift/skapa-din-egen-portfolio)". Du skall bygga en portfolio-sida som du taggar och publicerar på GitHub. Spara allt under `me/portfolio`.

1. Försäkra dig om att du har gjort `dbwebb publish portfolio` och taggat din inlämning med version 1.0.0 (eller högre) samt pushat repot inklusive taggarna till GitHub.



Resultat & Redovisning  {#resultat_redovisning}
-----------------------------------------------

*(ca: 1-2 studietimmar)*

Läs [instruktionen om hur du skall redovisa](./../redovisa).

Se till att följande frågor besvaras i redovisningstexten.

* Är du sedan tidigare van att jobba i ramverk för att bygga webbplatser?
* Det blev en del nya verktyg och tekniker i labbmiljön och för att jobba med portfolio-sidan, är du bekant med några av dem sedan tidigare?
* Har du några förutfattade meningar, eller kanske en etablerad övertygelse, inom design och användbarhet för webben?
* Hur kändes det att styla webbplatsen med CSS? Gick det bra?
* Vilken är din TIL för detta kmom?

TIL är en akronym för "Today I Learned" vilket leksamt anspelar på att det finns alltid nya saker att lära sig, varje dag. Man brukar lyfta upp saker man lärt sig och där man kanske hajade till lite extra över dess nyttighet eller enkelhet, eller så var det bara en ny lärdom för dagen som man vill notera.