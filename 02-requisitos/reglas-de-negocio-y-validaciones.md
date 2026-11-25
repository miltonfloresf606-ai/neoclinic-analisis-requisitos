# Reglas de Negocio y Validaciones — NEO_CLINIC

* **RN-HIS-01 (Normalización de alergias):** Al evaluar alergias registradas como texto (por ejemplo, `"Penicilina (rash)"`), se deben separar múltiples ítems y descartar descripciones entre paréntesis para obtener el término comparable.
* **RN-HIS-02 (Alertas farmacológicas):** Ante una prescripción, el sistema debe advertir cuando exista coincidencia exacta, pertenencia a la misma familia farmacológica o riesgo de reacción cruzada con alergias del paciente.
* **RN-LAB-01 (Lectura decimal flexible):** Los valores numéricos ingresados en laboratorio deben aceptarse tanto con coma decimal (`"14,2"`) como con punto decimal (`"14.2"`) y convertirse a valor numérico válido.
* **RN-LAB-02 (Ajuste por altitud OMS):** Los valores de hemoglobina y rangos aplicables en altura deben considerar el ajuste por altitud sobre el nivel del mar según criterios de la OMS.
* **RN-LAB-03 (Prioridad de rangos por edad y sexo):** Para obtener rangos de referencia, se debe evaluar primero la lista de intervalos pediátricos en `"ninos"` con estructura `(edad_min, edad_max, lim_inf, lim_sup)`; si no aplica a ningún rango infantil, se evalúan los valores por sexo (`"M"` o `"F"`) o se retorna `None` cuando no exista rango aplicable.
* **RN-CIT-01 (Prevención de cruces):** No debe permitirse agendar o reprogramar una cita en un horario ya ocupado que genere conflicto según las reglas de disponibilidad.
* **RN-FAR-01 (Coherencia de stock y recetas):** Los movimientos de inventario, recetas y ventas en farmacia deben mantener consistencia con el stock disponible y el kardex.
