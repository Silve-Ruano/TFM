
![B](https://github.com/Silve-Ruano/TFM/assets/157005665/1f9ec5e4-fc2a-474f-93dc-c876f0fe1486)
# Introducción
En este repositorio emplearemos la plataforma Beyondcell (Fustero-Torres et al., 2021). Esta se basa en identificar cómo los fármacos afectan a las diferentes líneas celulares en datos de scRNA-seq. Se trabaja en entorno R.
# Descripción del pipeline
![BCpipeline](https://github.com/Silve-Ruano/TFM/assets/157005665/48ee4417-9852-43d1-b1ff-ddc11cb0d847)

- Paso 1: A partir de dos matrices, una matriz de expresión Seurat (pre-procesada) y una firma de expresión de fármacos (PSc o SSc) calculamos las puntuaciones Beyondcell para cada par célula-fármaco.
- Paso 2: Las puntuaciones Beyondcell varían entre 0 y 1 midiendo la sensibilidad de cada célula a un fármaco. La matriz Beyondcell resultante debe estar escalada y normalizada.
- Paso 3: Con la matriz Beyondcell podemos obtener los clusteres terapéuticos (en UMAP) del dataset que deseemos, según la característica que queramos resaltar.
- Paso 4: Realizamos una priorización de fármacos obteniendo un ranking tras computar los rangos.
- Paso 5: La puntuación obtenida de cada medicamento (la susceptibilidad) se puede visualizar en una UMAP.

NOTA: La matriz PSc indica la susceptibilidad a la perturbación (antes vs después) y la SSc muestra la sensibilidad de las células a un fármaco. 

# Aplicaciones actuales
- Posibilidad de emplear una herramienta confiable para desentrañar la Heterogeneidad Tumoral.
- Ordenar fármacos por su efecto en varias líneas celulares tumorales.
- Priorizar medicamentos en la lucha contra determinados tipo de cáncer.

# Aplicaciones futuras
- Se incluirá una capa para la realización de Transcriptómica Espacial (ST), para investigar patrones de expresión dentro de tejidos (Próximamente).
- Detectar mecanismos de resistencia y de tolerancia frente a los medicamentos de las firmas farmacológicas.

# ¿Cómo instalamos el paquete 'Beyondcell'?
Se recomienda instalar el paquete Beyondcell en una versión de R >= 4.0.0. Asimismo, es necesario para su correcto funcionamiento la v4 Seurat. Para la correcta instalación del paquete usamos un ambiente conda: 

``` ruby
# Create a conda environment.
conda create -n beyondcell 
# Activate the environment.
conda activate beyondcell
# Install beyondcell package and dependencies.
mamba install -c bu_cnio r-beyondcell
```
# Autores
- Silvestre Ruano Rodríguez*
- Juan Antonio Nepomuceno Chamorro
- Isabel de los Ángeles Nepomuceno Chamorro
- Fátima Al-Shahrour
- María José Jiménez Santos ('Piti')
# Citación

# Apoyo técnico
Si surge alguna duda, recomendamos comentarlo en la pestaña 'issue' para su resolución. En caso de no resolverse de esta forma, no dude en enviar un email con la incidencia a silruarod@alum.us.es
