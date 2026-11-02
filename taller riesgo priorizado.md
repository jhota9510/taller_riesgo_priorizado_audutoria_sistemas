# Taller: Del Riesgo Priorizado al Plan de Auditoría

**Integrantes:**
- Wilfer Andres Carmona Orrego
- Jhonatan Moreno Hernandez

**Enlace al documento:** [Google Sheets - Matriz Unificada](https://docs.google.com/spreadsheets/d/10Nw3ttPou5gd7gfLSH_SRwkhoOxuNZx17GAFE-f2e1Y/edit?usp=sharing)  
**Institución:** Pascual Bravo — Tec. Desarrollo De Software  
**Asignatura:** Auditoria de Sistemas  
**Docente:** Juan Duque  
**Año:** 2026  

---

## Contexto del caso

En el área de ensamble de cubiertas de gas de la planta de Copacabana. En este proceso se instala el marco de la cubierta y se usan tuberías de aluminio, copas, inyectores y válvulas. Los códigos de las tuberías y las copas se registran en SAP para llevar el control de los materiales que se usan y de lo que se produce.

Unos de los posibles errores es escribir un código en SAP que puede afectar el inventario y también puede hacer que una cubierta quede mal ensamblada. Este plan se concentra en revisar cómo se registran esos códigos y qué controles podrían ayudar a evitar errores.

---

## Riesgo seleccionado de la matriz

| Campo | Información de la matriz vigente |
| :--- | :--- |
| **ID del riesgo** | R-01: Registro e historial de trazabilidad en SAP |
| **Activo o proceso** | Registro e historial de códigos de tuberías y copas en SAP |
| **Amenaza** | Digitación incorrecta o error manual de códigos por parte del operario durante el turno |
| **Vulnerabilidad** | No hay validación automática con lector de código de barras o QR en el punto de registro |
| **Consecuencia posible** | Se puede descontar material incorrecto, generar diferencias en el inventario y producir ensambles defectuosos |
| **Probabilidad** | 4 de 5 |
| **Impacto** | 4 de 5 |
| **Nivel de riesgo** | 16 (4 × 4), riesgo de alta prioridad |
| **Control actual indicado** | El registro se hace por digitación manual, sin control automático |
| **Control propuesto en la matriz** | Usar un lector de códigos de barras o QR conectado con SAP |

La matriz señala que este riesgo es de alta prioridad porque puede ocurrir durante el registro manual y puede afectar tanto el inventario como el ensamble de las cubiertas. Es un proceso concreto que se puede revisar por medio de registros, códigos y documentos. La auditoría propuesta busca saber si existen controles para detectar y corregir esos errores.

---

## Objetivo de auditoría

Determinar si el registro de los códigos de tuberías y copas en SAP cuenta con controles que ayudan a evitar, detectar y corregir errores de digitación durante el proceso de ensamble de cubiertas de gas, mediante la revisión del procedimiento, los registros del periodo elegido y la evidencia de las correcciones.

---

## Alcance de la auditoría

| Elemento | Alcance propuesto |
| :--- | :--- |
| **Proceso** | Registro de códigos de tuberías y copas usados en el ensamble de cubiertas de gas |
| **Sistema** | SAP, en la parte que permite registrar y consultar los códigos y movimientos de esos materiales |
| **Población** | Los registros de códigos de tuberías y copas del periodo que se acuerde con la empresa. La cantidad real se solicitará; no se conoce todavía |
| **Periodo** | Del 1 de agosto al 30 de septiembre de 2026. Se propone este periodo de dos meses para revisar registros recientes de producción; la empresa debe confirmar si hay datos disponibles |
| **Áreas y responsables** | Operarios que hacen el registro, supervisor del área de ensamble y personal de TI o SAP que pueda explicar los registros y los permisos |
| **Incluye** | Forma de registrar códigos, revisión de datos, corrección de errores y evidencia que permita saber quién hizo un cambio |
| **No incluye** | Una revisión completa de todos los módulos de SAP, la auditoría de toda la planta ni pruebas físicas de seguridad del producto. Estas actividades quedan fuera porque el objetivo se centra en el registro de códigos |
| **Límite** | Si no se entregan registros o documentos suficientes no se podrá determinar si el control funciona durante todo el periodo |

---

## Criterios para revisar

Los criterios son las condiciones que se compararán con la información de la empresa. En los trabajos anteriores se eligió ISO/IEC 27001, COBIT e ITIL. Para este riesgo se usará principalmente **ISO/IEC 27001**, porque el tema es cuidar los datos de SAP y revisar quién puede hacer cambios. **COBIT** puede servir como apoyo para revisar si hay responsables y reglas claras.

| Criterio | Fuente y estado |
| :--- | :--- |
| Los códigos registrados deben coincidir con el código del componente que se usa en el ensamble | Se debe confirmar con el procedimiento de registro de materiales y con la forma de trabajo vigente del área |
| Los errores encontrados deben poder identificarse y corregirse, dejando información de qué se cambió y quién lo hizo | Criterio por confirmar mediante solicitud del procedimiento vigente y de los registros de corrección |
| El acceso para crear o cambiar códigos debe estar limitado a las personas autorizadas para esa tarea | Se revisará con la lista de usuarios y permisos de SAP y con las reglas internas vigentes. La lista formal no aparece en los trabajos entregados |
| Los registros deben permitir revisar el código y el movimiento realizado | Se propone como condición para la trazabilidad. Se debe confirmar qué campos guarda SAP y qué pide el procedimiento de la empresa |
| **Marco de apoyo** | ISO/IEC 27001, elegido en el primer trabajo para cuidar los datos y controlar quién puede modificarlos. COBIT se usará solo como apoyo para revisar responsables y reglas |

---

## Programa de trabajo

Se proponen dos procedimientos principales y una revisión adicional. Los pasos se pueden ajustar cuando la empresa confirme qué información guarda SAP y qué documentos tiene disponibles.

| Control a evaluar | Criterio y fuente | Procedimiento del auditor | Población o muestra | Evidencia esperada y posibles excepciones |
| :--- | :--- | :--- | :--- | :--- |
| **Forma de registrar los códigos** | El código registrado debe coincidir con el componente usado.<br><br>*Fuente: procedimiento vigente, por confirmar.* | 1) Solicitar el procedimiento.<br>2) Preguntar al operario cómo registra el código.<br>3) Observar, si se permite, un registro de prueba.<br>4) Comparar los pasos con el documento y anotar diferencias. | Proceso de registro en SAP y registros del periodo. Se observará una operación autorizada si la empresa lo permite. | Procedimiento, explicación del operario y registro de prueba.<br><br>*Excepción: pasos diferentes al procedimiento o falta de documento.* |
| **Revisión de registros y errores** | Los registros deben permitir identificar el código usado y revisar errores o correcciones.<br><br>*Fuente: procedimiento y campos de SAP por confirmar.* | 1) Pedir el listado completo del periodo.<br>2) Confirmar cuántos registros contiene.<br>3) Elegir una muestra.<br>4) Comparar cada código con el documento o fuente autorizada del componente.<br>5) Revisar si los errores tienen corrección y explicación. | Todos los registros del periodo, si es posible. Si son muchos, muestra de registros de distintos días y turnos. El tamaño se define después de conocer la población. | Listado exportado de SAP, documentos de componentes y registros de corrección.<br><br>*Excepción: código diferente, falta de dato o corrección sin explicación.* |
| **Quién puede cambiar códigos** | Solo las personas autorizadas deben crear o modificar códigos.<br><br>*Fuente: lista de permisos y regla interna, por confirmar.* | 1) Solicitar usuarios y permisos relacionados.<br>2) Comparar los permisos con los cargos autorizados.<br>3) Revisar una muestra de cambios y el usuario que los hizo, si SAP guarda esa información. | Lista de usuarios con permiso y cambios del periodo. Se revisarán todos si son pocos; si no, se escogerá una muestra según cantidad y disponibilidad. | Listado de permisos y registro de cambios.<br><br>*Excepción: usuario sin autorización, permisos que no se pueden explicar o falta de historial.* |

