---
title: Privacy policy di ASLI
---

# Privacy policy di ASLI

**In vigore dal:** 9 settembre 2026
**Revisione precedente:** 8 settembre 2026, per la versione 1.4.0 prima di Gmail e dei calendari
**Si riferisce a:** ASLI per Android, versione 1.4.0 e successive
**Pubblicata da:** Andrea Salvadei

ASLI è un'app di chat con un modello di intelligenza artificiale che gira
interamente sul telefono. Questa pagina dice cosa succede ai tuoi dati, e
comincia dal fatto che conta più di tutti gli altri:

**chi pubblica ASLI non riceve alcun dato dai suoi utenti, tranne quello che
sei tu a mandargli scrivendo.** Non esistono account ASLI, non c'è un server
dell'app, non viene spedita nessuna telemetria, non c'è raccolta automatica
delle segnalazioni di errore, non viene creato nessun identificatore
dell'installazione. L'unica cosa che ci arriva è la posta che ci mandi tu, e ne
parla la sezione «Se ci scrivi».

## Cosa resta sul telefono

Conversazioni, titoli, foto allegate, preferenze e il modello scaricato
**restano su questo telefono**, nella cartella riservata all'app, che le altre
app non possono leggere.

Quella riserva vale per la cartella dell'app, non per tutto il telefono. Gli
appunti di sistema sono una superficie che le app si dividono, e ogni comando
«Copia» dell'app ci scrive: il rapporto diagnostico se sei tu a copiarlo, una
risposta del modello con «Copia la risposta», il testo di una segnalazione con
«Copia il testo». Ci scrive anche Work, quando gli chiedi di copiare un testo,
ed è il solo caso in cui il testo ci arriva approvando un piano invece che
premendo «Copia». Ne parlano «Le informazioni diagnostiche», «Se ci scrivi» e
«ASLI Work».

Il database è cifrato con SQLCipher e ogni foto è cifrata con AES-256-GCM. La
chiave madre vive nel Keystore di Android e non lascia il telefono.

## La chat in incognito

*Disponibile dalla versione 1.1.0.*

C'è anche un modo di fare una domanda che non resta, per quando il telefono
può finire in mano a qualcun altro: il comando in alto a destra apre una chat
in incognito.

La chat in incognito non viene salvata da nessuna parte. Non compare
nell'elenco delle conversazioni e le foto che le alleghi non finiscono fra
quelle dell'app. Non è cancellata dopo:
non è mai scritta, e chiudendola sparisce — anche se l'app viene chiusa di
colpo dal sistema.

Due cose che quel comando non può prometterti, e preferiamo dirle. Una foto
che scegli dalla galleria **resta nella galleria**, da dove l'hai presa:
l'incognito riguarda la conversazione, non i file che avevi già. E la
tastiera del telefono impara le parole che scrivi come fa sempre, perché è
del sistema e nessuna app la può escludere per conto suo.

## ASLI Work, il comando che agisce sul telefono

*Disponibile dalla versione 1.4.0.*

Work è la seconda destinazione dell'app: scrivi in italiano cosa vuoi far fare
al telefono, e l'app te lo restituisce come un piano di passaggi. A leggere il
comando è il modello installato, che gira qui come nella chat; e quello che il
piano può cambiare decide se ti viene chiesto di approvarlo prima che parta.

**Le azioni disponibili.** Work può accendere e spegnere la torcia,
cambiare il volume multimediale, leggere lo stato del telefono, copiare un
testo negli appunti di sistema, svuotare gli appunti, e consegnare un
collegamento all'app che Android sceglie. Può anche inviare email con Gmail,
e creare eventi nei calendari del telefono, nei percorsi descritti qui sotto.
L'elenco è chiuso nel codice: un
nome che non è fra quelli previsti, o un argomento che l'app non prevede, non
diventa un passaggio, e il telefono non viene toccato. Se dal comando non esce
un piano che l'app sa eseguire, te lo dice e non fa niente. E il modello può
rifiutare il comando: allora non nasce nessun piano, e niente cambia.

**Il comando lo legge una sessione a sé.** Per preparare il piano l'app apre
una sessione del modello nuova, la usa per quella richiesta e la chiude: quella
sessione **non vede la conversazione della chat e non vede le foto**. Nel testo
che le arriva ci sono tre cose e nient'altro: l'ora locale, il nome del fuso
orario e il comando che hai scritto. Quanto pesa un'azione non lo decide il
modello: il modello propone, e quali azioni possono partire da sole e quali no
lo calcola il codice dal nome dell'azione.

