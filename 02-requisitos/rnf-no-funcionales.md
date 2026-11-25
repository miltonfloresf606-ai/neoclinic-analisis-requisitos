# Requisitos No Funcionales — NEO_CLINIC

* **RNF-SEG-01 (Seguridad y control de acceso):** Las rutas y funciones sensibles deben restringirse según el rol y permisos del usuario autenticado.
* **RNF-AUD-01 (Trazabilidad y auditoría):** Las operaciones relevantes y cambios críticos deben quedar registrados para auditoría y control interno.
* **RNF-INT-01 (Integridad y coherencia de datos):** Los datos entre pacientes, citas, historia clínica, laboratorio, farmacia y facturación deben mantener coherencia y evitar inconsistencias.
* **RNF-COD-01 (Codificación de caracteres):** Los textos, reportes y archivos del sistema deben manejarse en codificación UTF-8 para preservar tildes y caracteres especiales (`á, é, í, ó, ú, ñ`).
* **RNF-RES-01 (Respaldos y recuperación):** El sistema debe contar con mecanismos de respaldo para resguardar la información operativa.
* **RNF-USA-01 (Usabilidad y claridad de mensajes):** Las pantallas, formularios y mensajes de validación deben ser claros para el personal clínico y administrativo.
