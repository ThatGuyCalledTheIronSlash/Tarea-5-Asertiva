# Tarea #5: Análisis de Trade-offs en un Proyecto de Software

**Universidad de San Carlos de Guatemala**
Facultad de Ingeniería, Escuela de Ciencias y Sistemas
Laboratorio de Comunicación Asertiva, Sección A, Segundo Semestre 2026

## Integrantes

|Nombre|Carnet|
|-|-|
|*Nombre 1*|*Carnet*|
|*Nombre 2*|*Carnet*|
|David Antonio Meza Silva|202500708|



## 1\. Planteamiento del problema

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

\---

## 2\. Identificación de trade-offs

<!-- Mínimo 3, todos relacionados con el problema planteado. -->

|Trade-Off|Opción A|Opción B|
|-|-|-|
|*Rapidez vs calidad*|*Entregar rápido con pruebas mínimas*|*Extender el plazo para pruebas completas*|
|*Costo vs funcionalidad*|*Recortar funcionalidades para ahorrar*|*Mantener todas y aumentar el presupuesto*|
|*Simplicidad vs escalabilidad*|*Arquitectura simple (monolito)*|*Arquitectura escalable (microservicios)*|

\---

## 3\. Análisis de alternativas

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



## 4\. Negociación técnica

<!-- Aquí se simula la discusión del equipo. Defiendan una decisión con argumentos técnicos, no con opiniones. -->

### 4.1 Decisión propuesta

*Qué decide el equipo y por qué esa y no la alternativa.*

### 4.2 Uso de evidencia

<!-- Datos, métricas, casos reales, documentación, estadísticas, experiencias previas del equipo. -->

* *Evidencia 1: dato o referencia concreta*
* *Evidencia 2: ...*

### 4.3 Análisis de impacto

|Aspecto|Impacto de la decisión|
|-|-|
|Cronograma|*...*|
|Presupuesto|*...*|
|Calidad|*...*|
|Equipo|*...*|
|Cliente|*...*|

### 4.4 Razonamiento lógico

<!-- Pasos del argumento: si pasa X, entonces Y, por lo tanto Z. -->

1. *Premisa 1*
2. *Premisa 2*
3. *Conclusión*

### 4.5 Posturas y acuerdos del equipo

<!-- Opcional pero suma: muestra cómo usaron comunicación asertiva al negociar. -->

|Integrante|Postura inicial|Argumento principal|Acuerdo final|
|-|-|-|-|
|*Nombre 1*|*...*|*...*|*...*|
|*Nombre 2*|*...*|*...*|*...*|
|*Nombre 3*|*...*|*...*|*...*|

\---

## 5\. Decisión final

### 5.1 Solución elegida

*Resumen claro de lo que se hará.*

### 5.2 Justificación

*Por qué es la mejor opción dadas las restricciones.*

### 5.3 Consecuencias de la decisión

|Tipo|Consecuencia|
|-|-|
|Positivas|*...*|
|Negativas / riesgos|*...*|
|Plan de mitigación|*...*|

\---

## 6\. Reflexión

### 6.1 ¿Qué tan difícil fue tomar la decisión?

*Respuesta del equipo.*

### 6.2 ¿Qué aprendieron sobre trade-offs?

*Respuesta del equipo.*

### 6.3 ¿Cómo aplicaron comunicación asertiva?

*Respuesta del equipo. Den ejemplos concretos de cómo expresaron desacuerdos, escucharon al resto y llegaron a acuerdos.*

\---

## Referencias

<!-- Si usaron fuentes para la evidencia. -->

* *Fuente 1*

