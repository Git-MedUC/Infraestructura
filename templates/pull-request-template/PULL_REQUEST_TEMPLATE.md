# Pull Request

## Descripción
[Proporciona una descripción concisa de los cambios realizados]

## Tipo de Cambio
<!-- Marca con "x" el tipo de cambio que corresponda -->
- [ ] Bug fix (cambio no disruptivo que corrige un issue)
- [ ] Nueva funcionalidad (cambio no disruptivo que agrega funcionalidad)
- [ ] Breaking change (fix o feature que causaría que funcionalidad existente no funcione como se espera)
- [ ] Cambio de documentación
- [ ] Refactorización (sin cambios funcionales)
- [ ] Mejora de performance
- [ ] Cambio en tests
- [ ] Validación médica

## Issues Relacionados
<!-- Referencia issues relacionados usando #número -->
Fixes #(issue)
Relates to #(issue)

## Contexto Médico (si aplica)
### Impacto Clínico
- [ ] Este cambio afecta funcionalidad clínica
- [ ] Este cambio ha sido validado médicamente
- [ ] Este cambio requiere validación médica adicional

### Descripción del Impacto
[Si aplica, describe cómo este cambio impacta el uso clínico]

### Validación Médica
- Revisado por: [nombre del médico revisor o N/A]
- Referencias: [citas científicas que respaldan el cambio]
- Limitaciones: [limitaciones conocidas del cambio]

## Cambios Realizados
<!-- Lista los cambios principales realizados -->
- [Cambio 1]
- [Cambio 2]
- [Cambio 3]

## Cómo se ha Probado
<!-- Describe las pruebas que ejecutaste para verificar tus cambios -->
### Tests Ejecutados
- [ ] Tests unitarios
- [ ] Tests de integración
- [ ] Tests end-to-end
- [ ] Tests manuales
- [ ] Validación médica/clínica

### Descripción de Tests
[Describe los escenarios de prueba y resultados]

### Configuración de Tests
- OS: [e.g. Ubuntu 20.04]
- Versión: [e.g. Python 3.9]
- Entorno: [desarrollo/staging/producción]

## Screenshots (si aplica)
<!-- Si hay cambios visuales, incluye screenshots de antes y después -->
### Antes
[Screenshot o N/A]

### Después
[Screenshot o N/A]

## Checklist de Revisión
<!-- Marca con "x" cuando hayas completado cada item -->

### General
- [ ] Mi código sigue los estándares de estilo de este proyecto
- [ ] He realizado una auto-revisión de mi código
- [ ] He comentado mi código, particularmente en áreas difíciles de entender
- [ ] He realizado los cambios correspondientes en la documentación
- [ ] Mis cambios no generan nuevas advertencias
- [ ] No hay conflictos con la rama base

### Tests
- [ ] He agregado tests que prueban que mi fix es efectivo o que mi feature funciona
- [ ] Tests unitarios nuevos y existentes pasan localmente con mis cambios
- [ ] Tests de integración pasan (si aplica)
- [ ] He verificado que no rompo tests existentes

### Documentación
- [ ] He actualizado el README si es necesario
- [ ] He actualizado docstrings/comentarios de funciones modificadas
- [ ] He actualizado la documentación técnica si es necesario
- [ ] He documentado limitaciones conocidas

### Código
- [ ] He eliminado código comentado o debug statements
- [ ] He eliminado imports no utilizados
- [ ] He seguido principios DRY (Don't Repeat Yourself)
- [ ] Las funciones tienen una sola responsabilidad
- [ ] He considerado casos edge y manejo de errores

### Seguridad y Privacidad (si aplica)
- [ ] No he incluido datos sensibles o de pacientes reales
- [ ] He implementado validación de inputs apropiada
- [ ] He considerado implicaciones de seguridad
- [ ] He seguido mejores prácticas de manejo de datos sensibles
- [ ] He considerado HIPAA/GDPR si aplica

### Consideraciones Médicas (si aplica)
- [ ] He consultado con un profesional médico si era necesario
- [ ] He incluido referencias científicas apropiadas
- [ ] He documentado casos de uso apropiados
- [ ] He documentado limitaciones y contraindicaciones
- [ ] He considerado sesgos potenciales

## Cambios Disruptivos (Breaking Changes)
<!-- Si hay breaking changes, descríbelos en detalle -->
- [ ] Este PR introduce breaking changes
- Descripción de breaking changes: [descripción o N/A]
- Plan de migración: [descripción o N/A]

## Dependencias
<!-- Lista cualquier nueva dependencia agregada o actualizada -->
- Nueva dependencia: [nombre y versión]
- Dependencia actualizada: [nombre, versión anterior → nueva versión]
- Justificación: [por qué es necesaria]

## Deployment Notes
<!-- Notas especiales para deployment -->
- [ ] Requiere cambios en configuración
- [ ] Requiere migración de base de datos
- [ ] Requiere actualización de dependencias
- [ ] Requiere variables de entorno nuevas
- Notas adicionales: [descripción o N/A]

## Revisores Sugeridos
<!-- Menciona a revisores específicos si es apropiado -->
- Técnico: @[username]
- Médico: @[username]
- Otro: @[username]

## Información Adicional
<!-- Cualquier información adicional que los revisores deban conocer -->
[Información adicional o N/A]

---

## Para Revisores
### Checklist del Revisor
- [ ] El código es legible y está bien estructurado
- [ ] Los tests son apropiados y completos
- [ ] La documentación es clara y completa
- [ ] No hay problemas evidentes de seguridad
- [ ] El impacto médico ha sido considerado apropiadamente
- [ ] Los cambios son apropiados para el objetivo del PR
- [ ] No hay cambios innecesarios o fuera de alcance

### Feedback
[Área para comentarios del revisor]
