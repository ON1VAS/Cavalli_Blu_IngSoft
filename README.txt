QUESTO PROGRAMMA HA COME PREREQUISITO XAMPP:

Step per il funzionamento del programma


1) Avviare xampp ed abilitare Apache e MySQL

2) Aprire localhost/phpmyadmin ed importare il database 'cavallibludb.sql'

3) Incollare tutti i file all'interno della cartella principale di xampp/htdocs

4) Per avviare la prima pagina del sito digitare 'localhost/index.html'

5) Da qui, si può decidere se accedere, inserire delle parole chiavi o registrarsi:
	**PER INSERIRE LE PAROLE CHIAVI, ANDARE AL PUNTO 6.1.2**

5.1) **ACCESSO**
	Se si vuole provare l'accesso con account già esistenti, si può usare questi ultimi, forniti di email e password:
	'emailprovata@gmail.com', 'susy2023' (utente)
	'emailnonesiste@hotmail.it', 'forzanapoli' (utente)
	'adminpocopalese@tiscali.it', 'bravagiovannabrava22' (admin)
	'utentemisterioso@gmail.com', 'cavalliblu23' (utente)
	'utentesicuro@hotmail.it', 'forzabari' (utente)

5.2) **REGISTRAZIONE**
	Se si clicca sul tasto di registrazione, si rimanda ad una finestra dove bisogna mettere email e password
	Dopo averli inseriti, c'è un timer che riporterà alla pagina di login.

6) Dopo aver fatto il login, c'è un controllo per verificare se l'utente è amministratore (6.2) o meno (6.1)

6.1) **LOGIN UTENTE**
	L'utente ha tre scelte: fare una recensione, fare il logout o inserire le parole chiave nel sistema.
	Se fa il logout, lo riporta alla pagina del login
	**PER INSERIRE LE PAROLE CHIAVI, ANDARE AL PUNTO 6.1.2**

6.1.1) **RECENSIONE**
	L'utente può scegliere se lasciare una recensione, vedere le proprie recensioni oppure eliminarle
	Se sceglie di lasciare una recensione, deve obbligatoriamente mettere il sito a cui si riferisce, la recensione effettiva e il voto (positivo o negativo), allora potrà inviarla
	Se sceglie di vedere le proprie recensioni, allora il sito fornirà l'elenco di tutte le recensioni che ha lasciato l'utente (ID - sito - recensione - voto), con un tasto sotto per tornare alla finestra precedente.
		Se non ci sono recensioni, il sito dirà che quell'utente non ha lasciato ancora recensioni
	Se sceglie di cancellare una recensione, il sito fornirà una finestra sulla quale scrivere l'ID della recensione da eliminare, se è tutto corretto la si elimina.
		Se l'ID non è corretto, il sito dirà che non esiste e fornirà un tasto per tornare indietro
		Se l'ID è di una recensione scritta da un altro utente, il sito darà errore e fornirà un tasto per tornare indietro.

6.1.2) **USO DELLO SCANNER**
	L'utilizzatore può scegliere di inserire delle parole chiavi e restituirà delle notizie.
	Esse verranno inanzitutto verificate dal programma, se tutte le news contengono parole chiave che già sappiamo essere finte allora restituirà il messaggio "Sono presenti parole chiave che portano a fake news. Visualizzazione interrotta."
	Se superano questo check, allora le notizie verranno visualizzate all'utente, compreso di titolo, sottotitolo, immagine e link, arricchite di statistiche in basso:
	- Presenza nella Whitelist/Blacklist
	- Indice di affidabilità secondo 3 scaglioni:
		Indice >60% -> Il sito è affidabile secondo le recensioni degli utenti
		Indice >50% ma <=60% -> Il sito è parzialmente affidabile
		Indice <50% -> Il sito non è affidabile, potrebbe trattarsi di satira oppure di fake news

6.2) **LOGIN AMMINISTATORE**
	L'amministratore ha molteplici scelte: può decidere se visualizzare, aggiungere siti o eliminare siti dalla blacklist e dalla whitelist, 
	decidere se visualizzare tutte le recensioni degli utenti o cancellarne una, uso dello scanner, segnalare alla polizia postale oppure fare il logout.
	**PER INSERIRE LE PAROLE CHIAVI, ANDARE AL PUNTO 6.1.2**
	
6.2.1) **BLACKLIST**
	Se si clicca sul tasto "Visualizza Blacklist Globale" verranno trovati tutti i siti da escludere dalla ricerca e che sono insicuri o dannosi, e il proprio id.
		Se per caso non ci sono siti nella blacklist, il sito dirà che non sono stati inseriti siti nella blacklist
	Se si clicca sul tasto "Aggiungi Blacklist Globale" il sito chiederà di inserire un sito alla blacklist, se è tutto corretto lo si aggiunge al database
		Se il sito è già presente nel database, allora il sito dirà che è già presente
	Se si clicca sul tasto "Rimuovi Blacklist Globale" il sito chiederà di rimuovere un sito alla blacklist, se è tutto corretto lo si rimuove dal database 
		Se il sito non è presente nel database, allora il sito dirà che non esiste il sito

6.2.2) **WHITELIST**
	Se si clicca sul tasto "Visualizza Whitelist Globale" verranno trovati tutti i siti che sono sicuri e da includere nella ricerca, e il proprio id.
		Se per caso non ci sono siti nella whitelist, il sito dirà che non sono stati inseriti siti nella whitelist
	Se si clicca sul tasto "Aggiungi Whitelist Globale" il sito chiederà di inserire un sito alla whitelist, se è tutto corretto lo si aggiunge al database
		Se il sito è già presente nel database, allora il sito dirà che è già presente
	Se si clicca sul tasto "Rimuovi Whitelist Globale" il sito chiederà di rimuovere un sito alla whitelist, se è tutto corretto lo si rimuove dal database 
		Se il sito non è presente nel database, allora il sito dirà che non esiste il sito
		
6.2.3) **MODERARE RECENSIONI UTENTI**
	L'amministratore ha per se un metodo per moderare le recensioni dei vari utenti, sia visualizzando tutte le recensioni mai lasciate dagli utenti (ordinati per il sito)
	oppure può cancellare una recensione (attraverso l'id)

6.2.4) **SEGNALAZIONE**
	L'amministratore ha un modo per segnalare un sito fraudolento.
	Se le recensioni sono abbastanza negative, l'amministratore può scegliere di cliccare il tasto che riporta alla pagina per i reati telematici, e da li fare la segnalazione
