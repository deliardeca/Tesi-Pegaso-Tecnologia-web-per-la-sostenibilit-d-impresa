# Report Professionale: Sviluppo di una Pagina Web per i Report di Sostenibilità di Ferrari

## Introduzione

Il presente documento descrive il processo di sviluppo di una pagina web dedicata al download dei report di sostenibilità di **Ferrari S.p.A.**, un'azienda leader nel settore automobilistico di lusso. Questo progetto è stato realizzato per rispondere alla crescente importanza della trasparenza aziendale in materia di sostenibilità ambientale, sociale ed economica (ESG). La pagina web mira a fornire agli stakeholder un accesso facile e intuitivo ai documenti che testimoniano l'impegno di Ferrari verso un futuro più sostenibile. Offre la possibilità di scaricare sia il report completo in formato PDF, sia riassunti testuali delle sezioni chiave.

---

## 1. Analisi del Contesto Aziendale: Ferrari S.p.A.

Fondata nel 1947 da Enzo Ferrari, Ferrari è un simbolo globale di eccellenza, innovazione e performance. Operando nel **settore secondario**, l'azienda non solo produce automobili sportive di lusso, ma è anche un'icona nel mondo delle corse con la Scuderia Ferrari. In un settore ad alta intensità di risorse e impatto ambientale, la sostenibilità è diventata un pilastro strategico per Ferrari, che si impegna a bilanciare la sua eredità di prestazioni con la responsabilità ambientale e sociale.

---

## 2. Analisi Approfondita del Report di Sostenibilità 2022

Il **Report di Sostenibilità 2022** di Ferrari delinea una strategia chiara e ambiziosa. Di seguito un'analisi più dettagliata dei punti salienti:

- **Decarbonizzazione e Elettrificazione**:
  - Ferrari si è impegnata a raggiungere la **neutralità carbonica entro il 2030**. 
  - Il piano prevede un'accelerazione nell'elettrificazione della gamma, con il lancio del primo modello completamente elettrico previsto per il 2025. L'obiettivo è che il 60% della gamma sia ibrida o elettrica entro il 2026.

- **Efficienza delle Risorse e Economia Circolare**:
  - Nel 2022, Ferrari ha raggiunto un tasso di **recupero dei rifiuti del 97%**.
  - Sono state implementate tecnologie innovative per ridurre il consumo di acqua ed energia nei processi produttivi, con un focus sull'utilizzo di fonti rinnovabili.

- **Catena di Fornitura Sostenibile**:
  - Ferrari promuove pratiche sostenibili lungo tutta la sua catena di fornitura, richiedendo ai suoi partner di aderire a standard etici e ambientali rigorosi.

- **Innovazione e Benessere dei Dipendenti**:
  - L'azienda investe costantemente in ricerca e sviluppo per creare materiali più leggeri e sostenibili.
  - Il benessere dei dipendenti è una priorità, con programmi di formazione continua, welfare aziendale e iniziative per promuovere la diversità e l'inclusione.

---

## 3. Descrizione del Codice e Scelte di Progettazione

La pagina web è stata sviluppata utilizzando **HTML5** e **CSS3**, seguendo le migliori pratiche per garantire accessibilità, reattività e manutenibilità.

### HTML (`index.html`)

Il codice HTML è strutturato semanticamente per migliorare l'indicizzazione da parte dei motori di ricerca e l'accessibilità. Ogni sezione è commentata per spiegare il suo scopo.

```html
<!DOCTYPE html>
<!-- Specifica la lingua del documento per una migliore accessibilità -->
<html lang="it">
<head>
    <!-- Imposta la codifica dei caratteri a UTF-8 per supportare tutti i caratteri speciali -->
    <meta charset="UTF-8">
    <!-- Garantisce che la pagina sia responsive e si adatti a diverse dimensioni di schermo -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Titolo della pagina visualizzato nella scheda del browser -->
    <title>Ferrari - Report di Sostenibilità</title>
    <!-- Collega il foglio di stile CSS esterno per la formattazione della pagina -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Sezione dell'intestazione della pagina -->
    <header>
        <!-- Logo dell'azienda, con un testo alternativo per l'accessibilità -->
        <img src="https://upload.wikimedia.org/wikipedia/it/5/59/Logo_della_Scuderia_Ferrari_%28vecchio%29.svg" alt="Logo Ferrari" id="logo">
        <!-- Titolo principale della pagina -->
        <h1>Report di Sostenibilità</h1>
    </header>

    <!-- Contenuto principale della pagina -->
    <main>
        <!-- Sezione dedicata alla lista dei report disponibili -->
        <section class="report-list">
            <!-- Titolo della sezione -->
            <h2>Scarica i nostri report</h2>
            <!-- Contenitore per un singolo report -->
            <div class="report-item">
                <!-- Titolo del report -->
                <h3>Report di Sostenibilità 2022</h3>
                <!-- Breve descrizione del report -->
                <p>Leggi il nostro ultimo report per scoprire i nostri progressi verso un futuro più sostenibile.</p>
                <!-- Link per il download del report completo in formato PDF -->
                <a href="reports/sustainability_report_2022.pdf" class="btn" download>Scarica Report Completo (PDF)</a>

                <!-- Sezione per il download dei dettagli -->
                <div class="details-download">
                    <h4>Scarica dettagli per categoria (.txt):</h4>
                    <a href="reports/decarbonizzazione.txt" class="btn btn-secondary" download>Decarbonizzazione</a>
                    <a href="reports/economia_circolare.txt" class="btn btn-secondary" download>Economia Circolare</a>
                    <a href="reports/innovazione_benessere.txt" class="btn btn-secondary" download>Innovazione e Benessere</a>
                </div>
            </div>
        </section>
    </main>

    <!-- Piè di pagina del sito -->
    <footer>
        <!-- Informazioni sul copyright -->
        <p>&copy; 2025 Ferrari S.p.A. - Tutti i diritti riservati.</p>
        <p>Sviluppato da Vincenzo De Carluccio</p>
    </footer>
</body>
</html>
```

