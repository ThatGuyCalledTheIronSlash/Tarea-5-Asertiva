# Tarea #5: Análisis de Trade-offs en un Proyecto de Software

**Universidad de San Carlos de Guatemala**

**Facultad de Ingeniería**

**Laboratorio de Comunicación Asertiva, Sección A, Segundo Semestre 2026**

## Integrantes

|Nombre|Carnet|
|-|-|
|*Nombre 1*|*Carnet*|
|*Nombre 2*|*Carnet*|
|David Antonio Meza Silva|202500708|



## 1. Planteamiento del problema

**Escenario simulado:** desarrollo de un sistema de gestión de inventario y ventas para una pequeña cadena de tiendas.

### 1.1 Contexto del proyecto

Una empresa de desarrollo de software fue contratada para implementar un sistema que reemplace los registros manuales y las hojas de cálculo que las tiendas usan hoy para llevar sus productos y ventas. Lo que se busca es tener información más precisa, agilizar el trabajo diario y contar con datos actualizados para tomar decisiones.

El alcance acordado originalmente incluye estas funciones:

* **Gestión de productos:** registrar, modificar y consultar la información de los artículos.
* **Control de inventario:** actualizar las existencias cada vez que se registra una venta.
* **Registro de ventas:** guardar las transacciones y calcular sus totales.
* **Reportes:** consultar ventas, existencias y productos disponibles.
* **Gestión de usuarios:** controlar el acceso según los permisos de cada empleado.

El equipo son tres desarrolladores y tienen ocho semanas en total para terminar el proyecto.

### 1.2 Descripción del problema

Al terminar la semana 5, el equipo se da cuenta de que va bastante atrasado. En las primeras pruebas aparecen errores al actualizar las existencias, sobre todo cuando dos ventas se registran casi al mismo tiempo. En ese caso, el inventario que muestra el sistema puede no coincidir con el real, y se corre el riesgo de vender productos que ya no hay.

Además, el cliente pidió alertas automáticas para los productos con pocas existencias. Esto no estaba en el alcance inicial y requiere más desarrollo y más pruebas. Aun así, el cliente quiere mantener la fecha de entrega acordada.

Cada parte tiene una prioridad distinta:

* **Cliente:** recibir un sistema útil y completo en la fecha prevista, con las nuevas alertas incluidas.
* **Equipo técnico:** corregir los errores del inventario y hacer suficientes pruebas para reducir fallos.
* **Dirección del proyecto:** cumplir con el presupuesto y el calendario sin dañar la relación con el cliente.

**Problema central:** decidir cómo entregar una solución funcional y confiable con tres semanas restantes, sin pasarse de los recursos disponibles ni poner en riesgo las operaciones de las tiendas.

### 1.3 Restricciones del proyecto

|Restricción|Condición del escenario|
|-|-|
|Tiempo|Plazo total de 8 semanas. Han pasado 5 y quedan 3 para terminar, probar y entregar.|
|Costo|Presupuesto aprobado de Q40,000. No hay fondos adicionales para contratar personal ni para ampliar el plazo.|
|Equipo|Tres desarrolladores que deben repartirse la corrección de errores, las funcionalidades pendientes y las pruebas.|
|Alcance|Se acordaron las funciones básicas de inventario y ventas. Las alertas automáticas son una solicitud posterior.|
|Calidad|El control de existencias tiene que ser consistente. Una entrega con errores podría afectar las ventas y causar pérdidas.|

### 1.4 Decisión que deberá resolver el equipo

El equipo debe comparar alternativas y negociar qué priorizar: mantener la fecha de entrega, asegurar la calidad de las funciones esenciales y decidir si las alertas adicionales se hacen ahora o se dejan para una fase posterior. La decisión tiene que justificar sus efectos sobre el tiempo, el costo, el alcance y la calidad.


## 2. Identificación de trade-offs

Se identifican tres trade-offs relevantes para el problema:

