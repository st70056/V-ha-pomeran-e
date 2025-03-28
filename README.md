# Váha pomeranče  

## 1. Shrnutí nápadu  
Projekt **Váha pomeranče** je zaměřen na odhad hmotnosti oloupaného pomeranče na základě vstupní hmotnosti a fotografie. Systém využívá strojové učení k analýze dat a poskytuje přesnou predikci zbývající hmotnosti po odstranění slupky.  

## 2. Pozadí projektu  

### Problém  
Při sledování kalorického příjmu je důležité znát hmotnost jedlé části pomeranče. Přesné zvážení je možné až po oloupání, což není ideální, pokud si člověk chce předem naplánovat stravu. Tento projekt umožňuje odhadnout hmotnost dužiny ještě před oloupáním, a tím zjednodušit evidenci příjmu živin.  

### Význam  
Tato metoda je užitečná zejména pro ty, kteří si pečlivě sledují nutriční hodnoty svého jídla nebo sestavují dietní plány. Přináší praktické využití jak pro jednotlivce, tak pro výživové poradce.  

### Osobní motivace  
Projekt vychází z vlastní zkušenosti – potřeby zjistit hmotnost dužiny pomeranče, aniž by bylo nutné ho předem loupat. Umělá inteligence nabízí efektivní a rychlé řešení tohoto problému.  

### Důležitost tématu  
Využití AI pro predikci hmotnosti potravin přispívá k přesnějšímu plánování stravy a usnadňuje sledování kalorického příjmu. Tento projekt ukazuje, jak lze strojové učení aplikovat v běžném životě pro jednodušší správu výživy.  

## 3. Data a AI techniky  

### Zdroj dat  

Projekt je závislý na vlastních datech vytvořených manuálním měřením hmotnosti pomerančů ve dvou stavech. Každý vzorek obsahuje:  
- Fotografii celého pomeranče položeného na váze (včetně slupky)  
- Fotografii stejného pomeranče po oloupání, kdy je na váze pouze jedlá dužina  

Tyto snímky slouží jako vizuální vstup pro model. Kromě fotografií je u každého vzorku zaznamenána i přesná hmotnost před a po oloupání, což umožňuje výpočet poměru dužiny a trénování predikčního modelu.  

### Ukázky vstupních snímků  

**Pomeranč před oloupáním:**  
<img src="https://github.com/user-attachments/assets/13cc0337-2704-47c2-ba59-34b568067db2" alt="pomeranc_pred" width="300"/>

**Pomeranč po oloupání:**  
<img src="https://github.com/user-attachments/assets/cdc34e81-fd8f-41e8-a0d8-7578866265fe" alt="pomeranc_po" width="300"/>

### Ukázková vstupní data  

Tabulka zobrazuje reálná měření hmotnosti pomerančů před a po oloupání:  

| Hmotnost před oloupáním (g) | Hmotnost dužiny (g) | Poměr dužiny (%) |
|-----------------------------|---------------------|------------------|
| 319                         | 246                 | 77,1 %           |
| 298                         | 246                 | 82,6 %           |
| 293                         | 233                 | 79,5 %           |
| 280                         | 213                 | 76,1 %           |
| 270                         | 218                 | 80,7 %           |
| 263                         | 162                 | 61,6 %           |
| 259                         | 190                 | 73,4 %           |
| 282                         | 203                 | 72,0 %           |
| 248                         | 187                 | 75,4 %           |
| 246                         | 163                 | 66,3 %           |
| 230                         | 153                 | 66,5 %           |
| 228                         | 155                 | 68,0 %           |
| 228                         | 173                 | 75,9 %           |
| 227                         | 172                 | 75,8 %           |
| 225                         | 178                 | 79,1 %           |
| 220                         | 166                 | 75,5 %           |
| 215                         | 133                 | 61,9 %           |
| 186                         | 127                 | 68,3 %           |
| 179                         | 124                 | 69,3 %           |
| 176                         | 120                 | 68,2 %           |

### Vhodné AI techniky  

Pro řešení tohoto problému se nabízí kombinace následujících technik umělé inteligence:

- **Počítačové vidění (Computer Vision)**  
  Pomocí zpracování obrazu lze analyzovat tvar, velikost a barvu pomeranče na vstupní fotografii. To může pomoci modelu lépe pochopit vizuální vlastnosti ovoce, které mohou souviset s poměrem dužiny.

- **Regresní modely (Linear Regression, Decision Trees)**  
  Slouží k predikci hmotnosti dužiny na základě číselných vstupů, jako je celková hmotnost. Tyto modely jsou jednoduché, ale efektivní pro první fázi vývoje.

- **Neuronové sítě (Deep Learning)**  
  Pokročilejší přístup, který by umožnil analyzovat fotografie a další proměnné zároveň. Například použití konvolučních neuronových sítí (CNN) by mohlo zvýšit přesnost odhadu díky hlubší analýze vizuálních vstupů.

V počáteční fázi projektu může být ideální začít jednodušším regresním modelem a následně experimentovat s pokročilejšími technikami pro zlepšení přesnosti.

### Kontext a cíloví uživatelé  

Systém bude využíván především jednotlivci, kteří si plánují stravu a sledují svůj kalorický příjem. Uplatnění najde například mezi sportovci, lidmi držícími redukční dietu, diabetiky nebo každým, kdo si vede záznamy o příjmu živin.  

Využití je zamýšleno v běžném domácím prostředí, kde uživatel jednoduše zváží pomeranč, pořídí fotografii, a systém mu na základě vstupu odhadne čistou hmotnost dužiny. Aplikace může být součástí mobilní aplikace pro výživu, fitness nebo dietní plánování.