**Tre azioni partono senza chiedere niente**: leggere lo stato del telefono, la
torcia e il volume. La prima è una lettura e non lascia niente; le altre due si
rimettono come stavano, e la ricevuta ti offre di rimetterle. Gli appunti e il
collegamento no: quelli chiedono che tu approvi il piano. E lo svuotamento
degli appunti chiede due volte — l'approvazione, e poi una conferma sua appena
prima di svuotare — perché non si può annullare:
quello che avevi negli appunti non torna.

**Lo stato del telefono** legge se è in carica, la memoria disponibile, lo
spazio disponibile, se c'è una connessione e di che tipo — riconoscendo anche
una VPN — la versione di Android e il modello del telefono; e il livello della
batteria, quando il telefono lo riporta. Non c'è nessun identificatore che ti
distingua: né il numero di serie, né l'identificatore che Android dà a
un'installazione, né l'IMEI. Lo spazio è quello del volume su cui vive l'app,
che su quasi tutti i telefoni è la memoria interna. Quei valori non li vedi
sullo schermo, non vengono salvati e non tornano al modello: stanno in memoria
per il tempo della ricevuta, e spariscono con lei.

**Gli appunti sono di tutto il telefono, non dell'app**, e questa è la
conseguenza da conoscere prima di dare quel comando. Un testo copiato negli
appunti di sistema lo può leggere ogni altra app, resta lì anche se disinstalli
ASLI, e «Elimina tutti i dati locali» non lo raggiunge, perché sta fuori dalla
cartella dell'app. Work negli appunti scrive e li svuota, e non li legge mai:
una lettura, nel codice, non esiste. Del testo da copiare la scheda del piano
ti mostra la prima riga, tagliata se è lunga, mentre negli appunti finisce il
testo intero: quella riga è un'anteprima, non tutto quello che stai approvando.

**ASLI consegna il collegamento, non lo apre.** Compone una richiesta di
apertura e la passa ad Android, che sceglie l'app a cui darla: può essere l'app
che apre i collegamenti, l'app del sito, o una finestra che ti fa scegliere.
ASLI non dichiara di saper aprire indirizzi web, quindi quella richiesta non
può tornare a lei. L'indirizzo lo vedi **per intero** prima di approvare, e
sono ammessi soltanto gli indirizzi `https`: un `http://` Work lo rifiuta
invece di consegnarlo. Dopo la consegna ASLI non sa più niente, nemmeno se il
collegamento è stato aperto, e di quello che fa il sito non risponde: ne parla
«Cosa esce dal telefono».

**Le email Gmail.** Colleghi un account con la schermata di autorizzazione
Google. ASLI richiede il permesso di inviare email e di conoscere l'indirizzo
del mittente, non di leggere la casella o i contatti. La bozza è preparata dal
modello locale. Puoi modificare destinatario, oggetto e testo completo prima
di premere «Conferma e invia». Solo allora ASLI invia il messaggio a Gmail via
HTTPS. Il messaggio raggiunge Google e il destinatario scelto: non il server
di chi pubblica ASLI, che non esiste. Non sono previsti allegati, CC o CCN.
L'invio non si annulla da ASLI. Un esito incerto richiede di controllare Gmail
prima di inviare ancora: l'app non riprova automaticamente.

La bozza e l'account collegato vivono nella memoria della sessione ASLI.
I token di autorizzazione restano nel componente Android e nelle cache gestite
da Google; non entrano nel modello, nel rapporto diagnostico o nell'archivio.
«Scollega Gmail» revoca l'accesso presso Google; se non riesce, lo segnala.
Puoi anche revocarlo dalla gestione delle connessioni del tuo account Google.
Scollegare o cancellare i dati ASLI non elimina le email già inviate.

