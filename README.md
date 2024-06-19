# Introducción
En este repositorio emplearemos la plataforma Beyondcell (Fustero-Torres et al., 2021). Esta se basa en identificar cómo los fármacos afectan a las diferentes líneas celulares en datos de scRNA-seq.
# Descripción del pipeline
- Paso 1: A partir de dos matrices, una matriz de expresión Seurat y una firma de expresión de fármacos (PSc o SSc) calculamos las puntuaciones Beyondcell para cada par célula-fármaco.
- Paso 2: Las puntuaciones Beyondcell varían entre 0 y 1 midiendo la sensibilidad de cada célula a un fármaco. La matriz Beyondcell resultante debe estar escalada y normalizada.
