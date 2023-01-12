# Istruzioni

## Modificare il path della cartella di lavoro nei file:
 *elaborazione.py<br />
 *moduli_temporale.py<br />
 *filtri_fissi.py<br />
 *filtri.py<br />
 *rumore.py<br />
 
## Eseguire gli script nel seguente ordine:
 *elaborazione.py<br />
 *temporale.py<br />
 *filtri_fissi.py<br />
 *filtri.py<br />
 *rumore.py<br />
 
## Breve descrizione dei file:
 *elaborazione.py: elabora i dati e li rende pronti per l'analisi.<br />
 *temporale.py: confronta temporalmente i dati e ne visualizza lo spettro, senza però filtrarli in alcun modo.<br />
 *filtri_fissi.py: confronta lo spettro dei dati e li ricostruisce con due differenti filtri sulla frequenza.<br />
 *filtri.py: confronta lo spettro dei dati dando la possibilità di scegliere se utilizzare un filtro sulla frequenza basato solo su questa o anche sull'ampiezza dei coefficienti di Fourier. Inoltre rispetto al file precedente permette di modificare il valore dei filtri in maniera (relativamente) più agevole.<br />
 *rumore.py: analizza lo spettro delle differenze tra i dati filtrati e non; esegue il fit con una funzione del tipo frequenza^(-beta).<br />
 
## Note:
 *Alcuni risultati o informazioni sui dati del plot sono stampate a schermo.<br />
 *Ogni script [nome] da eseguire necessita del file moduli_[nome] per funzionare.<br />
 *All'inizio di alcuni file sono presenti parametri per variare leggermente il comportamento degli script.<br />
 *Per velocizzare o eseguire solo in parte il file elaborazione.py sono presenti punti di salvataggio e caricamento di file da de-commentare.<br />
 *Gli unici file che vanno necessariamente salvati sono salvati automaticamente nella stessa cartella path specificata precedentemente; ciò viene fatto alla fine del file elaborazione.py e può essere disabilitato attraverso la variabile booleana all'inizio dello stesso.<br />
  *Lo script test.py esegue un semplice confronto sul tempo necessario a due differenti funzioni per eseguire la media giornaliera svolta nel file elaborazione.<br />


## Possibili miglioramenti:
  *Evitare ripetizioni di codice salvando sotto forma di file i risultati ottenuti, in particolar modo per i file filtri e rumore. <br />
  *Riscrivere in maniera più efficente la funzione 'funzione_stati2' in 'moduli_elaborazione.py utilizzando le funzioni 'selezione_stato' e 'dataframe_filtrato' dello stesso file; tuttavia il guadagno in termini temporali non dovrebbe essere particolarmente importante. <br />
  *Trovare un modo più corretto per sostituire i dati mancanti (stimati attraverso la media del dato precedente e successivo) o fisicamente non accettabili (posti uguali a zero)