**I calendari del telefono.** Work prepara un evento con titolo, inizio, fine,
luogo e descrizione modificabili. Quando chiedi l'elenco dei calendari, Android
richiede i permessi di lettura e scrittura del calendario. ASLI legge nomi e
account dei calendari scrivibili, non l'agenda. Scegli tu il calendario e
confermi i campi e il fuso mostrati prima del salvataggio. ASLI rilegge soltanto
l'evento appena inserito per verificarlo. Non aggiunge invitati o promemoria.
Un esito incerto richiede di controllare il calendario; non viene ritentato.
L'evento resta fuori dall'archivio ASLI: cancellare i dati dell'app non lo
elimina e per modificarlo o cancellarlo usi il calendario del telefono.
Il servizio dell'account scelto può sincronizzarlo secondo le sue impostazioni
e la propria informativa. ASLI non avvia una sincronizzazione e non ne verifica
l'esito: «salvato» indica la presenza nel calendario sul telefono.

**Cosa Work non fa.** Non salva il comando o il piano
su disco: vivono in memoria e spariscono. Non manda **nessuna** telemetria: nel
rapporto diagnostico non c'è un solo campo di Work, e l'esportazione
dell'archivio non ne porta niente. Non tocca foto, contatti, posizione,
microfono o SMS. Non usa un servizio di accessibilità e non guida
altre app al tuo posto.

**I permessi.** Per la torcia l'app chiede il permesso della fotocamera, con la
finestra di sistema, e **nessuna immagine viene acquisita**: accende la luce e
nient'altro. Quel permesso non nasce con Work, serviva già alla foto scattata
da dentro la chat. Work legge lo stato della rete per dirti se una connessione
c'è. I permessi calendario si chiedono soltanto quando carichi i calendari;
puoi revocarli dalle impostazioni Android dell'app.

## Cosa esce dal telefono

Le connessioni e le consegne descritte sotto dipendono dalle funzioni che
scegli di usare. La posta inviata al supporto è descritta in «Se ci scrivi».

**Il download del modello.** L'app apre una connessione a `huggingface.co`, alla
revisione fissata nel codice, e soltanto quando sei tu a chiederlo. Hugging Face
vede l'indirizzo IP del telefono, come ogni server vede chi lo contatta: quel
trattamento è suo e segue la sua informativa. Nessun messaggio e nessuna foto lo
accompagnano.

Se preferisci non scaricarlo puoi importare tu il file del modello, e non è una
scorciatoia che salta i controlli: l'app ricalcola l'impronta del file mentre lo
copia e lo rifiuta se non è, byte per byte, lo stesso che avrebbe scaricato.
Cambia solo come arrivano i byte.

**Il download dell'app, e questa pagina.** Il pacchetto di ASLI e il testo che
stai leggendo sono ospitati da GitHub, che vede l'indirizzo IP di chi scarica e
di chi legge. Anche questo trattamento è di GitHub.

**La copia di sistema di Android**, se l'hai lasciata accesa: ne parla la
sezione qui sotto.

**Il collegamento che approvi in Work.** ASLI non lo apre: compone la richiesta
di apertura e la consegna, e Android sceglie l'app che la riceve. La connessione
la apre quell'app, con le sue regole, e ASLI non sa nemmeno se il collegamento
è stato aperto.

Questa uscita non ha la forma delle altre tre, e la ragione va detta. Le altre
tre nominano il destinatario e ti rimandano alla sua informativa, perché il
destinatario è sempre lo stesso e lo conosciamo prima di te. Qui il destinatario
nasce dal comando che scrivi tu: nel codice non c'è nessuna lista di indirizzi,
quindi non c'è un nome da scriverti qui né un'informativa a cui rimandarti. Chi
pubblica ASLI non risponde di quello che fa il sito che apri; l'indirizzo lo
vedi per intero prima di approvare, e approvando sei tu a dirigere l'apertura.

