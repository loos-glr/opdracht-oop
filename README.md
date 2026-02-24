### Oefenopdracht: Maak je eigen CyberPet! 🐾🤖

**Inleiding: Wat is OOP eigenlijk?**
Object-Oriented Programming (OOP) klinkt ingewikkeld, maar eigenlijk valt het mee. Het is een manier om code te schrijven die lijkt op de echte wereld. 

Denk aan een koekjesvorm. De vorm zelf is de **Class** (de blauwdruk). Je kunt de vorm niet opeten. Maar als je deeg hebt, maak je een echt koekje. Dat echte koekje is het **Object**. Met één vorm (Class) kun je honderden verschillende koekjes (Objecten) maken!



In deze opdracht gaan we de blauwdruk maken voor een digitaal huisdier: de `CyberPet`. Daarna wekken we hem tot leven!

---

#### Stap 1: De Blauwdruk maken (De Class)
We beginnen met het maken van de vorm (de blauwdruk). In JavaScript doe je dit met het woordje `class`.

**Jouw taak:** Maak de `CyberPet` class aan. 
*Let op de hoofdletter 'C', dat is een afspraak onder programmeurs voor classes!*

```javascript
// Typ dit over in je code-editor:
class CyberPet {
  // Hierbinnen gaan we straks de eigenschappen en acties bouwen
}
```

---

#### Stap 2: Eigenschappen geven (De Constructor)
Een huisdier heeft eigenschappen (properties), zoals een naam, een diersoort en een energielevel. Om deze in onze blauwdruk te zetten, gebruiken we een speciale fabrieksmethode: de `constructor`. 

Het woordje `this` is heel belangrijk hier. `this` betekent eigenlijk: *"van dít specifieke beestje"*.

**Jouw taak:** Vul de ontbrekende code in op de puntjes (`...`).
1. Zorg dat de `constructor` een `naam` en een `soort` binnenkrijgt.
2. Geef het beestje een standaard `energie` van 100.

```javascript
class CyberPet {
  constructor(naam, soort) {
    this.naam = ...;         // Vul in: de naam die wordt meegegeven
    this.soort = ...;        // Vul in: de soort die wordt meegegeven
    this.energie = 100;      // Elk nieuw beestje start altijd met 100 energie!
  }
}
```

---

#### Stap 3: Acties toevoegen (De Methods)
Een huisdier dat niks doet is saai. We gaan hem acties (methods) geven. Een method is eigenlijk gewoon een functie, maar dan binnen in een class. 

Als je CyberPet gaat spelen, kost dat energie. Als hij gaat slapen, krijgt hij zijn energie weer terug.



**Jouw taak:** Voeg de methods `spelen()` en `slapen()` toe onder de constructor.

```javascript
class CyberPet {
  constructor(naam, soort) {
    this.naam = naam;
    this.soort = soort;
    this.energie = 100;
  }

  // Actie 1: Spelen
  spelen() {
    this.energie = this.energie - 10; // Spelen kost 10 energie
    console.log(this.naam + " is aan het spelen! Energie is nu: " + this.energie);
  }

  // Actie 2: Slapen
  slapen() {
    // JOUW BEURT: Zet hier de code om de energie weer op 100 te zetten!
    // ...
    console.log(this.naam + " is aan het slapen. Zzz... Energie is weer vol!");
  }
}
```

---

#### Stap 4: Je CyberPet tot leven wekken (Het Object)
De blauwdruk is af! Nu gaan we het echte beestje maken. Dit noemen we "het object instantiëren". Hiervoor gebruiken we het toverwoord `new`.

**Jouw taak:** 1. Maak jouw eigen CyberPet aan en sla deze op in een variabele.
2. Laat je CyberPet een paar keer spelen en daarna slapen.

```javascript
// We gebruiken de blauwdruk (class) om een echt beestje te maken:
let mijnHuisdier = new CyberPet("Bifi", "Hond");

// Laten we testen of het werkt! Typ het volgende:
console.log("Ik heb een " + mijnHuisdier.soort + " gemaakt, hij heet " + mijnHuisdier.naam);

// JOUW BEURT:
// 1. Roep de spelen() method aan op mijnHuisdier
// 2. Roep hem nog een keer aan
// 3. Roep daarna de slapen() method aan.
// Kijk goed in je console wat er gebeurt!
```

---
### 🎉 Gefeliciteerd!
Als je dit werkend hebt, heb je zojuist je allereerste Object-Oriented programma geschreven. Je begrijpt nu:
1. Wat een **Class** is (de blauwdruk `CyberPet`).
2. Wat **Properties** zijn (eigenschappen zoals `this.naam`).
3. Wat **Methods** zijn (acties zoals `spelen()`).
4. Wat een **Object** is (het echte beestje, opgeslagen in `mijnHuisdier`).

*Klaar voor de bonus-uitdaging? Zorg dat de energie niet onder de 0 kan komen tijdens het spelen met een `if`-statement!*