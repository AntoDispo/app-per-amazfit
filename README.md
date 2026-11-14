# ActiveInsight · prototipo Android nativo (v0.1)

Progetto Android Studio in Kotlin/Jetpack Compose per Amazfit Active 2 tramite Health Connect.

## Come avviare
1. Aprire questa cartella in Android Studio (JDK 17, Android SDK 35).
2. Lasciare che Gradle scarichi le dipendenze (connessione Internet richiesta per la prima compilazione).
3. Eseguire su telefono Android compatibile con Health Connect.
4. In Zepp abilitare la condivisione con Health Connect; in ActiveInsight → **Dati** autorizzare e sincronizzare.

## Funzioni presenti
- Lettura Health Connect (11 tipi di record), con permessi granulari.
- Grafici cartesiani reali per passi, FC, FC a riposo, HRV, SpO2, temperatura corporea, durata sonno, calorie, distanza, allenamenti.
- Diagnostica per record presenti, assenti e permessi mancanti.
- Schede Sonno, Recupero, Sforzo e Assistente analitico locale basato su regole esplicite.
- Nessun server, account o abbonamento necessario per queste funzioni.

## Limiti espliciti
- **Non è un APK precompilato**: questo ambiente non dispone di Android SDK/Gradle per compilare e testare.
- Lo stress Zepp, la temperatura cutanea, i punteggi Readiness/PAI e altri valori proprietari non sono garantiti via Health Connect.
- La temperatura corporea di Health Connect non deve essere confusa con la temperatura cutanea del dispositivo.
- Il grafico sonno iniziale usa la durata delle sessioni, non ancora l'ipnogramma a fasi.
- Le serie sono lette su 30 giorni, senza caching persistente; il diario Street Lifting persistente, lo storico delle autovalutazioni e il vero assistente AI conversazionale non sono ancora implementati.
- La ripartizione giornaliera delle sessioni che attraversano la mezzanotte è approssimata al giorno di inizio; per un'analisi accurata serve segmentazione per giorno e deduplicazione delle sorgenti.
- Non sono stati eseguiti test di compilazione, integrazione o validazione clinica.

## Privacy
I dati sono letti localmente con il consenso dell'utente. Non è presente un backend né una trasmissione automatica. Le autorizzazioni possono essere revocate da Health Connect.
