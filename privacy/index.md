---
title: Privacy policy di ASLI
---

# Privacy policy di ASLI

**In vigore dal:** 18 agosto 2026
**Si riferisce a:** ASLI per Android, versione 1.1.0 e successive
**Pubblicata da:** Andrea Salvadei

ASLI è un'app di chat con un modello di intelligenza artificiale che gira
interamente sul telefono. Questa pagina dice cosa succede ai tuoi dati, e
comincia dal fatto che conta più di tutti gli altri:

**chi pubblica ASLI non riceve alcun dato dai suoi utenti, tranne quello che
sei tu a mandargli scrivendo.** Non esistono account, non c'è un server
dell'app, non viene spedita nessuna telemetria, non c'è raccolta automatica
delle segnalazioni di errore, non viene creato nessun identificatore
dell'installazione. L'unica cosa che ci arriva è la posta che ci mandi tu, e ne
parla la sezione «Se ci scrivi».

## Cosa resta sul telefono

Conversazioni, titoli, foto allegate, preferenze e il modello scaricato
**restano su questo telefono**, nella cartella riservata all'app, che le altre
app non possono leggere.

Il database è cifrato con SQLCipher e ogni foto è cifrata con AES-256-GCM. La
chiave madre vive nel Keystore di Android e non lascia il telefono.

## La chat in incognito

*Disponibile dalla versione 1.1.0.*

C'è anche un modo di fare una domanda che non resta, per quando il telefono
può finire in mano a qualcun altro: il comando in alto a destra apre una chat
in incognito.

La chat in incognito non viene salvata da nessuna parte. Non compare
nell'elenco delle conversazioni e le foto che le allegi non finiscono fra
quelle dell'app. Non è cancellata dopo:
non è mai scritta, e chiudendola sparisce — anche se l'app viene chiusa di
colpo dal sistema.

Due cose che quel comando non può prometterti, e preferiamo dirle. Una foto
che scegli dalla galleria **resta nella galleria**, da dove l'hai presa:
l'incognito riguarda la conversazione, non i file che avevi già. E la
tastiera del telefono impara le parole che scrivi come fa sempre, perché è
del sistema e nessuna app la può escludere per conto suo.

## Cosa esce dal telefono

Tre cose, e nessuna riguarda quello che scrivi. Ce n'è una quarta che invece
lo riguarda, e succede soltanto se sei tu a volerlo: la trovi in «Se ci
scrivi».

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

Fuori da questi tre casi l'app non parla con nessuno. La chat funziona identica
in **modalità aereo**, ed è misurato: durante una conversazione completa i
contatori di rete del sistema per ASLI non si muovono di un byte. Il traffico
non cifrato è vietato dalla configurazione dell'app, che si fida soltanto delle
autorità di certificazione di sistema.

## Il backup di Android, e una conseguenza da conoscere prima

Se il backup automatico di Android è acceso, conversazioni e foto entrano nella
copia verso il tuo account Google; **il modello resta fuori**, perché si può
sempre riscaricare. È una scelta dell'app, dichiarata anche nella sua pagina
«Informazioni».

Quel trasferimento è un servizio che Google presta a te, dentro il tuo account:
chi pubblica ASLI non vi accede e non ne riceve niente.

La conseguenza da conoscere prima di averne bisogno: **La chiave che le cifra**
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

Le Impostazioni mostrano un rapporto con la versione dell'app, il sistema, lo
stato di ogni modello del catalogo con la sua revisione, i conteggi di
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
- **«Elimina tutti i dati locali»**, nelle Impostazioni: rimuove conversazioni,
  messaggi, foto, preferenze e il modello scaricato. **Non è reversibile.**
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

## Come contattarci

Per una segnalazione, un problema o una domanda su questa pagina:
asli.app@gmail.com. È l'indirizzo che l'app stessa usa quando tocchi
«Segnala la risposta» o «Scrivici».

## Cosa questa pagina non copre

- **Una versione modificata di ASLI.** Qui è descritta l'app pubblicata da noi:
  una build costruita da altri non è più questa app, e questa pagina non dice
  niente su di lei.
