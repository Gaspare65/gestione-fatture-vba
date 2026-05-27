# Istruzioni di Setup - Gestione Fatture VBA

## ⚠️ IMPORTANTE: Costruzione Manuale del Progetto

Poiché non è possibile caricare direttamente file binari .xlsm, seguire questi passaggi per assemblare l'applicazione:

## Step 1: Creazione Struttura Base Excel

1. Apri **Excel**
2. Crea un nuovo file e salvalo con il nome `GestioneFatture.xlsm` (importante: formato macro-enabled)
3. Crea questi 5 fogli (eliminando eventuali fogli vuoti):
   - `Impostazioni`
   - `Pazienti`
   - `Fatture`
   - `DettagliFatture`
   - `ModelloFattura`

## Step 2: Struttura dei Dati

### Foglio "Impostazioni"
Crea questa struttura nelle prime righe:
```
A1: Impostazioni Studio
A2: Nome Dottore          B2: [vuoto - da compilare]
A3: Indirizzo             B3: [vuoto - da compilare]
A4: Telefono              B4: [vuoto - da compilare]
A5: Email                 B5: [vuoto - da compilare]
A6: Partita IVA           B6: [vuoto - da compilare]
A7: Codice Fiscale        B7: [vuoto - da compilare]
A8: Aliquota IVA Default  B8: 22
A10: Ultimo Numero        B10: 0
```

### Foglio "Pazienti"
Intestazioni nella riga 1:
```
A1: ID
B1: Nome
C1: Cognome
D1: Indirizzo
E1: Città
F1: CAP
G1: Codice Fiscale
H1: Partita IVA
```

### Foglio "Fatture"
Intestazioni nella riga 1:
```
A1: ID
B1: Numero
C1: Data
D1: IDPaziente
E1: Stato
F1: Esenta
G1: AliquotaIVA
```

### Foglio "DettagliFatture"
Intestazioni nella riga 1:
```
A1: IDFattura
B1: Descrizione
C1: Quantità
D1: PrezzoUnitario
E1: Totale
```

### Foglio "ModelloFattura"
Struttura professionale (vedi template sotto)

## Step 3: Importare il Codice VBA

1. Premi **Alt + F11** per aprire l'editor VBA
2. Nel menu **Progetto**, clicca con tasto destro
3. Seleziona **Inserisci > Modulo**
4. Crea questi moduli:
   - `ModImpostazioni`
   - `ModPazienti`
   - `ModFatture`
   - `ModUtility`

5. Copia il codice da ogni file `.bas` in questo repository nei moduli corrispondenti

6. Crea le UserForm:
   - Clicca destro > **Inserisci > UserForm**
   - Crea: `FormImpostazioni`, `FormPazienti`, `FormFatture`
   - Copia il codice corrispondente

## Step 4: Creare il Menu Principale

1. Crea un foglio chiamato `Menu`
2. Aggiungi bottoni con queste macro:
   - Pulsante "Impostazioni" → `AperturaNModImpostazioni`
   - Pulsante "Pazienti" → `AperturaModuloPazienti`
   - Pulsante "Fatture" → `AperturaModuloFatture`

## Step 5: Salva e Testa

1. Salva il file come `.xlsm`
2. Chiudi e riapri per verificare che le macro funzionino
3. Abilita le macro se richiesto

---

## 📁 File Necessari

I file di codice sono disponibili in questo repository:
- `ModImpostazioni.bas`
- `ModPazienti.bas`
- `ModFatture.bas`
- `ModUtility.bas`
- `FormImpostazioni.frm`
- `FormPazienti.frm`
- `FormFatture.frm`

Copia il contenuto di ogni file e incollalo nei moduli/form corrispondenti in Excel.

---

**Tempo stimato**: 30-45 minuti

Se hai domande durante il setup, contattami!
