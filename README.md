# Ejercicio Práctico: Arquitectura de Integración Bancaria

Este repositorio contiene el documento entregable (PDF) como solución al **Ejercicio Práctico de Arquitectura de Integración**.

## 🎯 Propósito del Ejercicio

El desafío consiste en diseñar una arquitectura de integración robusta y moderna para un banco tradicional que busca modernizar su infraestructura tecnológica.

El escenario requiere la integración de:
* Un core bancario tradicional existente.
* Un nuevo core bancario digital.
* Nuevos sistemas de banca web y banca móvil.
* Plataformas de pago.
* Sistemas de gestión de riesgos y prevención de fraudes.

## 💡 La Solución Propuesta

El documento `SalgadoGabrielEjercicio.pdf` detalla una solución completa que responde a las 9 tareas solicitadas.

La arquitectura se basa en un **enfoque híbrido (multicore)**, habilitado por una **arquitectura orientada a eventos (EDA)** y un diseño **API-Led** alineado con los dominios de servicio del estándar **BIAN**.

### Pila Tecnológica Principal

La solución propuesta utiliza la siguiente pila tecnológica principal, como se especificaba en los requisitos:

* **API Gateway:** Azure API Gateway (APIM)
* **Microservicios:** Spring Boot 3 (Java)
* **Identidad y Acceso (IAM):** Keycloak
* **Observabilidad y Monitoreo:** Grafana (con Prometheus y Loki)
* **Orquestación:** Azure Kubernetes Service (AKS)
* **Mensajería:** Apache Kafka

### Puntos Clave del Diseño

* **Modelado C4:** La arquitectura se describe usando los niveles de Contexto, Contenedores y Componentes.
* **Patrón Strangler Fig:** Se utiliza para la migración gradual y de bajo riesgo del core tradicional al digital.
* **Gobierno Federado (C4E):** Se propone un modelo de gobierno para APIs y microservicios que balancea la agilidad y el control.
* **Consistencia de Datos:** Se abordan los retos del multicore mediante patrones como **Saga** y **Change Data Capture (CDC)**.
