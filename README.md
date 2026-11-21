# ROJ — drone synth (navdih: organski 8-glasni drone synthi)

Brskalniški synth v eni datoteki (`index.html`, brez odvisnosti).

## Zvok
- **8 glasov v 4 parih** — vsak glas drži pad (dotik, tipke `A S D F G H J K` ali MIDI nota).
- Na par: **Ton** (±18 poltonov na glas), **Mod** (FM globina), **Ostro** (sinus → kvadrat/fold),
  **Ovojnica** (hiter ↔ počasen nastop/izzvenevanje), **Drži** (glas ostane tiho prižgan kot drone).
- **Vir modulacije** na par (gumb "Mod:"): *LFO*, *Sosed* (naslednji par — križna FM) ali *Sam* (feedback FM).
- **Hiper LFO**: dva LFO-ja, seštevanje ali ring modulacija.
- **Delay**: dve liniji z nasičenim feedbackom, modulacijo časa in barvo.
- **Distorzija** + limiter na izhodu.

## MIDI kontroler (Akai APC mini / APC40 / karkoli)
Privzeta mapa (APC mini mk1/mk2):

| Kontrola | Funkcija |
|---|---|
| Spodnja vrsta padov (note 0–7) | glasovi 1–8 (pad zasveti) |
| Note 36–43 | glasovi 1–8 (večina pad kontrolerjev) |
| Drsniki 1–4 (CC 48–51) | Ton glasov 1, 3, 5, 7 |
| Drsniki 5–8 (CC 52–55) | Mod para 1–4 |
| Master drsnik (CC 56) | Glasnost |

**MIDI learn**: klikni *MIDI learn* → tapni gumb ali pad → premakni kontrolo na kontrolerju. Mapa se shrani v brskalnik.

## iPhone + kontroler
- APC (mini/40) je *class-compliant* USB MIDI, iPhone ga prepozna prek USB-C (iPhone 15+) ali
  adapterja *Lightning → USB 3 Camera Adapter* (z napajanjem). APC40 potrebuje svoje napajanje.
- **Safari na iOS ne podpira Web MIDI**, zato na iPhonu v Safariju igraš z dotikom.
  Za kontroler na iPhonu odpri stran v brskalniku z Web MIDI podporo (npr. aplikacija *Web MIDI Browser*),
  ali pa synth zaženi na računalniku (Chrome/Edge) s priključenim APC-jem.
- Za pravo iOS aplikacijo (CoreMIDI, AUv3 za AUM/GarageBand) je potreben Mac z Xcode.
- Izklopi tihi način, sicer iOS utiša spletni zvok.

## Zagon
Odpri `index.html` ali ga gostuj (npr. GitHub Pages). Web MIDI zahteva `https://` ali `localhost`.