| Trade-Off | Opción A | Opción B |
|---|---|---|
| Rapidez vs. Calidad | Entregar en la fecha acordada (8 semanas) priorizando las funciones esenciales, aunque queden pendientes pruebas exhaustivas. | Extender el plazo para corregir todos los errores de inventario y probar a fondo antes de entregar. |
| Alcance vs. Tiempo | Incluir las alertas automáticas solicitadas por el cliente dentro del plazo original, recortando pruebas o funcionalidades secundarias. | Mantener el alcance original acordado y posponer las alertas a una fase posterior (fase 2). |
| Costo vs. Funcionalidad | Mantener el presupuesto de Q40,000 sin contratar personal adicional, ajustando el alcance y las pruebas a lo que el equipo pueda cubrir. | Contratar apoyo externo o pagar horas extra para cubrir desarrollo y pruebas, excediendo el presupuesto aprobado. |


## 3. Análisis de alternativas

### 3.1 Trade-off 1: Rapidez vs calidad

#### Opción A: Entregar en la fecha acordada priorizando funciones esenciales

* **Explicación:** el equipo se enfoca en corregir solo los errores críticos de inventario, asegura las funciones básicas (productos, ventas, reportes y usuarios) y entrega en la semana 8, dejando las pruebas extensivas para después.
* **Ventajas:**

  * Se cumple el compromiso contractual de la fecha de entrega.
  * El cliente recibe un sistema funcional en el tiempo esperado.
  * Se evita dañar la relación comercial y la reputación del equipo.
* **Desventajas:**

  * Pueden quedar errores sin detectar en el control de existencias.
  * Podrían venderse productos que no están disponibles por inconsistencias no detectadas.
  * Si aparecen fallos en producción, el cliente confiará menos en el sistema.
* **Impacto en el proyecto:**

  * **Tiempo:** se respeta el cronograma.
  * **Costo:** se mantiene dentro del presupuesto.
  * **Calidad:** se reduce el nivel de pruebas y aumenta el riesgo operativo.
  * **Alcance:** se limita a lo esencial.

#### Opción B: Extender el plazo para asegurar calidad

* **Explicación:** el equipo negocia una extensión de 1 a 2 semanas para corregir todos los errores de inventario y hacer pruebas completas antes de entregar.
* **Ventajas:**

  * El control de existencias es más confiable.
  * Se reducen los fallos en producción y las pérdidas comerciales.
  * A largo plazo, el cliente percibe mejor la calidad del trabajo.
* **Desventajas:**

  * Se incumple la fecha acordada.
  * El cliente puede quedar insatisfecho y la relación puede deteriorarse.
  * Hay costos adicionales por horas extra o presión sobre el equipo.
* **Impacto en el proyecto:**

  * **Tiempo:** se extiende el cronograma.
  * **Costo:** aumenta el costo real del proyecto.
  * **Calidad:** mejora significativamente.
  * **Alcance:** se mantiene o se ajusta según lo negociado.



### 3.2 Trade-off 2:  Alcance vs. Tiempo

#### Opción A: Incluir las alertas automáticas en el plazo original

* **Explicación:** el equipo acepta desarrollar las alertas que pidió el cliente y las integra en las 3 semanas restantes, recortando pruebas o moviendo otras tareas.
* **Ventajas:**

  * El cliente recibe todo lo que pidió, incluida la nueva funcionalidad.
  * Se fortalece la relación comercial y la satisfacción del cliente.
  * El sistema queda más completo desde la primera entrega.
* **Desventajas:**

  * Queda menos tiempo para corregir los errores críticos de inventario.
  * Hay más riesgo de fallos por pruebas insuficientes.
  * El equipo se sobrecarga y puede desmotivarse.
* **Impacto en el proyecto:**

  * **Tiempo:** se mantiene, pero con mucha presión.
  * **Costo:** se mantiene, aunque con riesgo de horas extra no pagadas.
  * **Calidad:** disminuye por falta de pruebas.
  * **Alcance:** aumenta, pero a costa de la calidad.

