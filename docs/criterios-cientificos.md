# Criterios cientificos

Usa esta lista antes de decir que un resultado "funciona".

## Datos

- Se conoce la procedencia de los datos.
- Hay identificadores, versiones y fecha de descarga.
- Se revisaron duplicados, faltantes y outliers.
- La division train/test no filtra informacion.

## Modelo

- Existe un baseline simple.
- La metrica responde a la pregunta biologica.
- El modelo no se evalua solo en entrenamiento.
- El resultado se interpreta con incertidumbre.

## Biologia

- El resultado tiene sentido con conocimiento del dominio.
- Se distinguen correlacion, prediccion y mecanismo.
- Se indica que parte requiere validacion experimental.

## Reproducibilidad

- Ambiente, versiones y seeds estan documentados.
- El flujo puede repetirse sin pasos manuales escondidos.
- La bitacora registra datos, transformaciones, resultado y limite.

