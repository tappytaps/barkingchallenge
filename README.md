# Barkio barking challenge
## Proč to děláme

## Co je cílem
- rozpoznat štěkání v MP3
- k dispozici je ukázkový soubor, na kterém je možné algoritmus vyzkoušet. Samozřejmě je možné použít i vlastní zvuky. 
Samotné vyhodnocení proběhne na jiném, nyní "tajném" souboru.

## Pravidla
- naklonuj si toto repozitory
- napiš program v libovolném jazyce, který analyzuje audio a na výstup vypíše JSON s výsledky
- samotný dektekční program musí běžet bez internetové sítě (případná instalace / konfigurace samozřejmě sít k dispozici mít bude)
- v tvém naklonovaném repozitáři připrav sobor install.sh nebo install.bat, který spustí instalaci / konfiguraci aplikace
- v tvém naklonovaném repozitáři připrav sobor run.sh nebo run.bat, který akceptuje 1 parametr - cestu k MP3. Tento skript spustí
analýzu souboru a na standardní výstup vypíše výsledek analýzy ve formátu JSON
- tvoje řešení bude veřejné, zůstane na GitHubu a bude ho moci kdokoliv v budouocnu použít (nejen TappyTaps)

## Vyhodnocení
- v souboru bude X částí se stěkáním, za každou detekci správné části získá účastník 1 bod
- za označení špatné části 1 bod ztratí
- za správné určení délky je další bod
- tolerance určení začátku štěkání je +- 1 sekunda, tolerance určení délky jsou +-  2 vteřiny
- celkové hodnocení se udává procenty - (počet_bodů / X * 2) * 100
- pořadí určuje počet bodů, při stejném počtu bodů rozhoduje rychlost zpracování (doba běhu programu)

### Přílad
V testovací MP3 bylo celkem 10 intervalů, kdy pes štěkal. Testovaný algoritmus rozopozná správn+ celkem 9 začátky intervalů, 
u 7 z ních určí správně i délku. Zároveň označí i jeden interval, kdy štěkání není.
- celkový možný počet bodů: 20
- body za rozpoznání: 9
- body za intervaly: 7
- trestné body za špatné rozpoznání: -1

Celkové skóre je (9 + 7 - 1) / 20 * 100 = 75%

### Ceny
- nejlepší algoritmus, který získá alespoň 60% - 500 USD
- druhý nejlepší algoritmus, který získá alespoň 60% - 300 USD
- třetí nejlepší algoritmus, který získá alespoň 60% - 100 USD
#### Bonus pro přesný algoritmus
- nejlepší algoritmus, který získá alespoň 80% - dalších 300 USD
