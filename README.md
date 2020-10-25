# Domácí úkol 2 - Les se zvířátky

### Jak spustit

1. Stáhnout si obsah repozitáře
1. Přejit v konzoli do adresáře staženého repozitáře
1. Spustit příkaz **npm install**

### Scripty

Dev server - spustí se vývojový server a live reloading

```
npm run start
```

Development build - webpack zkompiluje celý náš projekt a vytvoří složku dist

```
npm run dev
```

Production build - webpack zkompiluje projekt a optimalizuje kód pro vystavení na produkční server

```
npm run build
```

### Zadání

Úkol částečně navazuje na předešlý v tom smyslu, že budeme dělat nějaký výpis. Tentokrát to bude ale s malou změnou. Začneme používat třídy a moduly. První krok je vytvořit třídu, která bude reprezentovat zvíře. Tato třída bude do konstruktoru brát:
1. Jméno druhu zvířete
1. Čím se živí
1. Stupeň ohrožení
1. Celkovou populaci
Pro stupně ohrožení si naimportuj objekt ze souboru conservationStatus využij ho. Pokud by vám vadily anglické názvy, klidně si je přepište do češtiny.

Dále bude třída pro zvíře obsahovat metodu, která vytvoří html element li podle předlohy, kterou najdeš v index.html. Tento vytvořený element metoda bude vracet. Tříde může mít libovolný počet pomocných metod.

Dalším krokem pro vás bude vytvořit třídu reprezentující les. Tato třída bude do konstruktoru brát pole již existujících zvířat, nebo nic (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters).

Dále tato třída bude obsahovat dvě metody:
1. Pro přidání zvířete do pole k ostatním zvířatům
1. Metodu pro vytvoření seznamu zvířat, která vytvoří ul element a vygeneruje do něj li elementy všem zvířatům, která třída zná. Metoda vrací vytvořený ul element
Třída může opět obsahovat libovolný počet pomocných metod

Soubor index.js bude sloužit pouze jako entry point aplikace. To znamená, že v něm nebude žádná logika. Pouze vytvoření instance lesa, případně zvířat a vložení vygenerovaného seznamu do DOMu.

Jak má výsledná struktura vypadat najdeš v index.html včetně všech CSS tříd, aby to i nějak vypadalo :)

BONUS #1 pro šprtky: Obdobně vytvoř třídu a seznam pro reprezentaci stromů v lese. Styly jsou pro to připravené. Budeš muset vytvořit novou třídu pro strom a upravit/rozšířit třídu lesa. HTML strukturu to bude mít velice podobnou jen všechny "animal" přepíšeš na "tree" (případně nakoukni do CSS). Strom by měl znát název druhu, zda je jehličnatý nebo listnatý a zda je ohrožený (plus co tě napadne přidat, fantazii se meze nekladou).

BONUS #2 pro mega šprtky: Rozšiř třídu zvířete tak, že bude možné vyplnit popis, váha a výška… případně další informace o zvířeti. Tyto informace zobraz v detailu zvířete, který se ukáže po kliknutí na řádek v seznamu. Když na řádek klikneš znovu tak se detail zavře. Když kliknu na jiné zvíře tak se detail přepíše novýmy informacemi. U tohoto úkolu si budeš muset dopsat vlastní CSS