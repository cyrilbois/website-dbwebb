---
author: moc
revision:
    "2020-01-13": (A, moc) Skapad inför VT21.
category:
    - oopython
...
Bygg en bank med flask
===================================

[FIGURE src=/image/oopython/kmom02/bank.png?w=c5 class="right"]

Uppgiften går ut på att med hjälp av klasser, Flask, jinja2 och CSS, skapa en webbsida där man kan flytta pengar och räkna på räntor.

<!--more-->


Förkunskaper {#forkunskaper}
-----------------------

Du har gått introduktionskursen i Python.  
Du har läst artikeln "[GET, POST i Flask](kunskap/flask-get-post)".  
Du har läst guiden "[Klass relationer](guide/kom-igang-med-objektorienterad-programmering-i-python)".  



Introduktion {#intro}
-----------------------    

Du jobbar vid sidan om dina studier och din kund vill att du gör klart en webbsida som redan är påbörjad. Gränssnittet och routes för sidan är redan klart, du ska skapa klasserna för backend:en till webbsidan. I och med att frontend redan är klar och innehåller anrop till koden du ska skapa behöver dina klasser uppfylla abstraktionskraven som det medför. Med det menas att i dina klasser behöver det finnas vissa metoder och attribut med rätt namn, annars kommer inte frontend fungera med din backend. I klassdiagrammet nedanför kan du se vilket gränssnitt din klasser måste uppfylla. Med gränssnitt menas existerande publika metoder.

[YOUTUBE src=PCGwx_wpzME width=630 caption="Så här kan det se ut när det är färdigt."]

Du ska implementera klasserna för person klassen, de två kontotyperna och handlern som app.py jobbar mot.

[FIGURE src=/image/oopython/kmom02/bank_uml.png caption="Klassdiagram för uppgiften."]

Attributen och metoderna som är **bold**-markerad används av den färdiga koden ni får och måste därför implementeras av er med de namnen. Övriga är bara exempel på vad man kan ha med.

[YOUTUBE src=GBmyT_TntXA width=630 caption="Andreas förklarar klassdiagrammet och koden som ska skrivas."]

Appen följer överlag samma struktur som i övningen, den enda skillnaden är att vi skall använda oss av en json-fil för att spara den dynamiska data som applikationen inte kommer ihåg mellan request:en. Ett tips, när du börjar utveckla en ny metod som anropas från den färdiga koden, använd dig av `print()` i metoden du skapar och kolla klassdiagrammet för att ta reda på vad som skickas som argument till din metod.

[YOUTUBE src=rqfqn29glIo width=630 caption="Hur ska man börja med bank uppgiften?"]


Krav {#krav}
-----------------------

Börja med att kopiera frontend koden till ditt uppgift.

```bash
# Ställ dig i kurskatalogen
# börja med att uppdatera mappen med senaste exempelkoden
dbwebb update
cp -ri example/flask/bank me/kmom02/
cd me/kmom02/bank
```

1. Kolla på youtube-klippen ovanför för att få en översyn av vad du ska göra.

1. Bekanta dig med koden, kolla igenom app.py för att se vilka routes som finns och vilka html filer som används till vad. Leta efter alla anrop som görs till klasserna du ska skapa så att du får en bild av vilka metod som behövs och vad de används till.

1. Skapa filen `static/data/accounts.json` där du lägger in den data du behöver för att återskapa alla klasser. Filen skall automatiskt läsas in när en ny instans av `AccountManager` skapas. Uppdateras något (t.ex. ens kontobalans) skall ändringarna också skrivas till filen.  
Strukturen på filen väljer du själv, kodbasen innehåller ett [exempel](https://github.com/dbwebb-se/oopython/tree/master/example/flask/bank/static/data/accounts-example.json) du kan utgå ifrån.

1. Implementera klasserna som behövs i filerna `handler.py`, `persons.py` och `accounts.py`. Totalt skall det minst finnas tre konton av varje typ.


1. Handlern ska äga alla tillgängliga konton, kunna överföra pengar mellan två konton samt, räkna ut den ränta man kommer till att få mellan dagens datum till den som skickas in från datepickern.  
Det ska finnas metoder för att hämta alla konton, hämta ett specifikt konto, lägga till ett nytt konto samt hantera json-filen.

1. Ett konto skall få sitt `_id` tilldelad från klass variabeln `Account.account_number`, den skall ej skickas med i konstruktorn.  
`interest_rate` representerar hur många `%` balansen ökar med under ett år.  
`transaction_fee` säger procenten som skall dras av det överförda beloppet. Överför man exempelvis 100kr med en avgift på 1%, skall 100kr dras från kontot men mottagaren ska endast få 99kr insatta.


1. `SavingsAccount` har en extra överföringsavgift och högre dag-för-dag ränta beroende på hur gammal ägaren är. Denna skall motsvara `0.1%` av hens ålder.

1. Du ska inte behöva ändra i några av de andra filerna, förutom kanske style.css, men om du känner att du vill/behöver det skriv varför i din redovisningstext.

```bash
# Ställ dig i kurskatalogen
dbwebb validate bank
dbwebb publish bank
```

Rätta eventuella fel som dyker upp och validera igen. När det ser grönt ut så är du klar.



Extrauppgift {#extra}
-----------------------

Det finns inga extrauppgifter.



Tips från coachen {#tips}
-----------------------

Validera ofta. Så slipper du en massa valideringsfel i slutet av övningen.

Lycka till och hojta till i discord om du behöver hjälp!