**Il collegamento e gli invii Gmail.** Quando colleghi l'account ASLI comunica
con Google per l'autorizzazione e la verifica del mittente; quando confermi un
invio, invia a `gmail.googleapis.com` destinatario, oggetto e testo. Google
tratta questi dati secondo la propria [informativa](https://policies.google.com/privacy).
Il collegamento è facoltativo. ASLI non usa i dati Google per pubblicità o
addestramento di modelli: il contenuto della casella non viene letto.

Fuori da questi casi, e dalla posta che ci mandi tu, l'app non parla con
nessuno. La chat funziona in **modalità aereo**; collegare Gmail e inviare email
richiede invece una connessione.
Il traffico non cifrato è vietato dalla configurazione
dell'app, che si fida soltanto delle autorità di certificazione di sistema; e da
Work non parte nessun collegamento `http://`, perché l'app lo rifiuta invece di
consegnarlo.

## Il backup di Android, e una conseguenza da conoscere prima

Se il backup automatico di Android è acceso, conversazioni e foto entrano nella
copia verso il tuo account Google; **il modello resta fuori**, perché si può
sempre riscaricare. È una scelta dell'app, dichiarata anche nella sua pagina
«Informazioni».

Quel trasferimento è un servizio che Google presta a te, dentro il tuo account:
chi pubblica ASLI non vi accede e non ne riceve niente.

La conseguenza da conoscere prima di averne bisogno. **La chiave che le cifra**
non viaggia con il backup, perché resta nel Keystore di questo telefono. Un
ripristino su un altro telefono, o dopo una disinstallazione,
**non può rileggerle**, e l'app riparte da zero dichiarandolo.

## Le foto

L'app non chiede il permesso di leggere la tua galleria: usa il selettore di
sistema e riceve soltanto i file che scegli, uno per uno. Una foto scattata da
dentro l'app non finisce in galleria.

La foto che alleghi viene copiata nell'area dell'app e ridimensionata:
cancellarla dalla conversazione non tocca l'originale che hai in galleria, e
cancellare l'originale non la toglie dalla conversazione.

## Le informazioni diagnostiche

La schermata Profilo mostra un rapporto con la versione dell'app, il sistema,
lo stato di ogni modello del catalogo con la sua revisione, i conteggi di
conversazioni, messaggi e foto, lo spazio occupato dal modello, dalle immagini
e dal database, lo spazio libero e il numero di versione dello schema del
database. Esce da qui soltanto se sei tu a copiarlo,
o se le alleghi a una segnalazione con «Scrivici»: in entrambi i casi il testo
che parte è esattamente quello che vedi, riga per riga, senza niente di
nascosto. Le informazioni diagnostiche **non contengono testi** dei messaggi,
titoli né percorsi delle foto. Dove poi le incolli, o se scegli di allegarle, è
una scelta tua.

**L'app scrive anche dei segnalibri tecnici nel registro del telefono**, quello
di sistema: nomi di eventi, tempi, conteggi di token, l'esito di una
generazione. Servono a capire un guasto, non partono verso nessuno e nessun'altra
app li può leggere — per vederli bisogna avere il telefono in mano, con il
debug USB acceso e un computer collegato. Non contengono quello che scrivi:
verificato il 26 luglio 2026 su una registrazione di 12.142 righe presa durante
una conversazione intera, cercandovi frammenti dei messaggi. Un identificatore
casuale distingue una sessione dall'altra dentro quel registro: nasce a ogni
avvio dell'app, non viene salvato da nessuna parte e non ti segue fra un avvio e
il successivo.

## Se ci scrivi

Dentro l'app ci sono due modi per farci arrivare qualcosa: «Segnala la
risposta», sotto ogni risposta del modello, e «Scrivici», nella pagina
«Informazioni».

**ASLI non spedisce niente da sé.** Prepara il messaggio, te lo mostra per
intero prima che parta, e lo consegna alla tua app di posta: a premere invio
**sei tu a spedirlo**, dalla tua casella. Se cambi idea davanti al messaggio
già scritto, non parte niente.

Lo stesso standard vale in Work per il collegamento, che vedi per intero prima
di approvare. La seconda metà però è diversa, e va detta: la posta la spedisci
tu premendo invio, mentre il collegamento lo consegna ASLI appena hai approvato
il piano. In Work il tuo atto è l'approvazione, non un secondo tocco.

**Parte solo quello che hai scelto.** Segnalando una risposta partono quella
risposta, la nota che scrivi se la compili, la versione dell'app e il nome e
la revisione del modello; la domanda che l'ha prodotta parte soltanto se
spunti la casella, perché è testo tuo. Scrivendoci per un problema parte quello che scrivi, insieme alla
versione dell'app — non il nome del modello — e le informazioni diagnostiche
solo se le alleghi: quelle non contengono testi dei messaggi, titoli né
percorsi delle foto. In nessuno dei due casi partono foto, il resto della
conversazione, o un identificatore del telefono o dell'installazione.

**Cosa ne facciamo.** Riceviamo il tuo indirizzo email — perché scrivi dalla
tua casella — e quello che hai allegato. Ce ne serviamo per capire il
problema, correggerlo e risponderti, e per niente altro: nessuna lista,
nessun invio. La base giuridica è il nostro legittimo interesse a ricevere
segnalazioni sulla sicurezza e sul funzionamento dell'app (art. 6, par. 1,
lett. f del GDPR).