### CSS (`style.css`)

Il CSS è stato progettato per riflettere l'identità visiva di Ferrari, utilizzando una palette di colori iconica (nero, rosso e bianco) e un layout pulito e professionale. I commenti nel codice spiegano ogni regola e scelta stilistica.

```css
/* Stili generali del corpo della pagina */
body {
    font-family: Arial, sans-serif; /* Imposta un font pulito e leggibile */
    margin: 0;
    padding: 0;
    background-color: #f4f4f4; /* Colore di sfondo leggero */
    color: #333; /* Colore del testo principale */
}

/* Stili dell'intestazione */
header {
    background-color: #000; /* Sfondo nero per l'intestazione */
    color: #fff; /* Testo bianco */
    padding: 20px;
    text-align: center;
    border-bottom: 4px solid #D40000; /* Bordo rosso Ferrari */
}

#logo {
    width: 150px; /* Dimensione del logo */
    margin-bottom: 10px;
}

header h1 {
    margin: 0;
    font-size: 2.5em; /* Dimensione del titolo principale */
}

/* Stili della sezione principale */
main {
    padding: 20px;
    max-width: 800px; /* Larghezza massima per una migliore leggibilità */
    margin: 0 auto; /* Centra il contenuto */
}

.report-list h2 {
    text-align: center;
    color: #D40000; /* Colore rosso Ferrari per i titoli di sezione */
    font-size: 2em;
    margin-bottom: 20px;
}

.report-item {
    background-color: #fff; /* Sfondo bianco per gli elementi del report */
    border: 1px solid #ddd; /* Bordo leggero */
    padding: 20px;
    margin-bottom: 20px;
    border-radius: 5px; /* Angoli arrotondati */
    box-shadow: 0 2px 4px rgba(0,0,0,0.1); /* Ombra per un effetto di profondità */
}

.report-item h3 {
    margin-top: 0;
    font-size: 1.5em;
}

/* Stili per il pulsante di download */
.btn {
    display: inline-block;
    background-color: #D40000; /* Colore di sfondo rosso Ferrari */
    color: #fff; /* Testo bianco */
    padding: 10px 20px;
    text-decoration: none; /* Rimuove la sottolineatura del link */
    border-radius: 5px; /* Angoli arrotondati */
    font-weight: bold;
    transition: background-color 0.3s; /* Transizione per l'effetto hover */
}

.btn:hover {
    background-color: #A00000; /* Colore più scuro al passaggio del mouse */
}

/* Stili per la sezione dei download di dettaglio */
.details-download {
    margin-top: 20px; /* Aggiunge spazio sopra la sezione dei dettagli */
    padding-top: 15px;
    border-top: 1px solid #eee; /* Linea di separazione */
}

.details-download h4 {
    margin-bottom: 10px;
}

/* Stili per i pulsanti secondari */
.btn-secondary {
    background-color: #6c757d; /* Colore grigio per i pulsanti secondari */
    margin-right: 10px; /* Spazio tra i pulsanti */
}

.btn-secondary:hover {
    background-color: #5a6268; /* Colore più scuro al passaggio del mouse */
}

/* Stili del piè di pagina */
footer {
    background-color: #000; /* Sfondo nero per il piè di pagina */
    color: #fff; /* Testo bianco */
    text-align: center;
    padding: 10px;
    position: fixed; /* Fissa il footer in fondo alla pagina */
    width: 100%;
    bottom: 0;
}
```

---

## 4. Processo di Sviluppo e Riflessioni Finali

Il processo di sviluppo ha seguito una metodologia strutturata:

1.  **Fase di Analisi**: Comprensione approfondita dei requisiti del progetto e scelta di un'azienda pertinente.
2.  **Progettazione**: Definizione della struttura della pagina e dello stile visivo, in linea con il brand Ferrari.
3.  **Sviluppo**: Scrittura del codice HTML e CSS, con un approccio iterativo per risolvere problemi come il download del logo.
4.  **Documentazione**: Creazione di questo report per documentare ogni aspetto del progetto.

Questo progetto non solo ha permesso di applicare competenze di programmazione web a un caso d'uso realistico, ma ha anche offerto l'opportunità di approfondire l'importanza della **Responsabilità Sociale d'Impresa (RSI)**. L'analisi del report di sostenibilità di Ferrari ha dimostrato come un'azienda di lusso possa integrare con successo pratiche sostenibili nel suo modello di business, comunicando in modo trasparente i propri sforzi e risultati.
