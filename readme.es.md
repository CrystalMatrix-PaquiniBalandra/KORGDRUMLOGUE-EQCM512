KORGDRUMLOGUE-EQCM512.V.2.0.

KORG DRUMLOGUE-CRYSTALMATRIX EQ
Free EQCM512, V.2.0 — 4-Band Parametric EQ (Korg drumlogue)

Desarrollado por CrystalMatrix aka Paquini Balandra

Es un ecualizador paramétrico estéreo de 4 bandas específicamente diseñado y emulado para la plataforma logue SDK de Korg drumlogue. Permite esculpir el espectro de frecuencias graves, medias graves, medias agudas y agudas; además incluye controles independientes de ganancia de entrada, salida y mezcla paralela (Dry & Wet).
CARACTERÍSTICAS

    Procesamiento estéreo completo: incluye suavizado de parámetros libre de clics, brincos y pops.
    4 bandas de ecualización independientes: L.F. (Low Frequency), L.M.F. (Low-Mid Frequency), H.M.F. (High-Mid Frequency) y H.F. (High Frequency).
    Control de etapa de ganancia: ajuste de ganancia de entrada (INPUT) y salida (OUTPUT), con un margen de -20.0 dB hasta +20.0 dB.
    Mezcla paralela: incluye controles dedicados para señal procesada (WET) y señal original (DRY).

INSTALACIÓN EN KORG DRUMLOGUE

    Descarga el archivo del plugin compilado (.drmlgunit) desde la sección Releases de este repositorio.
    Conecta tu Korg drumlogue a tu computadora mediante USB en modo almacenamiento (Storage Mode).
    Copia el archivo .drmlgunit dentro de la carpeta correspondiente a efectos (Units/MasterFX o Units/ModFX, según la compilación).
    Expulsa la unidad de forma segura y reinicia el sintetizador.

PARÁMETROS Y CONTROLES
ETAPA DE ENTRADA Y MEZCLA — Primera ventana en drumlogue
Parámetro 	Etiqueta 	Rango 	Valor por defecto 	Descripción
Input Gain 	INPUT 	-20.0 dB a +20.0 dB 	0.0 dB 	Ajusta el nivel de la señal antes de entrar a las bandas de ecualización.
Wet Level 	WET 	0.0 a 10.0 	10.0 	Nivel de volumen de la señal ya ecualizada.
Dry Level 	DRY 	0.0 a 10.0 	0.0 	Nivel de volumen de la señal limpia sin procesar (útil para ecualización paralela).
Output Gain 	OUTPUT 	-20.0 dB a +20.0 dB 	0.0 dB 	Controla el nivel final de salida del efecto.
BANDAS DE ECUALIZACIÓN
1. Banda Grave — L.F. (Low Frequency) — Segunda ventana

Ideal para dar peso al bombo (kick) o limpiar frecuencias subgraves (Low Shelf).
Parámetro 	Etiqueta 	Rango 	Valor por defecto 	Descripción
Frecuencia 	FRQLF 	20 Hz – 400 Hz 	100 Hz 	Frecuencia de corte del filtro Low Shelf.
Resonancia / Q 	QLF 	0.107 – 2.507 	0.707 	Controla la pendiente y resonancia de la curva.
Ganancia 	GLF 	-15.0 dB a +15.0 dB 	0.0 dB 	Atenúa o realza las frecuencias graves.
2. Banda Media-Grave — L.M.F. (Low-Mid Frequency) — Tercera ventana

Útil para controlar el cuerpo de la caja (snare), toms o eliminar resonancias acartonadas (Peak / Bell).
Parámetro 	Etiqueta 	Rango 	Valor por defecto 	Descripción
Frecuencia 	FRQLMF 	100 Hz – 2000 Hz 	700 Hz 	Frecuencia central de la campana.
Ancho de banda / Q 	QLMF 	0.107 – 2.507 	0.707 	Valores bajos afectan un rango amplio; valores altos son más quirúrgicos.
Ganancia 	GLMF 	-15.0 dB a +15.0 dB 	0.0 dB 	Atenúa o realza alrededor de la frecuencia seleccionada.
3. Banda Media-Aguda — H.M.F. (High-Mid Frequency) — Cuarta ventana

Enfocada en la presencia, el ataque de las baquetas y la definición de los sintetizadores (Peak / Bell).
Parámetro 	Etiqueta 	Rango 	Valor por defecto 	Descripción
Frecuencia 	FRQHMF 	400 Hz – 8000 Hz 	2500 Hz 	Frecuencia central de la campana.
Ancho de banda / Q 	QHMF 	0.107 – 2.507 	0.707 	Controla la amplitud de la campana.
Ganancia 	GHMF 	-15.0 dB a +15.0 dB 	0.0 dB 	Atenúa o realza la zona media-aguda.
4. Banda Aguda — H.F. (High Frequency) — Quinta ventana

Añade aire y brillo a platillos (hi-hats), platos y colas de reverberación (High Shelf).
Parámetro 	Etiqueta 	Rango 	Valor por defecto 	Descripción
Frecuencia 	FRQHF 	1000 Hz – 20000 Hz 	10000 Hz 	Frecuencia de corte del filtro High Shelf.
Resonancia / Q 	QHF 	0.107 – 2.507 	0.707 	Controla la pendiente de transición hacia los agudos.
Ganancia 	GHF 	-15.0 dB a +15.0 dB 	0.0 dB 	Atenúa o realza las frecuencias altas.
FLUJO DE LA SEÑAL

[ADC IN] ──> [INPUT GAIN] ──┬──> [LF] ──> [LMF] ──> [HMF] ──> [HF] ──> [WET GAIN] ──┐
                            │                                                       ├──> [OUTPUT GAIN] ──> [DAC OUT]
                            └────────────────────────────────────────> [DRY GAIN] ──┘

DESARROLLO Y COMPILACIÓN

Esta emulación fue desarrollada en Pure Data, PlugData y la librería Heavylib por CrystalMatrix aka Paquini Balandra, y compilada utilizando Heavy Compiler (hvcc), el logue SDK de Korg y la herramienta web de conversión boochow pd2drumlogue.
CRÉDITOS Y LICENCIA

    Autor / Emulación: CrystalMatrix aka Paquini Balandra
    Licencia: Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo LICENSE para más detalles.
