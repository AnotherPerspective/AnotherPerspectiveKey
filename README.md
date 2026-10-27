# AnotherPerspectiveKey — powered by CorridorKey

Scontorno green e blue screen con l'intelligenza artificiale dentro **DaVinci Resolve**, **Adobe
Premiere Pro** e **Adobe After Effects**, basato su [CorridorKey 2.0](https://github.com/nikopueringer/CorridorKey2.0)
di **Corridor Digital**. Gratuito, gira sul tuo computer, nessun abbonamento.

Di [Another Perspective Pictures](https://www.anotherperspectivepictures.com). *English below.*

## Scarica

**[Ultima versione](https://github.com/AnotherPerspective/AnotherPerspectiveKey/releases/latest)** — 1.1.1 beta

| Sistema | File |
|---|---|
| **Windows** (consigliato) | [AnotherPerspectiveKey-1.1.1-beta-windows-setup.exe](https://github.com/AnotherPerspective/AnotherPerspectiveKey/releases/download/v1.1.1-beta/AnotherPerspectiveKey-1.1.1-beta-windows-setup.exe) |
| Windows, con gli script | [AnotherPerspectiveKey-1.1.1-beta-windows.zip](https://github.com/AnotherPerspective/AnotherPerspectiveKey/releases/download/v1.1.1-beta/AnotherPerspectiveKey-1.1.1-beta-windows.zip) |
| Linux (solo DaVinci Resolve) | [AnotherPerspectiveKey-1.1.1-beta-linux.tar.gz](https://github.com/AnotherPerspective/AnotherPerspectiveKey/releases/download/v1.1.1-beta/AnotherPerspectiveKey-1.1.1-beta-linux.tar.gz) |
| Mac | non supportato: CorridorKey 2.0 richiede una scheda NVIDIA |

Il file è piccolo: il resto (CorridorKey, PyTorch, i modelli, circa 10 GB) lo scarica l'installazione
dalle fonti ufficiali.

## Cosa fa

1. Selezioni le clip girate su green o blue screen: in timeline in Resolve e Premiere, i livelli in After Effects.
2. Apri il plugin e premi **Scontorna**. Con la finestra aperta puoi aggiungere altre clip, anche da
   altre timeline: è pensato per lavorare su decine di clip in coda.
3. CorridorKey scontorna solo il pezzo usato (più qualche fotogramma di margine) e il risultato torna
   da solo al suo posto:
   - **Resolve**: la matte agganciata alla clip originale (pagina Color › Add Matte), più a scelta la
     matte in bianco e nero e la clip scontornata sulla traccia sopra;
   - **Premiere Pro**: la clip scontornata sopra e la matte come Track Matte Key sull'originale;
   - **After Effects**: il livello scontornato sopra e la matte come track matte Alpha.

L'originale non viene mai modificato.

## Cosa serve

- Windows 10 22H2 o Windows 11 (Linux solo per Resolve)
- Scheda **NVIDIA RTX** (serie 30 o più recente, 8 GB o più; 16-24 GB per il 4K) con driver **570** o più recente
- DaVinci Resolve 21, Premiere Pro 2022 o After Effects 2023 (o versioni più recenti)
- Circa 25 GB liberi e una connessione a internet per l'installazione

Su una RTX 4090 ci vogliono circa 4 secondi per fotogramma 4K.

## Installare su Windows

1. Chiudi DaVinci Resolve, Premiere Pro e After Effects.
2. Apri **AnotherPerspectiveKey-1.1.1-beta-windows-setup.exe**. Il Setup non è firmato con un certificato
   a pagamento, quindi Windows mostra "Windows ha protetto il PC": *Ulteriori informazioni* › *Esegui comunque*.
3. Accetta la licenza di CorridorKey, scegli i programmi (quelli trovati sul PC sono già accesi) e premi
   **Installa**. Ci vogliono 20-30 minuti.
4. Riapri i programmi:
   - **Resolve**: Workspace › Scripts › AnotherPerspectiveKey › Key selected clips
   - **Premiere Pro / After Effects**: Finestra › Estensioni › AnotherPerspectiveKey powered by CorridorKey

Per disinstallare: Impostazioni › App › AnotherPerspectiveKey powered by CorridorKey.

## Colore

CorridorKey è addestrato su immagini Rec.709. In **Resolve** il girato Log e RAW viene convertito con la
gestione colore del progetto o con una LUT. In **Premiere e After Effects** per il Log serve una LUT di
conversione (.cube); i RAW si scontornano da Resolve.

## È una beta

Funziona, ma è ancora in prova. Non ancora provati: progetti Resolve con RCM/ACES, Resolve gratuito,
After Effects a 8 o 16 bit, timeline 29,97 drop-frame in Resolve. Clip con cambi di velocità, compound e
multicam vengono segnalate e saltate.

Se qualcosa non va, apri una segnalazione in [Issues](https://github.com/AnotherPerspective/AnotherPerspectiveKey/issues)
con uno screenshot e, se l'installazione si ferma, il file `%LOCALAPPDATA%\AnotherKey\setup.log`.

## Licenza

AnotherPerspectiveKey è distribuito con la stessa **Corridor Key Licence 2.0** di CorridorKey
(CC BY-NC-SA 4.0 con termini aggiuntivi, vedi [LICENSE](LICENSE) e [NOTICE](NOTICE)):

- puoi usarlo anche per lavori commerciali, e ciò che produci è tuo;
- non può essere venduto e ogni versione modificata deve restare gratuita e mantenere il nome CorridorKey;
- le aziende con fatturato annuo oltre 20 milioni di dollari devono acquistare una licenza per persona
  su [corridorkey.com](https://corridorkey.com).

CorridorKey è di Corridor Digital; modelli e strumenti di terze parti hanno le loro licenze
([THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)). AnotherPerspectiveKey non è affiliato a Corridor
Digital, Blackmagic Design o Adobe.

---

## English

AI green and blue screen keying inside **DaVinci Resolve**, **Adobe Premiere Pro** and **Adobe After
Effects**, built on Corridor Digital's [CorridorKey 2.0](https://github.com/nikopueringer/CorridorKey2.0).
Free, runs locally, no subscription.

**Download:** [latest release](https://github.com/AnotherPerspective/AnotherPerspectiveKey/releases/latest) —
Windows Setup (recommended), Windows zip, or Linux (DaVinci Resolve only). macOS is not supported:
CorridorKey 2.0 needs an NVIDIA GPU. The download is small; installation fetches CorridorKey, PyTorch
and the models (about 10 GB) from their official sources.

**Needs:** Windows 10 22H2 / 11, an NVIDIA RTX GPU (30 series or newer, 8 GB+) with driver 570+, and
DaVinci Resolve 21, Premiere Pro 2022+ or After Effects 2023+. About 25 GB free.

**Install:** close the programs, run the Setup (Windows warns about an unknown publisher: *More info* ›
*Run anyway*), accept the CorridorKey licence, pick the programs, press Install (20-30 minutes). Then:
Resolve › Workspace › Scripts › AnotherPerspectiveKey › Key selected clips; Premiere / After Effects ›
Window › Extensions › AnotherPerspectiveKey powered by CorridorKey.

**What it does:** select green/blue screen clips, press Key. Only the used range is keyed; the matte
comes back attached to the original clip in Resolve, as a Track Matte Key in Premiere and as an Alpha
track matte in After Effects, with the keyed clip above. The original is never modified.

**Beta:** not tested yet with RCM/ACES Resolve projects, Resolve free, 8/16 bpc After Effects projects.
Report problems in [Issues](https://github.com/AnotherPerspective/AnotherPerspectiveKey/issues).

**License:** Corridor Key Licence 2.0 (CC BY-NC-SA 4.0 + additional terms). Free for commercial work;
it may not be sold; derivatives must stay free and keep the CorridorKey name; organisations above
US$20M revenue need per-seat licences from corridorkey.com. Not affiliated with Corridor Digital,
Blackmagic Design or Adobe.