**Per quanto.** Una segnalazione resta nella nostra casella finché serve a
trattarla, e comunque non oltre dodici mesi.

## Cancellare

Tre livelli, tutti nelle tue mani.

- **Una conversazione.** Eliminandola spariscono anche le foto dei suoi
  messaggi, nella stessa operazione.
- **«Elimina tutti i dati locali»**, nel Profilo: rimuove conversazioni,
  messaggi, foto, preferenze e il modello scaricato. **Non è reversibile.**
  Non arriva agli appunti di sistema, che sono del telefono e non dell'app: ne
  parla «ASLI Work».
- **Disinstallare l'app.** Android porta via i dati privati dell'app e con essi
  la chiave che li cifra. È definitivo: nemmeno un backup ripristinato dopo
  riesce a rileggere quello che c'era.

## Per quanto tempo

Chi pubblica ASLI non conserva niente di quello che fai nell'app, perché non
lo riceve: i tuoi dati restano sul telefono finché sei tu a tenerceli.
L'unica eccezione è la posta che ci mandi tu, e dura non oltre dodici mesi.

## I tuoi diritti

Accesso, rettifica, cancellazione, limitazione, opposizione e portabilità sono
diritti che si esercitano nei confronti di chi tratta i tuoi dati. Per ASLI non
c'è nessuno a cui rivolgerli, perché i tuoi dati non sono mai usciti dalle tue
mani: li eserciti da solo, e l'app ti dà gli attrezzi — l'esportazione
dell'archivio ti consegna le conversazioni in un file, la cancellazione è
descritta qui sopra.

Su due cose quegli attrezzi non arrivano: quello che un comando di Work ha
copiato negli appunti di sistema, che sono del telefono e non dell'app, e un
collegamento che hai approvato e che un'altra app ha aperto. Gli appunti li
svuoti tu, e Work ha un comando che lo fa; per quello che ha visto il sito che
si è aperto, quei diritti si esercitano verso chi pubblica quel sito, non verso
chi pubblica ASLI.

Se ci scrivi, cambia: da quel momento abbiamo il tuo indirizzo e quello che
ci hai mandato, e quei diritti li eserciti verso di noi, all'indirizzo qui
sotto.

## A chi si rivolge l'app

ASLI è pensata per un pubblico adulto, dai 18 anni in su, e non è rivolta a
minori.

Non c'è una verifica dell'età, e la ragione è la stessa che regge tutto il resto
di questa pagina: l'app non ti chiede dati e non ne raccoglie, quindi non ha
modo di sapere chi la sta usando. Una casella da spuntare non verificherebbe
niente, e ti chiederebbe una dichiarazione che non potremmo né controllare né
conservare.

Il modello rifiuta le richieste peggiori: dietro c'è un prompt di sistema, non
l'applicazione della politica sugli usi vietati di Gemma nella sua interezza.
Gira comunque sul telefono, e nessun filtro locale può garantire che ogni
risposta sia adatta a un minore. Per questo l'app lo dice anche al suo interno,
nell'avviso che si apre toccando la banda sopra la barra di invio.

## Modifiche a questa pagina

Ogni modifica passa da un commit e porta una data. Quella in vigore è la pagina
che stai leggendo; le precedenti restano nella storia del repository.

L'ultima è del 9 settembre 2026: aggiunge a Work le email inviate con Gmail
dopo la tua conferma e gli eventi scritti nei calendari del telefono. Quella
dell'8 settembre 2026 aveva aggiunto «ASLI Work, il comando che agisce sul
telefono», il quarto caso di «Cosa esce dal telefono», e gli appunti di
sistema fra le superfici che l'app tocca. La revisione prima, del 25 agosto
2026, descriveva la versione 1.3.1, dove Work non esisteva.

## Come contattarci

Per una segnalazione, un problema o una domanda su questa pagina:
asli.supporto@gmail.com. È l'indirizzo che l'app stessa usa quando tocchi
«Segnala la risposta» o «Scrivici».

## Cosa questa pagina non copre

- **Una versione modificata di ASLI.** Qui è descritta l'app pubblicata da noi:
  una build costruita da altri non è più questa app, e questa pagina non dice
  niente su di lei.
