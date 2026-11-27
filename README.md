**1- Enunciado**: 

Auditor de Logs y Guardrails para Prompts de IA Generativa
Nivel: Intermedio
OBJETIVO DE NEGOCIO
Supervisar el funcionamiento de un asistente de IA en producción para garantizar respuestas rápidas,
satisfactorias y libres de fugas de información confidencial.
QUÉ DEBE HACER TU CÓDIGO (GUÍA DE TRABAJO)
Detectar riesgos de seguridad (Guardrails): Revisar el texto de cada respuesta buscando si contiene alguna
de las palabras_prohibidas (sin importar si están en mayúsculas o minúsculas) y marcar esos
registros como alerta de seguridad.
Evaluar rendimiento técnico: Identificar qué interacciones superaron el tiempo máximo de respuesta
permitido (3.0 segundos) y calcular el consumo total y promedio de tokens.
Medir satisfacción: Calcular el porcentaje de feedback positivo por categoría de consulta, ignorando los
casos donde el usuario no dejó valoración (None)
