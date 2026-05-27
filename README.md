# Gestione Fatture VBA - Excel

Applicazione VBA completa per la gestione professionale di fatture in Excel, sviluppata per studi medici (nutrizionisti, medici, ecc.).

## 📋 Caratteristiche Principali

### Archivi
- **Archivio Pazienti**: Gestione completa dei dati dei pazienti
- **Archivio Fatture**: Gestione fatture con numerazione automatica

### Funzionalità CRUD
Per ogni archivio (Pazienti e Fatture):
- ✅ **Inserisci**: Aggiungi nuovi record
- ✅ **Modifica**: Aggiorna dati esistenti
- ✅ **Visualizza**: Vedi i dettagli
- ✅ **Cancella**: Rimuovi record
- ✅ **Annulla**: Annulla fatture (senza eliminarle)

### Sistema di Numerazione Fatture
- Numerazione automatica formato: **1/2026, 2/2026, ecc.**
- Possibilità di **resettare** la numerazione
- Possibilità di **partire da un numero personalizzato**

### Gestione Pazienti
- Nome, Cognome, Indirizzo, Città, CAP
- Codice Fiscale e Partita IVA
- Selezione paziente da archivio durante inserimento fattura
- Possibilità di inserire nuovo paziente al volo

### Modello Fattura Professionale
- Intestazione personalizzabile con dati dello studio
- Dati paziente automaticamente compilati
- Numero fattura e data
- Multiple righe di descrizione prestazioni
- Quantità e prezzo unitario per cada descrizione
- **Calcoli automatici**:
  - **IVA**: Personalizzabile (22%, 10%, 5%, ecc.) o esente
  - **Bollo**: Automatico quando importo supera €77,47
  - **Ritenuta d'Acconto**: 4% calcolata automaticamente
  - **Totale Netto**: Calcolato automaticamente

### Foglio Impostazioni
Personalizza i dati del tuo studio:
- Nome Dottore
- Indirizzo Studio
- Telefono e Email
- Partita IVA
- Codice Fiscale
- Gestione numerazione fatture

### Esportazione PDF
- Esporta le fatture come PDF professinali
- Pronto per l'invio ai clienti/pazienti

## 🚀 Come Usare

### 1. Apertura Applicazione
1. Apri il file `GestioneFatture.xlsm` in Excel
2. Abilita le macro quando richiesto
3. Vedrai il menu principale

### 2. Configurazione Iniziale
1. Clicca su **"Impostazioni"**
2. Compila i dati del tuo studio:
   - Nome, Indirizzo, Telefono, Email
   - Partita IVA, Codice Fiscale
3. Salva le impostazioni

### 3. Gestione Pazienti
1. Clicca su **"Pazienti"**
2. Scegli:
   - **Nuovo**: Inserisci un nuovo paziente
   - **Modifica**: Aggiorna dati paziente
   - **Visualizza**: Vedi i dati
   - **Cancella**: Rimuovi paziente
3. Compila i campi e salva

### 4. Creazione Fatture
1. Clicca su **"Fatture"**
2. Scegli **"Nuova Fattura"**
3. Seleziona il paziente dall'elenco (o inserisci uno nuovo)
4. Scegli se la fattura è **esente IVA** o meno
5. Se non esente, seleziona **l'aliquota IVA** (22%, 10%, 5%, ecc.)
6. Inserisci le descrizioni delle prestazioni:
   - Descrizione
   - Quantità
   - Prezzo Unitario
   - **Premi Invio o Tab per la prossima riga**
   - **Lascia il campo descrizione vuoto per terminare**
7. Salva la fattura
8. Il numero fattura viene generato automaticamente (es. 1/2026)

### 5. Visualizzazione e Esportazione
1. Clicca su **"Visualizza Fattura"**
2. La fattura si apre nel modello professionale
3. Clicca **"Esporta PDF"** per scaricare il file PDF

### 6. Modifiche e Annulli
- **Modifica Fattura**: Aggiorna i dati (numero e data rimangono fissi)
- **Annulla Fattura**: Marca la fattura come "Annullata" senza eliminarla

## 📊 Struttura Dati

### Fogli Excel
1. **Impostazioni**: Dati dello studio e parametri
2. **Pazienti**: Archivio pazienti (ID, Nome, Cognome, ecc.)
3. **Fatture**: Archivio fatture (ID, Numero, Data, Paziente, Stato, ecc.)
4. **DettagliFatture**: Righe di dettaglio (Descrizione, Quantità, Prezzo)
5. **ModelloFattura**: Template professionale per visualizzazione

### Moduli VBA
- `ModImpostazioni`: Gestione impostazioni e numerazione
- `ModPazienti`: CRUD pazienti
- `ModFatture`: CRUD fatture e calcoli
- `ModUtility`: Funzioni di utilità (PDF, visualizzazione, ecc.)

## ⚙️ Configurazione Avanzata

### Reset Numerazione
1. Apri **"Impostazioni"**
2. Clicca **"Reset Numerazione"**
3. Inserisci il numero da cui ricominciare
4. La prossima fattura avrà quel numero

### Modifica Aliquota IVA
Le aliquote IVA vengono scelte al momento dell'inserimento della fattura. Puoi usare qualsiasi percentuale (22%, 10%, 5%, ecc.)

### Bollo
Il bollo di €2,00 viene calcolato automaticamente quando l'importo totale (lordo + IVA) supera €77,47

### Ritenuta d'Acconto
La ritenuta del 4% viene calcolata automaticamente sul totale lordo

## 💡 Suggerimenti

1. **Backup regolari**: Salva regolarmente il file in una cartella di backup
2. **Non eliminare colonne**: La struttura è ottimizzata, non aggiungere/eliminare colonne
3. **Nomi unici pazienti**: Cerca di usare nomi/cognomi unici per evitare confusione
4. **Verifica dati**: Prima di esportare PDF, verifica i dati visualizzati nel modello

## 🐛 Troubleshooting

### Le macro non si eseguono
- Verifica che Excel sia impostato per eseguire macro
- File > Opzioni > Centro Trust > Impostazioni Centro trust > Impostazioni Macro

### Errore "Paziente non trovato"
- Assicurati di aver inserito correttamente il paziente prima di creare la fattura
- Usa il bottone "Nuovo Paziente" durante l'inserimento fattura se necessario

### PDF non si esporta
- Verifica che sia installato un lettore PDF
- Controlla che la cartella di salvataggio abbia i permessi di scrittura

## 📝 Note Legali

Questa applicazione è fornita come è. Verificare sempre la conformità alle normative fiscali vigenti per la propria giurisdizione.

Per fatture, bollo e ritenuta d'acconto, consultare un commercialista.

---

**Versione**: 1.0  
**Sviluppato**: 2026  
**Licenza**: Uso personale
