# Informe Final de Incidente de Seguridad

**Fecha del Reporte:** 31 de diciembre de 2025
[cite_start]**Estado:** Cerrado [cite: 5]
**Analista:** [Angel Marmolejo]

## 1. Resumen Ejecutivo
[cite_start]El 28 de diciembre de 2022, la organización detectó un acceso no autorizado a información de identificación personal (PII) y financiera[cite: 3].
* [cite_start]**Impacto:** Aproximadamente 50,000 registros de clientes comprometidos[cite: 4].
* [cite_start]**Costo Estimado:** $100,000 en costos directos y pérdida de ingresos[cite: 4].
* **Gravedad:** Alta.

## 2. Cronología de Eventos
* **22-Dic-2022, 3:13 p.m. [cite_start]PT:** Recepción de un correo de extorsión solicitando $25,000 en criptomonedas[cite: 7, 9]. [cite_start]El empleado lo clasifica erróneamente como spam.
* [cite_start]**28-Dic-2022:** Segundo correo del atacante con una muestra de datos robados y una demanda aumentada a $50,000[cite: 11, 12].
* **28-Dic-2022, 7:20 p.m. [cite_start]PT:** Identificación oficial del incidente y notificación al equipo de seguridad[cite: 3, 13].
* **28-31 Dic-2022:** Investigación técnica y determinación del alcance[cite: 14].

## 3. Investigación y Análisis de Causa Raíz
La investigación en el sitio identificó una vulnerabilidad crítica en la aplicación web de comercio electrónico[cite: 16, 17].

### Vector de Ataque: Navegación Forzada (*Forced Browsing*)
* [cite_start]**Descripción:** El atacante manipuló la variable del número de orden en la URL de la página de confirmación de compra[cite: 18].
* [cite_start]**Explotación:** Esto permitió visualizar y recolectar (exfiltrar) páginas de confirmación de otros clientes de manera secuencial[cite: 19].
* **Evidencia Técnica:** Los registros de acceso al servidor (logs) mostraron un volumen inusualmente alto de solicitudes de pedidos listados secuencialmente desde una única fuente[cite: 21, 26].

## 4. Respuesta y Remediación
La organización implementó las siguientes medidas inmediatas:
1. **Comunicación:** Divulgación de la brecha de datos a los clientes en colaboración con Relaciones Públicas[cite: 23].
2. **Mitigación:** Oferta de servicios gratuitos de protección de identidad para los afectados[cite: 24].
3. **Análisis Forense:** Revisión exhaustiva de los logs del servidor para confirmar el método de ataque[cite: 25].

## 5. Recomendaciones para Prevención Futura
Para evitar la recurrencia de este tipo de incidentes, se establecen las siguientes acciones:
* [cite_start]**Escaneos de Vulnerabilidades:** Realizar pruebas de penetración y escaneos rutinarios de forma obligatoria[cite: 29].
* **Control de Acceso:**
    * [cite_start]Implementar *allowlisting* para restringir el acceso solo a rangos de URL autorizados[cite: 31].
    * Asegurar que todo el contenido sensible requiera autenticación de usuario previa[cite: 32].
