# Dashboard Finanziamenti Auto

Dashboard statica (HTML/CSS/JS, nessuna build necessaria) con offerte reali di finanziamento auto raccolte dal web, organizzate in 5 categorie:

- **Auto Nuove**
- **Auto Usate / Km0**
- **Neopatentati**
- **Anticipo Zero**
- **Maxirata Finale Zero**

## Come usarla

Apri `index.html` in un browser, oppure servi la cartella con un server statico qualsiasi (es. `python3 -m http.server`) e vai su `http://localhost:8000`.

La pagina permette di:
- filtrare le offerte per una o più categorie (i filtri si combinano in AND)
- cercare per marca/modello
- ordinare per rata, anticipo o marca
- vedere per ogni offerta: prezzo, anticipo, rata mensile, numero rate, eventuale maxirata finale, TAN/TAEG, note e link alla fonte originale

## Dati

I dati si trovano in [`data/offerte.json`](data/offerte.json) e sono incorporati anche direttamente in `index.html` come fallback (così la pagina funziona anche aperta come semplice file, senza server). Per aggiornare le offerte, modifica entrambi i file mantenendo la stessa struttura.

Ogni offerta include marca, modello, tag di categoria, cifre del finanziamento (dove disponibili) e la fonte pubblica da cui è stata raccolta.

**Attenzione:** i dati sono stati raccolti da siti di case automobilistiche, concessionarie e testate di settore tramite ricerca web e sono aggiornati indicativamente ad agosto 2026. Le promozioni cambiano mensilmente e variano per allestimento, provincia e concessionario: verificare sempre l'offerta reale (documento IEBCC/SECCI) prima di firmare un contratto di finanziamento.
