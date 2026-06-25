# 📃 Messaggi in Musica 🎼

Benvenuto in **Messaggi in Musica**, un innovativo progetto di cifratura che unisce l'informatica alla musica. Questo software consente di cifrare e decifrare messaggi testuali utilizzando un sistema polialfabetico ispirato al classico [Cifrario di Vigenère](https://it.wikipedia.org/wiki/Cifrario_di_Vigen%C3%A8re), traducendo le lettere non in semplici caratteri, ma in vere e proprie **note e strutture musicali**.

Mentre sul web esistono innumerevoli tool per la cifratura tradizionale, **Messaggi in Musica** colma un vuoto, offrendo un sistema per trasformare messaggi segreti in spartiti musicali digitali riproducibili.

---

## 💻 Le Due Versioni del Programma

Il progetto si compone di due varianti distinte, capaci di soddisfare sia l'approccio puramente matematico/sperimentale sia quello più melodico e tonale:

1. **🎶 Note Message (Approccio Meccanico)**
   * Impiega **singole note musicali** per la cifratura.
   * Produce sonorità particolari, dal tono similare a quello delle avanguardie e dello sperimentalismo musicale.
2. **🎼 Music Message (Approccio Tonale - Minuetto)**
   * Adopera **intere battute in 3/8**, ispirandosi all'andamento di un minuetto classico.
   * Si ispira al gioco musicale *Musikalisches Würfelspiel* (edizione del 1793) per garantire un esito decisamente più "tonale" e piacevole all'ascolto.

---

## 🛠️ Tecnologie e Requisiti

I programmi sono stati sviluppati interamente in **Python 3** utilizzando esclusivamente librerie standard, garantendo massima portabilità senza necessità di installare moduli di terze parti:

> 📥 **Software Consigliato per la riproduzione:**
> Per visualizzare e ascoltare lo spartito generato (`musica.xml`), si raccomanda caldamente l'uso del programma gratuito e open-source di scrittura musicale **[MuseScore](https://musescore.org/it)**.

---

## 📂 Installazione e Avvio

Per utilizzare il software, segui attentamente questi passi:

1. Scarica la cartella completa di questo progetto sul tuo computer (puoi salvarla in qualsiasi percorso).
2. ⚠️ **IMPORTANTE:** **Non trasferire alcun file** (inclusi gli **ESEGUIBILI**) al di fuori della loro cartella originale. Il corretto funzionamento del programma dipende dalla struttura relativa dei file all'interno della directory.
3. Avvia l'eseguibile relativo alla versione che desideri utilizzare (`Note Message` o `Music Message`).

---

## 📖 Istruzioni per l'Uso

L'interfaccia grafica è identica per entrambi i programmi ed è estremamente intuitiva. Si divide in due modalità operative:

### 🟢 Fase di Codifica (Cifratura)
1. Inserisci nel **campo superiore** la tua **Chiave** di cifratura (sono ammessi *solo caratteri alfanumerici*).
2. Inserisci nel **campo inferiore** il **Testo del messaggio** che desideri camuffare in musica.
3. Clicca sul pulsante verde **'Codifica'**.
4. Il programma genererà, all'interno della cartella principale, un file denominato `musica.xml`. Questo file può essere aperto immediatamente con **MuseScore** per essere visionato e riprodotto.

🚨 **ATTENZIONE:** Se intendi creare più file musicali, **ricordati di rinominare il file musicale vecchio** prima di avviare una nuova codifica. In caso contrario, il nuovo file sovrascriverà quello precedente, causandone la perdita irreversibile.

### 🔵🔴 Fase di Decodifica (Decifratura)
1. Inserisci nel **campo superiore** la **Chiave** corretta (la stessa usata per la codifica, *solo caratteri alfanumerici*).
2. Clicca sul pulsante azzurro **'Carica musica'** per sfogliare i tuoi file e selezionare il file `.xml` della musica che vuoi decodificare.
3. Clicca sul pulsante rosso **'Decodifica'**: il testo del messaggio originale apparirà magicamente a schermo.

<p align="center">
  <img src="assets/interfaccia.png" alt="Interfaccia" width="400">
</p>

---

## 📜 Approfondimento Culturale: Il *Musikalisches Würfelspiel*

Per la versione **Music Message**, l'ispirazione non è puramente matematica, ma affonda le radici in un documento del XVIII secolo.

Il **[Musikalisches Würfelspiel](https://vmirror.imslp.org/files/imglnks/usimg/7/7c/IMSLP798374-PMLP1260062-attr_mozart_g.270.g.-2.-_Anleitung_Walzer_oder_Schleifer_mit_zwei_Wu-rfeln_zu_componiren.pdf)** (*"Gioco per comporre musica con i dadi, senza intendersi di musica o di composizione"*) è stato un celebre espediente per generare musica in modo semicasuale. Pubblicato in anni diversi e da vari editori, la sua paternità è stata storicamente attribuita a vari compositori, tra cui *Johann Philipp Kirnberger*, *Carl Philipp Emanuel Bach* e, soprattutto, *Wolfgang Amadeus Mozart* (sebbene la responsabilità di quest’ultimo sia fortemente messa in discussione).

### Struttura Musicale Implementata nel Programma
Analizzando la parte musicale del gioco originale, si nota che molte battute si ripetono assumendo una precisa funzione strutturale. Per mantenere una coerenza musicale ed evitare un caos tonale, l'algoritmo di **Music Message** adotta le seguenti regole:

* **Matrice di Selezione:** Invece di singole note, vengono associate **intere battute** selezionate direttamente dal gioco musicale (per un totale di **85 battute** scelte).
* **Distribuzione delle Battute:**
  * **10** battute destinate esclusivamente come *battute iniziali*.
  * **36** battute dedicate alla *prima parte del minuetto*.
  * **36** battute dedicate alla *seconda parte*.
  * **2** battute di ritornello (una per la prima parte del minuetto e una per la seconda).
  * **1** ultima battuta finale
* **Vincoli di Cifratura:** Per ragioni di coerenza formale ed estetica musicale, il sistema **esclude dalla cifratura** la battuta iniziale, la battuta finale e le due battute centrali a ridosso del ritornello. In questo modo la struttura del Minuetto classico rimane intatta e riconoscibile all'orecchio.

---

*Progetto sviluppato con passione da Lorenzo Cignoni, studente di Ingegneria Informatica presso il Politecnico di Milano, per coniugare l'arte della crittografia al fascino della musica classica.* Il materiale necessario per il progetto e i due eseguibili sono disponibili in questa repository.
