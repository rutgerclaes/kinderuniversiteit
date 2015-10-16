Vandaag leer je programmeren.  Je leert hoe je vanuit een software programma lampjes kan aansturen.  Met die lampjes kan je bijvoorbeeld een verkeerslicht maken.

## Bouwblokken

We gaan vandaag op een bijzondere computer werken: een *Raspberry Pi*.  Dat is een erg kleine computer die je gemakkelijk toelaat andere dingen, zoals lampjes, aan te sturen.

![Raspberry Pi computer](images/raspberrypi.jpg)

Bovenop die computer gebruiken we een *Traffic Hat*.  Dit bordje heeft 3 LEDs, een drukknop en een zoemer.  Al die dingen zijn 
verbonden met de computer via pinnetjes. Je computer kan dan signalen versturen over die pinnetjes en zo de lampjes, zoemer en knop besturen.

![TrafficHat bord](images/traffichat.jpg)

Op de computer gaan we software schrijven.  Dat doen we in een taal die *Scratch* noemt.  Je kan met Scratch programma's maken zoals spelletjes.  Je kan met Scratch op een Raspberry Pi ook de lichtjes, zoemer en drukknop van het verkeerslicht aansturen.

![Scratch programmeer omgeving](images/scratch.png)

## Scratch

Je kan Scratch starten door op je bureaublad op het kat icoontje te drukken.

![Scratch icoon](images/icon.png)

Je krijgt dan dit te zien

![Scratch programmeer omgeving en GPIO melding](images/scratch-gpio.png)

Die boodschap wil zeggen dat Scratch klaar is om je verkeerslicht aan te sturen.  Dit is een Scratch venster waarin de bouwblokken voor het verkeerslicht al gemaakt zijn.

![Scratch blokje](images/traffichat-block.png)

Om Scratch samen met het verkeerslicht te gebruiken moet je deze blokjes altijd in je programma hebben staan.  Ze vertellen Scratch dat je met een TrafficHat zal werken.

Tip: de andere blokjes kan je best ook ergens in je venster laten, dan kan je ze gemakkelijk kopieren (rechtermuisclick -> kopieren).

### Scratch blokjes

Elk van die blokjes is een instructie voor je computer.  Als je blokjes aan elkaar hangt zullen ze in die volgorde uitgevoerd worden.

![Scratch blokjes](images/sequence.png)

Deze blokjes zullen bijvoorbeeld eerst het rode lampje aanzetten.  Daarna 2 tellen wachten en dan het rode lampje terug uitschakelen.

Opgelet, indien er geen 'wacht' tussen een aan en een uit signaal staat zal het lampje enkel het eerste signaal ontvangen en dus niet uitgaan.

### Herhalen

Je kan het uitvoeren van blokjes herhalen.  Het programma hieronder zal het rode lichtje 10 keer laten knipperen.  Het `herhaal` blok herhaalt de blokjes die er in zitten 10 keer.

![Herhalen in Scratch](images/repeat.png)

### Kiezen

Je kan in je programma ook keuzes maken.  In het programma hieronder vraagt de
Scratch kat op het computer scherm welke kleur er moet gaan branden. De gebruiker kan dan een antwoord invullen in het tekstvakje onder de kat. Daarna kiest
het programma op basis van het antwoord welk lichtje gaat branden.

![Kiezen in Scratch](images/choice.png)

### Lichtjes bedienen

Je kan de lichtjes bedienen door een *signaal* te verzenden.  Dat signaal is dan een kleur ( `red`, `green`, `orange` ) samen met `on` om de lamp aan te zetten of `off` om de lamp uit te zetten.

![De lampjes aan en uit zetten](images/leds.png)

### Zoemer bedienen

De zoemer bedien je net zoals de lichtjes.  Je stuurt een signaal naar de `buzzer`.  Gebruik de zoemer niet te vaak, anders gaat iedereen vanavond met hoofdpijn naar huis.

![De zoemer aan en uit zetten](images/buzzer.png)

### Drukknop gebruiken

De drukknop gebruiken is wat moeilijker.  Je kan in je programma wachten tot er
op de drukknop gedrukt wordt.  Onderstaand voorbeeld zal bijvoorbeeld het rode
lampje laten branden totdat er op de knop gedrukt wordt.  Daarna gaat het
lampje 2 tellen uit en start het programma opnieuw.

![De drukknop gebruiken](images/button-sequence.png)

In Scratch kan je ook <i>interne</i> signalen versturen, die een ander stukje van je programma kunnen activeren. Ken je al een beetje Scratch en wil je met zo een signalen werken?  Dat kan zeker.  Bijvoorbeeld, je kan je push butten een intern signaal laten verzenden, als volgt:

![De drukknop een signaal laten verzenden](images/button-signal.png)

### Overige blokjes

Kijk eens rond in de verschillende categorien van blokjes. Er bestaan bijvoorbeeld ook blokjes om de kat iets te doen zeggen, om de tijd te meten, om een willekeurig getal te genereren, om variabelen te maken enzomeer.

## Opdrachtjes

We starten allemaal samen met een eenvoudig voorbeeldje.  Daarna mag je bouwen
wat je wil.  Een verkeerslicht, een spelletje of iets anders.  Je kan de
lichtjes, de zoemer en de drukknop gebruiken zoals je zelf wil.  Als je niet
direct weet wat te doen hebben we hier zelf wat ideetjes.

### Een eenvoudig verkeerslicht

Maak een eenvoudig verkeerslicht dat:

1. Eerst 6 tellen rood is
2. Daarna 6 tellen groen is
3. Daarna 2 tellen oranje is
4. Terug rood wordt

Het verkeerslicht blijft zo maar verder veranderen in de volgorde die jij programmeert.

### Een verkeerslicht voor voetgangers

Maak een verkeerslicht voor voetgangers dat steeds rood is. Als een voetganger wil oversteken ken die via de drukknop vragen om direct groen te worden. Daarna moet het verkeerslicht oranje en daarna weer rood worden.

### Reactietijd testen

Maak een programma dat iemands reactietijd kan testen.  Laat eerst alle drie de lichtjes branden en doe ze daarna één voor één uit.  Wanneer het laatste lichtje uit is moet je zo snel mogelijk op de knop drukken.  Je programma meet de tijd.

### Een verkeerslicht voor blinden

Maak een verkeerslicht voor blinden.  Maak een verkeerslicht dat rood, groen en oranje wordt.  Wanneer iemand op de knop drukt zal tijdens de volgende groene periode de zoemer geluid maken.  Als niemand op de knop gedrukt heeft moet de zoemer geen geluid maken.

### Simon Says

Maak een geheugen spelletje.  Je spelletje laat een aantal lampjes branden.  Elk lampje komt overeen met een toets op het toetsenbord (bijvoorbeeld rood: J, geel: K en groen: L).  De speler moet op het keyboard die toetsen in dezelfde volgorde indrukken om naar het volgende level te gaan.  In het volgende level zullen er meer lampjes gaan branden.

### Reactietijd uitbreiding

Maak een programma dat reflexen en reactietijd meet. Laat ofwel het groene lampje, ofwel alle lampjes branden. Indien het groene lampje brand meet je de reactietijd voor de gebruiker op de knop duwt. Indien alle lampjes branden en de gebruiker duwt op de knop is hij mis en laat je bijvoorbeeld de zoemer gaan.

