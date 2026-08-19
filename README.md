# VestaMaintenance - contratto dei dati e vocabolario dei rilevamenti

Questo repository contiene **soltanto artefatti generati**: lo schema del file
JSON che VestaMaintenance produce a ogni esecuzione, e una pagina per ognuno dei
436 identificativi di rilevamento.

**Non contiene il prodotto ne' il suo codice sorgente.**

## Contratto

- [`schema/run-1.1.json`](schema/run-1.1.json)

La versione si incrementa **solo** per modifiche non retrocompatibili: un
aggregatore la usa per rifiutare cio' che non sa interpretare.

## Rilevamenti

- [Elenco completo](https://thedarkholeyt.github.io/vesta-schema/findings/index.html)
- [`findings.json`](findings.json) - indice macchina-leggibile

Un identificativo pubblicato **non si rinomina e non si riusa mai per un altro
significato**: e' cio' che permette di confrontare i dati di oggi con quelli
dell'anno scorso, e di sommare trecento computer in un numero solo.

Ogni identificativo ha anche un numero di evento stabile, con cui compare nel
Registro eventi di Windows sotto il log `VestaMaintenance`.

## Verificare un file senza avere il prodotto

Lo script `Test-RunFile.ps1`, distribuito con il prodotto, non importa nessun
modulo e non richiede l'installazione: si copia accanto allo schema e risponde
se un file e' un run valido.

## Licenza

Documentazione e indice: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Il prodotto e il suo codice non rientrano in questa licenza.

---

Generato da `build/New-SchemaSite.ps1`. Le modifiche fatte a mano qui si
perdono alla prossima generazione.