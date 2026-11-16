**Langue :** [English](README.md) | [Español](README.es.md) | Français

# Free EQCM512, V.2.0 — Égaliseur Paramétrique 4 Bandes (Korg drumlogue)

**Développé par CrystalMatrix aka Paquini Balandra**

Un égaliseur paramétrique stéréo à 4 bandes spécialement conçu et émulé pour la plateforme **logue SDK** du **Korg drumlogue**. Il permet de sculpter le spectre fréquentiel sur les graves, bas-médiums, haut-médiums et aigus, avec des étages de gain d'entrée/sortie indépendants et des contrôles de mixage parallèle (**Dry & Wet**).

---

## CARACTÉRISTIQUES

1. **Traitement stéréo complet :** inclut un lissage des paramètres sans clics ni bruits parasites (*click-free, pop-free*).
2. **4 bandes d'égalisation indépendantes :** L.F. (*Low Frequency* / Graves), L.M.F. (*Low-Mid Frequency* / Bas-médiums), H.M.F. (*High-Mid Frequency* / Haut-médiums) et H.F. (*High Frequency* / Aigus).
3. **Contrôle de structure de gain :** réglages indépendants du gain d'entrée (`INPUT`) et de sortie (`OUTPUT`), allant de `-20.0 dB` à `+20.0 dB`.
4. **Mixage parallèle :** contrôles dédiés pour le signal traité (`WET`) et le signal d'origine (`DRY`).

---

## INSTALLATION SUR KORG DRUMLOGUE

1. Téléchargez le fichier du plugin compilé (`.drmlgunit`) depuis la section **Releases** de ce dépôt.
2. Connectez votre **Korg drumlogue** à votre ordinateur via USB en **Mode Stockage** (*Storage Mode*).
3. Copiez le fichier `.drmlgunit` dans le dossier d'effets correspondant (`Units/MasterFX` ou `Units/ModFX`, selon la version compilée).
4. Éjectez le périphérique en toute sécurité et redémarrez le synthétiseur.

---

## PARAMÈTRES ET CONTRÔLES

### ÉTAGE D'ENTRÉE ET DE MIXAGE — *Première page sur le drumlogue*

| Paramètre | Étiquette | Plage | Par défaut | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Gain d'entrée** | `INPUT` | `-20.0 dB` à `+20.0 dB` | `0.0 dB` | Ajuste le niveau du signal avant qu'il n'entre dans les bandes d'égalisation. |
| **Niveau Wet** | `WET` | `0.0` à `10.0` | `10.0` | Niveau de volume de sortie du signal égalisé. |
| **Niveau Dry** | `DRY` | `0.0` à `10.0` | `0.0` | Niveau de volume de sortie du signal non traité (utile pour l'égalisation parallèle). |
| **Gain de sortie** | `OUTPUT` | `-20.0 dB` à `+20.0 dB` | `0.0 dB` | Contrôle le niveau de sortie final. |