#### Opción B: Posponer las alertas a una fase posterior

* **Explicación:** el equipo mantiene el alcance original acordado y negocia con el cliente implementar las alertas automáticas en una fase 2, después de una entrega estable.
* **Ventajas:**

  * Permite concentrar los esfuerzos en corregir los errores de inventario.
  * Se asegura la calidad de las funciones esenciales.
  * Se entrega un sistema estable y confiable en la fecha prevista.
* **Desventajas:**

  * El cliente no recibe todo lo que pidió en la primera entrega.
  * Puede verse como falta de flexibilidad del equipo.
  * Requiere negociar y, posiblemente, firmar un nuevo contrato o adenda.
* **Impacto en el proyecto:**

  * **Tiempo:** se respeta el cronograma original.
  * **Costo:** se mantiene dentro del presupuesto.
  * **Calidad:** mejora en las funciones esenciales.
  * **Alcance:** se reduce temporalmente, con opción de ampliarse después.



### 3.3 Trade-off 3: Costo vs. Funcionalidad

#### Opción A: Mantener el presupuesto sin personal adicional

* **Explicación:** el equipo se ajusta a los Q40,000 aprobados y a los 4 desarrolladores, redistribuyendo tareas y priorizando lo esencial.
* **Ventajas:**

  * Se respeta el presupuesto aprobado.
  * No se comprometen recursos adicionales que no estaban planificados.
  * El proyecto se mantiene sostenible en lo financiero.
* **Desventajas:**

  * Hay menos capacidad para cubrir desarrollo, corrección de errores y pruebas al mismo tiempo.
  * Hay riesgo de sobrecarga del equipo.
  * Podría ser necesario recortar alcance o calidad.
* **Impacto en el proyecto:**

  * **Tiempo:** se mantiene, pero con riesgo de retrasos por sobrecarga.
  * **Costo:** se controla estrictamente.
  * **Calidad:** puede resentirse si no se prioriza bien.
  * **Alcance:** se limita a lo esencial.

#### Opción B: Contratar apoyo externo o pagar horas extra

* **Explicación:** el equipo pide ampliar el presupuesto o contrata personal temporal para cubrir el desarrollo de las alertas y las pruebas necesarias.
* **Ventajas:**

  * Hay más capacidad para cumplir con alcance, calidad y plazo.
  * Se reduce la carga de los 4 desarrolladores actuales.
  * Se pueden atender tanto los errores como las funcionalidades nuevas.
* **Desventajas:**

  * Se excede el presupuesto aprobado de Q40,000.
  * Requiere aprobación de la dirección y, posiblemente, del cliente.
  * El personal nuevo necesita tiempo para integrarse y aprender el proyecto.
* **Impacto en el proyecto:**

  * **Tiempo:** se mantiene o mejora.
  * **Costo:** aumenta y puede salirse del presupuesto.
  * **Calidad:** mejora al tener más recursos.
  * **Alcance:** se puede cubrir completo.



## 4. Negociación técnica

### 4.1 Decisión propuesta
 
El equipo propone **entregar el sistema en la semana 8 con las funciones esenciales completas**, dando prioridad absoluta a corregir el error de ventas simultáneas y a probar a fondo inventario y ventas. Las alertas automáticas se posponen a una fase 2 mediante una adenda al contrato, sin contratar personal y sin pasar de los Q40,000.
 
Esto se traduce en una postura para cada trade-off:
 
| Trade-off | Postura del equipo | Resumen |
|---|---|---|
| 1. Rapidez vs. Calidad | Opción A, con un ajuste | Se entrega en la fecha, pero "esencial" incluye un inventario consistente. Los recortes de pruebas se hacen en módulos secundarios (por ejemplo, reportes) y nunca en inventario ni ventas. |
| 2. Alcance vs. Tiempo | Opción B | Las alertas pasan a la fase 2. |
| 3. Costo vs. Funcionalidad | Opción A | Se mantienen los Q40,000 y los 4 desarrolladores. |
 
