# Historias de Usuario: Historia Clínica y Laboratorio — NEO_CLINIC

## HU-HIS-01: Normalización de alergias y alertas al prescribir
**Como** médico, **quiero** que el sistema limpie el texto de alergias registradas y me alerte si un medicamento coincide, pertenece a la misma familia o implica reacción cruzada, **para** evitar prescripciones riesgosas para el paciente.

* **Criterio 1 (Caso normal / limpieza):** **Dado** un paciente con alergia registrada como `"Penicilina (rash)"`, **cuando** el sistema normaliza el término, **entonces** extrae `"Penicilina"` sin el detalle entre paréntesis.
* **Criterio 2 (Caso borde / alerta):** **Dado** un paciente con alergia registrada, **cuando** se prescribe un fármaco con coincidencia exacta, misma familia o reacción cruzada, **entonces** el sistema muestra una alerta de precaución antes de confirmar.
* **Criterio 3 (Caso sin alergias):** **Dado** un paciente sin alergias registradas, **cuando** se evalúa una prescripción, **entonces** el sistema no genera alerta de alergia.

## HU-LAB-01: Lectura decimal, ajuste por altitud y rangos de referencia
**Como** profesional de laboratorio o médico, **quiero** que el sistema acepte valores decimales con coma o punto, ajuste la hemoglobina por altitud según criterios de la OMS y calcule rangos por edad y sexo, **para** interpretar correctamente los resultados clínicos.

* **Criterio 1 (Caso normal / decimal):** **Dado** un resultado manual ingresado como `"14,2"` o `"14.2"`, **cuando** el sistema lo procesa, **entonces** lo interpreta como valor decimal `14.2` y lo compara con el rango correspondiente.
* **Criterio 2 (Caso borde / rango pediátrico y retorno nulo):** **Dado** un parámetro con rangos en `"ninos"` usando tuplas `(edad_min, edad_max, lim_inf, lim_sup)`, **cuando** se consulta una edad válida (por ejemplo, `edad=8`) devuelve el rango respectivo, y **cuando** se consulta una edad sin rango aplicable (por ejemplo, `edad=2`), **entonces** devuelve `None`.
* **Criterio 3 (Caso de altura):** **Dado** un paciente ubicado en altitud (por ejemplo, `3827 m` o `2500 m`), **cuando** se calcula el ajuste por altitud, **entonces** aplica el factor correspondiente según la referencia de la OMS.
