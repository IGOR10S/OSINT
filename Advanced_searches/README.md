

# OSINT - Ricerca avanzata su browser

Di seguito verranno mostrate una serie di ricerche (input) da effettuare sul browser per cercare informazioni specifiche sul web.

## Ricerca di una frase esatta

- Se cerchi notizie specifiche puoi usare le virgolette per cercare una frase esatta. Questa ricerca ti darà risultati che contengono esattamente queste parole e frasi.

    ```bash
    "Phishing" "Attacco ASL"
    ```

## Ricerca con esclusioni

- Se vuoi escludere certi termini che potrebbero creare confusione (come notizie non rilevanti o altre località), puoi utilizzare il segno meno (`-`). In questo modo, escludi risultati che contengono le parole legate ai termini specificati con il segno meno (`-`).

    ```bash
    "Phishing" "Attacco ASL" -dati -sanitari
    ```

## Ricerca per sito specifico

- Se vuoi limitare la ricerca a un certo tipo di siti (ad esempio giornali o siti governativi), puoi usare l'operatore `site:`. Questo ti mostrerà solo i risultati dal sito specificato.

    ```bash
    "Phishing" site:wikipedia.org

    appure

    "Phishing" site:it.wikipedia.org
    ```

## Ricerca su social media

- Anche su Google puoi cercare informazioni provenienti da piattaforme di social media, usando operatori come `site:` per focalizzarti su contenuti di piattaforme come **Twitter** o **Reddit**.

    ```bash
    "CyberSecurity" site:twitter.com
    ```

## Ricerca di file PDF o documenti ufficiali

- Se cerchi documenti ufficiali, come verbali o atti giudiziari, puoi usare l'operatore `filetype:` per trovare documenti di tipo PDF o DOC. Questa ricerca ti mostrerà documenti che contengono le parole chiave.

    ```bash
    "Phishing" filetype:pdf
    ```

## Ricerca per data

- Se quello che stai cercando è recente o è accaduto in un periodo specifico, puoi limitare i risultati a una determinata data utilizzando lo strumento di ricerca temporale di Google. Dopo aver fatto la ricerca, vai su **Strumenti** e seleziona **Intervallo di date** o scegli tra le opzioni disponibili come "*Ultimo mese*" o "*Ultimo anno*".

## Ricerca per intervallo di date

- Puoi usare l'operatore `..` per cercare informazioni che riguardano un determinato intervallo di date. Questo è utile se vuoi cercare notizie, eventi o trend di un certo periodo.

    ```bash
    "Phishing" "ASL" 2020..2023
    ```

## Ricerca con sinonimi

- Utilizza il simbolo tilde (`~`) prima di una parola per cercare risultati che includono sinonimi o concetti correlati.

    ```bash
    ~attacco "Phishing" Dati
    ```

## Ricerca con più alternative

- Puoi usare l'operatore `OR` per includere più alternative nella ricerca. Devi scrivere `OR` (**in maiuscolo**) tra le parole o frasi.

    ```bash
    "Attacco Phishing" OR "Attacco Ransomware"
    ```

## Ricerca nel titolo di una pagina

- Usa l'operatore `intitle:` per cercare una parola o una frase che appaia nel titolo delle pagine web.

    ```bash
    intitle:"Attacco Phishing"
    ```

## Ricerca in URL

- Puoi usare l'operatore `inurl:` per trovare pagine che contengano una parola specifica nell'URL. Utile quando cerchi articoli o documenti che potrebbero avere una struttura di URL prevedibile.

    ```bash
    inurl:phishing "Security"
    ```

## Ricerca di termini collegati a una parola

- Puoi usare l'operatore `*` come jolly per cercare combinazioni di parole collegate. Questo è utile se non ricordi esattamente una frase o se cerchi varianti della stessa ricerca.

    ```bash
    "Security * Web"
    ```

## Ricerca geografica (in un'area specifica)

- Usa l'operatore `location:` per cercare notizie relative a una specifica area geografica. Questo è utile per restringere la ricerca a eventi locali.

    ```bash
    "Phishing Attack" location:"America"
    ```

## Ricerca verificando il collegamento tra parole

- Se vuoi cercare pagine che contengano entrambe le parole, ma non necessariamente vicine, puoi usare l'operatore `AND`.

    ```bash
    phishing AND "Security"
    ```

## Ricerca basata su link

- Se vuoi cercare pagine che fanno riferimento a un determinato sito o URL, puoi usare l'operatore `link:`.

    ```bash
    link:nist.gov

    oppure

    link:csrc.nist.gov
    ```

## Ricerca di una parola vicina a un'altra

- Se vuoi cercare due parole che appaiono vicine l'una all'altra, puoi usare l'operatore `AROUND(X)` per specificare la distanza massima (X) tra le due parole.

    ```bash
    "Sicurezza" AROUND(5) Ransomware
    ```

<br>

.

.

.

<br>

> <h2> !! Attendi l'aggiunta di altri esempi di ricerca avanzata !! </h2>

<br>

.

.

.

<br>

## Combina operatori per ricerche più complesse

- Puoi combinare più operatori per una ricerca molto specifica. Facendo la seguente ricerca avanzata, ci si aspetta di trovare documenti ufficiali in **PDF** relativi al **phishing** o ad un **attacco** phishing all'**ASL**, escludendo riferimenti ai **dati sanitari**, presenti sul sito web **hosting.aruba.it**, pubblicati tra il **2020** e il **2023**.

    ```bash
    "Phishing" "Attacco ASL" -dati -sanitari site:hosting.aruba.it filetype:pdf 2020..2023
    ```

> **NOTA:** Si prega di notare che questi sono semplici esempi a scopo dimostrativo, perciò non è sicuro che tale ricerca restituisca dei risultati, o almeno quelli che ci si aspetta di trovare.