### 4.2 Uso de evidencia
 
**Datos del propio proyecto**
 
- Han pasado 5 de las 8 semanas (62.5% del plazo) y quedan 3.
- Con 4 desarrolladores, la capacidad restante es de **12 persona-semanas**.
- El presupuesto es fijo (Q40,000) y no hay fondos adicionales para personal ni para ampliar el plazo.
**Naturaleza del error**
 
- El fallo aparece cuando dos ventas se registran casi al mismo tiempo. Es un problema de concurrencia (condición de carrera): ambas ventas leen la misma existencia antes de que la otra la actualice.
- No es un detalle visual. Afecta la función principal del sistema, que es llevar un inventario preciso, y puede causar ventas de productos que ya no hay.
- Es un problema conocido y tiene soluciones estándar, como transacciones en la base de datos o actualizaciones atómicas de las existencias. Lo que lleva tiempo es probarlo bien, porque estos errores no aparecen siempre.
**Experiencia en la industria**
 
- Según la Ley de Brooks, agregar personas a un proyecto que ya va atrasado tiende a atrasarlo más, porque el personal nuevo necesita tiempo para aprender y el equipo se coordina con más gente (Brooks, 1975). Esto va en contra de contratar apoyo externo en la semana 5.
**Estimación de esfuerzo (supuestos del equipo)**
 
| Tarea | Persona-semanas estimadas |
|---|---|
| Corregir el error de concurrencia en inventario y ventas | 3 |
| Terminar funciones pendientes | 3 |
| Pruebas (con énfasis en inventario y ventas) | 4 |
| Margen para imprevistos | 1 |
| **Total del trabajo esencial** | **11 de 12 disponibles** |
| Alertas automáticas (desarrollo y pruebas) | 2 a 3 adicionales |
 
Sumando las alertas, el trabajo llegaría a unas 13 o 14 persona-semanas, más de las 12 disponibles. Esas estimaciones son un supuesto del equipo, pero la conclusión se sostiene aun si los números cambian un poco, porque casi no queda margen.
 
### 4.3 Análisis de impacto
 
| Aspecto | Impacto de la decisión |
|---|---|
| Cronograma | Se respeta la entrega de la semana 8. Las alertas se programan en una fase 2 con fecha acordada. |
| Presupuesto | Se mantiene en Q40,000. La fase 2 se cotiza aparte. |
| Calidad | El inventario y las ventas quedan corregidos y probados. Los módulos secundarios tienen pruebas más ligeras. |
| Equipo | La carga se reparte sin necesidad de horas extra y con un pequeño margen. |
| Cliente | Recibe un sistema confiable en la fecha pactada, pero sin las alertas en la primera entrega. |
 
### 4.4 Razonamiento lógico
 
1. La capacidad restante es de 12 persona-semanas, y el trabajo esencial ocupa casi toda (unas 11).
2. Las alertas necesitan de 2 a 3 persona-semanas más, así que no caben sin recortar pruebas o dejar el error sin corregir.
3. El error de inventario afecta la función central del sistema. Si se entrega sin corregir, el sistema no cumple con su propósito, que es dar información precisa.
4. Extender el plazo incumple el compromiso con el cliente, y ampliar el equipo o el presupuesto no es viable (no hay fondos y, según Brooks, probablemente retrasaría más).
5. Por lo tanto, lo menos dañino es recortar lo que no estaba en el alcance original, las alertas, y negociar su entrega en una fase 2.
### 4.5 Posturas y acuerdos del equipo
 
<!-- Ajusten esta tabla a cómo discutieron realmente y pongan sus nombres. -->
 
