# Historias de Usuario: Operación Clínica y Administrativa — NEO_CLINIC

## HU-CIT-01: Agendar y reprogramar citas sin cruce de horarios
**Como** personal de admisión, **quiero** programar y reprogramar citas médicas verificando disponibilidad, **para** evitar choques de horario en la agenda.

* **Criterio 1 (Caso normal):** **Dado** un profesional con horario libre, **cuando** se registra o reprograma una cita, **entonces** la cita queda guardada en el horario seleccionado.
* **Criterio 2 (Caso de conflicto):** **Dado** un bloque horario ya ocupado por otra cita, **cuando** se intenta agendar o mover otra cita al mismo horario, **entonces** el sistema impide el cruce y notifica el conflicto.
* **Criterio 3 (Caso alterno):** **Dado** una cita vigente, **cuando** se cancela o reprograma a un espacio disponible, **entonces** el estado y el horario se actualizan correctamente.

## HU-EME-01: Atención de emergencias y control de camas
**Como** personal de emergencias, **quiero** registrar atenciones urgentes (incluso cuando la identificación está pendiente) y gestionar la disponibilidad de camas, **para** atender con oportunidad y mantener el control de ocupación.

* **Criterio 1 (Caso normal):** **Dado** un ingreso de emergencia, **cuando** se registra el evento y se asigna una cama libre, **entonces** el paciente queda vinculado a la atención y la cama pasa a estado ocupado.
* **Criterio 2 (Caso borde):** **Dado** un paciente que ingresa sin documento inmediato (caso NN), **cuando** se inicia su atención de emergencia, **entonces** el sistema permite registrarlo para completar su identificación posteriormente.
* **Criterio 3 (Caso sin disponibilidad):** **Dado** que no hay camas libres, **cuando** se intenta asignar una cama, **entonces** el sistema informa la falta de disponibilidad.

## HU-FAR-FAC-01: Despacho de recetas, stock y facturación coherente
**Como** encargado de farmacia o caja, **quiero** que el despacho de medicamentos y la facturación mantengan coherencia con el inventario y las atenciones, **para** evitar faltantes no registrados o montos inconsistentes.

* **Criterio 1 (Caso normal):** **Dado** una receta o venta con stock suficiente, **cuando** se registra la salida, **entonces** se actualiza el stock/kardex y se genera el comprobante correspondiente.
* **Criterio 2 (Caso de error / falta de stock):** **Dado** un medicamento sin stock suficiente, **cuando** se intenta completar el despacho, **entonces** el sistema bloquea o advierte la insuficiencia de inventario.
* **Criterio 3 (Caso de coherencia):** **Dado** movimientos registrados en el sistema, **cuando** se revisan reportes o cuentas, **entonces** los datos mantienen coherencia entre módulos.
