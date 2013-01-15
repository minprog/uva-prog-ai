# Stijlgids

Als nakijkers van jouw practicum merken we al snel of iets goed leesbaar is of niet. Begrijpen we snel wat je code doet? Ook in de praktijk blijkt het handig om goed leesbare code te schrijven. Voor een ander, die je code moet uitbreiden, of voor jezelf, als je een tijdje niet naar de code gekeken hebt.

Er is niet één correcte manier om je code te schrijven. Maar je kunt zeker een hoop fout (of laten we zeggen, onleesbaar) doen. Bij dit vak eisen we niet dat je je aan een vastgelegde stijl houdt, maar we raden je ten strengste aan om de conventies hieronder in acht te nemen, tenzij je jouw assistent kunt overtuigen dat jouw manier net zo goed is, of beter.

## Commentaar

Teveel commentaar is fout. Te weinig commentaar is fout. Maar hoeveel is dan goed? Een vuistregel is om je code op te delen in kleine blokken — van elk een paar regels code — en elk blok van een regel commentaar te voorzien.

Eén van de volgende twee vragen is meestal zeer relevant om te beantwoorden:

* Wat doet dit blok code?
* Waarom is het op deze manier geïmplementeerd?

### Voorbeeld

Variabelenamen leggen vaak al een beetje uit waarvoor ze dienen, en maken je code leesbaarder. En zo leg je dan uit wat je *precies* opslaat in de variabele:

~~~ java
// compute student average
double average = (int) (sum / quizzes + 0.5)
~~~

Middenin je code schrijf je in principe geen volzinnen, maar om het leesbaar te houden zet je wel netjes een spatie na de `//`.

Dus niet zo:

~~~ java
//compute student's average
// Compute student's average.
~~~

Uitgebreider commentaar kan je tussen `/*` en `*/` zetten. Dit commentaar mag meerdere regels beslaan. Gebruik dit vooral bovenaan je bestand en boven methodes.

### Bovenaan je Java bestand

Zet bovenaan je bestand de problem set, je naam, studentnummer en een korte beschrijving van het programma. Zoals in het voorbeeld hieronder:

~~~ java
/*
 * Problem set 1.13
 *
 * Daan Smit
 * 1932819
 *
 * This program makes Karel the Robot walk from the left side of
 * the room to the right side, while putting a beeper down on 
 * every third step.
 */
~~~~

### Lange regels commentaar

Let op de omschrijving van het programma in het voorbeeld hierboven. De omschrijving paste niet meer op één regel, dus is een nieuwe regel toegevoegd, ook weer beginnend met een `*`.

## Structuur

### Lange regels code

Vermijd regels langer dan 80 tekens; zo weet je zeker dat het op elk scherm en op papier goed weergegeven kan worden. Er zijn meerdere methodes om regels af te breken. Je kan delen van een expressie in een variabele stoppen, of een parameters van een methode op de volgende regel zetten. Regels die het statement van de vorig regel afmaken zijn altijd ingesprongen:

~~~ java
anExtremelyLongMethodName(parameterOne,
    parameterTwo, parameterThree);
~~~

dat mag ook zo:

~~~ java
anExtremelyLongMethodName(parameterOne,
                          parameterTwo,
                          parameterThree);
~~~

### Indentatie

Indentatie of inspringen is het toevoegen van witruimte aan het begin van een regel om structuur zichtbaar te maken. Zoals in het voorbeeld hieronder waar de body van de while-loop met vier spaties is ingesprongen.

~~~ java
while (stack.hasNext())
{
    stack.pop();
}
~~~~    

Spring consistent in en doe dit alleen met de inhoud van een block-statement, dus niet met het statement zelf en ook niet met de accolades. Dus niet:

~~~ java
while (stack.hasNext())
    {
    stack.pop();
    }
~~~

Spring altijd op dezelfde manier in, met 4 spaties, of met tabs, gebruik geen spaties en tabs door elkaar. De aangeleverde bestanden springen allemaal in met 4 spaties het is daarom het makkelijkst dit aan te houden. Je kan gEdit instellen om 4 spaties in te voegen als je op tab drukt, kijk daarvoor in Preferences.

Om verloren tabs of spaties op te sporen kan je de zoekfunctie in gEdit gebruiken. Met `\t` kan je op tabs zoeken.

### Accolades

Plaats accolades bij voorkeur op de volgende regel net zoveel ingesprongen als het voorgaande statement. Je mag de openingsaccolade ook achter het voorgaande statement plaatsen zoals in het voorbeeld hieronder. De sluitaccolade gaat dan evengoed op een nieuwe regel.

~~~ java
while (stack.hasNext()) {
    stack.pop();
}
~~~
