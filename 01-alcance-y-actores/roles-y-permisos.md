# Roles y Permisos — NEO_CLINIC

| Rol | Alcance principal | Restricciones clave |
| :--- | :--- | :--- |
| Administrador | Gestión de usuarios, configuración general, respaldos y auditoría | Toda acción crítica queda registrada en auditoría |
| Médico | Consulta médica, historia clínica, prescripción y revisión de laboratorio | Debe respetar alertas de alergias y rangos clínicos |
| Admisión / Caja | Registro de pacientes, agenda de citas y facturación | No modifica diagnósticos ni resultados de laboratorio |
| Laboratorio | Gestión de órdenes, captura de resultados y reportes | Resultados sujetos a validación de rangos y formatos |
| Farmacia | Control de inventario/kardex, despacho de recetas y ventas | Sujeto a stock disponible y recetas válidas |
