**Sprache:** [English](README.md) | [Español](README.es.md) | [Français](README.fr.md) | [日本語](README.ja.md) | [中文](README.zh.md) | Deutsch

# Free EQCM512, V.2.0 — Parametrischer 4-Band-Equalizer (Korg drumlogue)

**Entwickelt von CrystalMatrix aka Paquini Balandra**

Ein parametrischer 4-Band-Stereo-Equalizer, der speziell für die **logue SDK**-Plattform des **Korg drumlogue** entwickelt und emuliert wurde. Er ermöglicht die präzise Bearbeitung des Frequenzspektrums über Bässe, untere Mitten, obere Mitten und Höhen und verfügt über unabhängige Ein- und Ausgangs-Gain-Stufen sowie Regler für paralleles Mixing (**Dry & Wet**).

---

## FUNKTIONEN

1. **Vollständige Stereoverarbeitung:** Beinhaltet eine Parameter-Glättung (*Parameter Smoothing*) ohne Klicken oder Knackgeräusche (*click-free, pop-free*).
2. **4 unabhängige EQ-Bänder:** L.F. (*Low Frequency* / Bässe), L.M.F. (*Low-Mid Frequency* / Untere Mitten), H.M.F. (*High-Mid Frequency* / Obere Mitten) und H.F. (*High Frequency* / Höhen).
3. **Gain-Staging-Kontrolle:** Unabhängige Anpassung von Eingangs- (`INPUT`) und Ausgangs-Gain (`OUTPUT`) im Bereich von `-20.0 dB` bis `+20.0 dB`.
4. **Paralleles Mixing:** Dedizierte Regler für das bearbeitete Signal (`WET`) und das Originalsignal (`DRY`).

---

## INSTALLATION AUF DEM KORG DRUMLOGUE

1. Laden Sie die kompilierte Plugin-Datei (`.drmlgunit`) aus dem Bereich **Releases** dieses Repositorys herunter.
2. Verbinden Sie Ihren **Korg drumlogue** per USB im **Speichermodus** (*Storage Mode*) mit Ihrem Computer.
3. Kopieren Sie die `.drmlgunit`-Datei in den entsprechenden Effekt-Ordner (`Units/MasterFX` oder `Units/ModFX`, je nach kompilierter Version).
4. Werfen Sie das Laufwerk sicher aus und starten Sie den Synthesizer neu.

---

## PARAMETER & BEDIENELEMENTE

### EINGANGS- UND MIX-STUFE — *Erste Seite auf dem drumlogue*

| Parameter | Beschriftung | Bereich | Standard | Beschreibung |
| :--- | :--- | :--- | :--- | :--- |
| **Eingangs-Gain** | `INPUT` | `-20.0 dB` bis `+20.0 dB` | `0.0 dB` | Passt den Signalpegel an, bevor das Signal die EQ-Bänder durchläuft. |
| **Wet-Pegel** | `WET` | `0.0` bis `10.0` | `10.0` | Ausgangslautstärke des mit dem EQ bearbeiteten Signals. |
| **Dry-Pegel** | `DRY` | `0.0` bis `10.0` | `0.0` | Ausgangslautstärke des unbearbeiteten Signals (nützlich für paralleles EQing). |
| **Ausgangs-Gain** | `OUTPUT` | `-20.0 dB` bis `+20.0 dB` | `0.0 dB` | Steuert den endgültigen Ausgangspegel. |