| Integrante | Postura inicial | Argumento principal | Acuerdo final |
|---|---|---|---|
| _Nombre 1_ (perspectiva del cliente) | Incluir las alertas y entregar en la fecha. | El cliente espera un sistema completo y la fecha es un compromiso. | Aceptó posponer las alertas si se entrega un inventario confiable y se comunica con anticipación. |
| _Nombre 2_ (perspectiva técnica) | Extender el plazo para probar todo a fondo. | El error de concurrencia puede causar pérdidas reales y requiere pruebas serias. | Aceptó entregar en la fecha si las pruebas se concentran en inventario y ventas. |
| _Nombre 3_ (perspectiva de dirección) | Mantener presupuesto y calendario sin dañar la relación con el cliente. | No hay fondos extra y contratar gente ahora retrasaría más. | Propuso la adenda para la fase 2 como forma de conservar la relación con el cliente. |
 
---
 
## 5. Decisión final
 
### 5.1 Solución elegida
 
Entregar en la semana 8 un sistema con las cinco funciones acordadas (productos, inventario, ventas, reportes y usuarios), con el error de ventas simultáneas corregido y probado, dentro del presupuesto de Q40,000. Las alertas automáticas de stock bajo se implementarán en una fase 2, formalizada con una adenda.
 
### 5.2 Justificación
 
Es la única alternativa que respeta a la vez el plazo, el presupuesto y la calidad de lo esencial. Lo que se sacrifica es una funcionalidad que el cliente pidió después y que no estaba en el contrato, no algo que el sistema necesite para funcionar. Un sistema con inventario inconsistente generaría justo el problema que el cliente quiere evitar, así que entregarlo así tendría un costo mayor que esperar por las alertas.
 
### 5.3 Consecuencias de la decisión
 
| Tipo | Consecuencia |
|---|---|
| Positivas | Entrega a tiempo, inventario confiable, presupuesto respetado, equipo sin sobrecarga y relación con el cliente conservada. |
| Negativas / riesgos | El cliente no tendrá las alertas en la primera entrega y podría molestarse. Si el equipo se atrasa más, el margen de 1 persona-semana puede no alcanzar. |
| Plan de mitigación | Comunicar la decisión al cliente cuanto antes, con datos del error y del esfuerzo. Mientras llegan las alertas, el reporte de existencias permite consultar qué productos tienen pocas unidades. Dar una fecha concreta y una cotización para la fase 2. Hacer reuniones de avance semanales hasta la entrega. |
 
---
 
## 6. Reflexión
 
### 6.1 ¿Qué tan difícil fue tomar la decisión?
 
Fue más difícil de lo que parecía al principio, porque ninguna opción era buena del todo. Cada una resolvía una parte del problema y empeoraba otra: cumplir la fecha ponía en riesgo la calidad, y dar más tiempo dañaba la relación con el cliente. Lo que más costó fue aceptar que había que dejar algo afuera, y ahí ayudó mucho ponerle números a la capacidad del equipo y ver que las alertas simplemente no cabían.
 
### 6.2 ¿Qué aprendieron sobre trade-offs?
 
Aprendimos que casi nunca hay una opción perfecta. Un trade-off consiste en elegir qué se está dispuesto a perder, y por eso conviene comparar las opciones con criterios claros (tiempo, costo, alcance y calidad) en lugar de decidir por intuición. También vimos que los trade-offs están conectados: decidir sobre el tiempo afecta el alcance y el costo. Y notamos que no todo se puede negociar por igual, porque la calidad de la función central (el inventario) pesaba más que una función extra.
 
### 6.3 ¿Cómo aplicaron comunicación asertiva?
 
Cada uno defendió su postura sin imponerla y sin ignorar la de los demás. Usamos frases como "entiendo que la fecha es importante, pero el error de inventario nos puede costar más" y "propongo que probemos a fondo solo inventario y ventas para poder cumplir la fecha". Escuchamos las tres perspectivas (cliente, equipo técnico y dirección) antes de decidir, respaldamos los desacuerdos con datos del proyecto y no con opiniones, y buscamos un acuerdo en el que cada quien cediera algo. Además, planteamos la decisión pensando en cómo comunicársela al cliente, con transparencia y con una alternativa concreta (la fase 2).
