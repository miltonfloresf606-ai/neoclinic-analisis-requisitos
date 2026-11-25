# Checklists de Aceptación y Observaciones — NEO_CLINIC

## Revisión 1: Historia Clínica y Laboratorio
* **Verificación de alergias:** Se comprobó la separación y limpieza de términos con paréntesis (como 'Penicilina (rash)') y la evaluación de alertas por coincidencia, familia farmacológica y reacción cruzada.
* **Verificación de rangos y decimales:** Se validó la lectura de valores con coma ('14,2') y punto ('14.2'), el ajuste por altitud y la consulta de rangos infantiles con tuplas (edad_min, edad_max, lim_inf, lim_sup) y retorno None cuando no aplica.
* **Observaciones atendidas:** Se corrigieron discrepancias en claves/estructuras de datos, casos límite de rangos y codificación de textos en UTF-8.