---

## Cómo se escogería la muestra

1. Primero se pediría la cantidad total de registros del periodo.
2. Si la cantidad es pequeña, se revisarán todos.
3. Si es grande, se escogerán registros de diferentes días y turnos, e incluirán registros con correcciones o errores reportados.
4. La selección se dejará escrita para que otra persona pueda repetirla.

---

## Cómo se guardaría la evidencia

- Guardar el nombre del archivo o documento, la fecha en que se recibió y el periodo que cubre.
- Anotar qué registro se revisó, qué criterio se comparó y cuál fue el resultado de esa comparación.
- Conservar solo la información necesaria y seguir las reglas de la empresa para cuidar los datos.
- Si no se entrega una evidencia, escribir *"no entregada"* o *"pendiente"* sin decir que el control falló por ese solo motivo.

---

## Cronograma y responsables

| Fase | Actividad | Responsables propuestos | Tiempo estimado |
| :--- | :--- | :--- | :--- |
| **Preparación** | Confirmar el riesgo, el objetivo, el periodo y la lista de información que se pedirá | Equipo auditor: Wilfer Andrés y Jhonatan Moreno | 1 día. Depende de acordar el alcance |
| **Solicitud de información** | Pedir procedimiento, listado de registros SAP, lista de permisos y registros de corrección | Equipo auditor; supervisor y responsable de SAP entregan la información | 2 días. Depende de la disponibilidad de la empresa |
| **Revisión** | Comparar el procedimiento con el proceso explicado y revisar la muestra de registros | Equipo auditor; operarios y supervisor aclaran dudas | 3 días. Depende de recibir los archivos y poder consultarlos |
| **Organización de evidencia** | Guardar referencias, resultados de comparación y excepciones encontradas | Equipo auditor | 1 día, después de la revisión |
| **Cierre propuesto** | Presentar qué se revisó, qué evidencia faltó y qué preguntas quedan pendientes | Equipo auditor y responsables del área | 1 día. Se requiere una reunión de cierre |

---

**Enlace a la matriz Unificada:** [Google Sheets - Matriz Unificada](https://docs.google.com/spreadsheets/d/10Nw3ttPou5gd7gfLSH_SRwkhoOxuNZx17GAFE-f2e1Y/edit?usp=sharing)