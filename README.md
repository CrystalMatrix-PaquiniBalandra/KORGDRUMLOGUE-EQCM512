**Language:** English | [Español](README.es.md) | [Français](README.fr.md) | [日本語](README.ja.md) | [中文](README.zh.md) | [Deutsch](README.de.md)

# KORGDRUMLOGUE-EQCM512.V.2.0

## KORG DRUMLOGUE - CRYSTALMATRIX EQ
### Free EQCM512, V.2.0 — 4-Band Parametric EQ (Korg drumlogue)

**Developed by CrystalMatrix aka Paquini Balandra**

A 4-band stereo parametric equalizer specifically designed and emulated for the **Korg drumlogue** **logue SDK** platform. It allows you to sculpt the frequency spectrum across lows, low-mids, high-mids, and highs; it also includes independent input and output gain controls, as well as parallel mixing (**Dry & Wet**).

---

## FEATURES

* **Full stereo processing:** Includes parameter smoothing free of clicks, jumps, and pops.
* **4 independent EQ bands:** L.F. (*Low Frequency*), L.M.F. (*Low-Mid Frequency*), H.M.F. (*High-Mid Frequency*), and H.F. (*High Frequency*).
* **Gain staging control:** Independent input (`INPUT`) and output (`OUTPUT`) gain adjustments, ranging from `-20.0 dB` to `+20.0 dB`.
* **Parallel mixing:** Dedicated controls for the processed signal (`WET`) and the original dry signal (`DRY`).

---

## INSTALLATION ON KORG DRUMLOGUE

1. Download the compiled plugin file (`.drmlgunit`) from the **Releases** section of this repository.
2. Connect your **Korg drumlogue** to your computer via USB in **Storage Mode**.
3. Copy the `.drmlgunit` file into the corresponding effects folder (`Units/MasterFX` or `Units/ModFX`, depending on the build).
4. Safely eject the drive and restart the synthesizer.

---

## PARAMETERS & CONTROLS

### INPUT & MIX STAGE — *First Page on drumlogue*

| Parameter | Label | Range | Default | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Input Gain** | `INPUT` | `-20.0 dB` to `+20.0 dB` | `0.0 dB` | Adjusts the signal level before entering the EQ bands. |
| **Wet Level** | `WET` | `0.0` to `10.0` | `10.0` | Output volume level of the equalized signal. |
| **Dry Level** | `DRY` | `0.0` to `10.0` | `0.0` | Output volume level of the clean, unprocessed signal (useful for parallel EQ). |
| **Output Gain** | `OUTPUT` | `-20.0 dB` to `+20.0 dB` | `0.0 dB` | Controls the final output level of the effect. |

---

## EQUALIZATION BANDS

### 1. Low Band — L.F. (Low Frequency) — *Second Page*

Ideal for adding weight to the kick drum or cleaning up sub-bass frequencies (*Low Shelf*).

| Parameter | Label | Range | Default | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Frequency** | `FRQLF` | `20 Hz` – `400 Hz` | `100 Hz` | Cutoff frequency of the Low Shelf filter. |
| **Resonance / Q** | `QLF` | `0.107` – `2.507` | `0.707` | Controls the slope and resonance of the curve. |
| **Gain** | `GLF` | `-15.0 dB` to `+15.0 dB` | `0.0 dB` | Cuts or boosts low frequencies. |

### 2. Low-Mid Band — L.M.F. (Low-Mid Frequency) — *Third Page*

Useful for controlling the body of the snare, toms, or removing boxy resonances (*Peak / Bell*).

| Parameter | Label | Range | Default | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Frequency** | `FRQLMF` | `100 Hz` – `2000 Hz` | `700 Hz` | Center frequency of the bell filter. |
| **Bandwidth / Q** | `QLMF` | `0.107` – `2.507` | `0.707` | Lower values affect a wider range; higher values are more surgical. |
| **Gain** | `GLMF` | `-15.0 dB` to `+15.0 dB` | `0.0 dB` | Cuts or boosts around the selected frequency. |

### 3. High-Mid Band — H.M.F. (High-Mid Frequency) — *Fourth Page*

Focused on presence, stick attack, and synthesizer definition (*Peak / Bell*).

| Parameter | Label | Range | Default | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Frequency** | `FRQHMF` | `400 Hz` – `8000 Hz` | `2500 Hz` | Center frequency of the bell filter. |
| **Bandwidth / Q** | `QHMF` | `0.107` – `2.507` | `0.707` | Controls the width of the bell curve. |
| **Gain** | `GHMF` | `-15.0 dB` to `+15.0 dB` | `0.0 dB` | Cuts or boosts the high-mid frequency range. |

### 4. High Band — H.F. (High Frequency) — *Fifth Page*

Adds air and shimmer to hi-hats, cymbals, and reverb tails (*High Shelf*).

| Parameter | Label | Range | Default | Description |
| :--- | :--- | :--- | :--- | :--- |
| **Frequency** | `FRQHF` | `1000 Hz` – `20000 Hz` | `10000 Hz` | Cutoff frequency of the High Shelf filter. |
| **Resonance / Q** | `QHF` | `0.107` – `2.507` | `0.707` | Controls the transition slope toward the highs. |
| **Gain** | `GHF` | `-15.0 dB` to `+15.0 dB` | `0.0 dB` | Cuts or boosts high frequencies. |

---

## SIGNAL FLOW

```text
[ADC IN] ──> [INPUT GAIN] ──┬──> [LF] ──> [LMF] ──> [HMF] ──> [HF] ──> [WET GAIN] ──┐
                            │                                                       ├──> [OUTPUT GAIN] ──> [DAC OUT]
                            └────────────────────────────────────────> [DRY GAIN] ──┘
```

---

## DEVELOPMENT & COMPILATION

This emulation was developed in **Pure Data**, **PlugData**, and the **Heavylib** library by **CrystalMatrix aka Paquini Balandra**, and compiled using **Heavy Compiler (`hvcc`)**, the **Korg logue SDK**, and the web conversion tool **boochow pd2drumlogue**.

---

## CREDITS & LICENSE

* **Author / Emulation:** CrystalMatrix aka Paquini Balandra
* **License:** This project is distributed under the **MIT License**. See the `LICENSE` file for more details.
