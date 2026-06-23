# Forward Deployed Bioinformatics Playbook

Este playbook convierte la guia en una practica de campo. La meta no es saber
mas teoria; es poder entrar a un laboratorio, entender una necesidad real,
construir una solucion repetible y dejarla operando.

## 1. Intake

Antes de tocar datos, llena esto:

```text
Decision que se quiere tomar:
Usuario final:
Dato disponible:
Formato:
Volumen:
Restricciones: privacidad, tiempo, costo, compute, regulacion
Metrica tecnica:
Metrica biologica:
Baseline aceptable:
Entrega esperada:
Responsable despues del handoff:
```

## 2. Diagnostico del dato

Un FDE no asume que el dato esta listo.

- Procedencia y version.
- Manifest o schema.
- IDs y metadata.
- Duplicados y faltantes.
- Batch effects o sesgos de muestreo.
- Permisos de uso y comparticion.

## 3. Arquitectura minima

```text
input -> validacion -> transformacion -> modelo/metodo -> reporte -> handoff
```

Cada flecha debe tener:

- comando o notebook que la produce,
- parametros visibles,
- ambiente reproducible,
- salida nombrada,
- log o evidencia.

## 4. Delivery package

La entrega minima debe incluir:

- `README` de ejecucion.
- Datos de ejemplo o manifest.
- Ambiente: `environment.yml`, `requirements.txt` o contenedor.
- Script/notebook/pipeline parametrizado.
- Reporte con resultado, incertidumbre y limites.
- Runbook de fallas.
- Checklist de validacion.

## 5. Validacion

No basta con "corrio".

- Corre dos veces con la misma entrada.
- Compara contra baseline simple.
- Revisa fuga de informacion.
- Revisa plausibilidad biologica.
- Reporta que NO demuestra el resultado.

## 6. Handoff

La prueba real: otra persona puede correrlo sin ti.

Debe poder responder:

- Como instalo?
- Como corro?
- Donde pongo el input?
- Donde sale el output?
- Como se que fallo?
- Que hago si falla?
- Que decision puedo tomar con el resultado?

## 7. Rubrica FDE

| Nivel | Evidencia |
| --- | --- |
| Analista | Corre notebooks y explica metricas. |
| Builder | Automatiza un flujo repetible. |
| FDE junior | Entrega pipeline, reporte y runbook. |
| FDE solido | Maneja stakeholders, restricciones, validacion y handoff. |
| FDE senior | Diseña arquitectura, reduce riesgo operacional y deja sistema mantenible. |

## 8. Estandares que debes reconocer

- GA4GH para datos genomicos responsables.
- Nextflow o Snakemake para workflows reproducibles.
- nf-core para convenciones de pipelines.
- CWL para workflows portables.
- RO-Crate para empaquetar metadatos.
- Bioconda/containers para ambientes repetibles.

