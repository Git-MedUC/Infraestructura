# Lineamientos de Contribución - Git-MedUC

¡Gracias por tu interés en contribuir a Git-MedUC! Este documento proporciona lineamientos para contribuir efectivamente a nuestros proyectos.

## Tabla de Contenidos
- [Código de Conducta](#código-de-conducta)
- [Cómo Empezar](#cómo-empezar)
- [Proceso de Contribución](#proceso-de-contribución)
- [Estándares de Código](#estándares-de-código)
- [Estándares de Documentación](#estándares-de-documentación)
- [Proceso de Revisión](#proceso-de-revisión)
- [Consideraciones Médicas y Éticas](#consideraciones-médicas-y-éticas)

## Código de Conducta

Este proyecto adhiere a un Código de Conducta. Al participar, se espera que mantengas este código. Por favor, reporta comportamientos inaceptables a los mantenedores del proyecto.

## Cómo Empezar

### 1. Familiarízate con el Proyecto
- Lee el README.md del repositorio
- Revisa la documentación existente
- Explora issues abiertos etiquetados como `good first issue` o `help wanted`
- Lee el documento de GOVERNANCE.md para entender la estructura organizacional

### 2. Configura tu Entorno de Desarrollo
- Haz fork del repositorio
- Clona tu fork localmente
- Configura el repositorio upstream
- Instala las dependencias necesarias según el README del proyecto específico

```bash
git clone https://github.com/TU-USUARIO/nombre-del-repo.git
cd nombre-del-repo
git remote add upstream https://github.com/Git-MedUC/nombre-del-repo.git
```

### 3. Mantén tu Fork Actualizado
```bash
git fetch upstream
git checkout main
git merge upstream/main
```

## Proceso de Contribución

### 1. Identifica o Crea un Issue

Antes de comenzar a trabajar:
- Busca issues existentes relacionados
- Si no existe, crea un nuevo issue describiendo:
  - El problema o mejora propuesta
  - Contexto médico relevante (si aplica)
  - Solución propuesta
  - Impacto esperado

### 2. Discute la Solución

Para cambios significativos:
- Comenta en el issue tu enfoque propuesto
- Espera feedback de los mantenedores
- Para cambios arquitectónicos, puede requerirse un RFC (Request for Comments)

### 3. Trabaja en una Rama

```bash
git checkout -b feature/descripcion-breve
# o
git checkout -b fix/descripcion-del-bug
```

Convenciones de nombres de ramas:
- `feature/` - nuevas funcionalidades
- `fix/` - corrección de bugs
- `docs/` - cambios en documentación
- `refactor/` - refactorización de código
- `test/` - adición o mejora de tests
- `medical-validation/` - validaciones médicas

### 4. Desarrolla tu Contribución

#### Commits
Usa mensajes de commit claros y descriptivos:

```
tipo: Descripción breve (máx 50 caracteres)

Descripción más detallada si es necesaria (máx 72 caracteres por línea)

- Punto adicional 1
- Punto adicional 2

Refs: #123
```

Tipos de commit:
- `feat`: Nueva funcionalidad
- `fix`: Corrección de bug
- `docs`: Cambios en documentación
- `style`: Formato, punto y coma faltantes, etc.
- `refactor`: Refactorización de código
- `test`: Adición o corrección de tests
- `chore`: Mantenimiento, configuración
- `medical`: Validaciones o cambios médicos

Ejemplos:
```
feat: Agregar detección de riesgo suicida en análisis de texto

Implementa modelo basado en transformers para identificar señales
de riesgo suicida en texto libre de pacientes.

- Integración con modelo BERT fine-tuned
- Validación médica pendiente
- Tests unitarios incluidos

Refs: #45
```

```
fix: Corregir cálculo de score GAD-7

El cálculo previo no consideraba items invertidos correctamente.
Ahora sigue el protocolo estándar del GAD-7.

Refs: #78
```

### 5. Tests

- Escribe tests para nuevas funcionalidades
- Asegura que todos los tests pasen antes de enviar PR
- Incluye tests unitarios y de integración según sea apropiado
- Para funcionalidades médicas, incluye casos de validación clínica

```bash
# Ejecuta tests
npm test
# o
python -m pytest
```

### 6. Documentación

Actualiza la documentación según sea necesario:
- Docstrings en el código
- README.md si cambias funcionalidad principal
- Archivos en `/docs` si aplica
- Comentarios en código complejo
- Ejemplos de uso para nuevas funcionalidades

### 7. Crea un Pull Request

#### Antes de Enviar
- [ ] Todos los tests pasan
- [ ] El código sigue los estándares del proyecto
- [ ] La documentación está actualizada
- [ ] Los commits están bien formateados
- [ ] No hay conflictos con la rama main

#### Contenido del PR
Usa la plantilla de PR y proporciona:
- Descripción clara del cambio
- Referencia a issue(s) relacionado(s)
- Tipo de cambio (bugfix, feature, breaking change, etc.)
- Checklist de validación
- Screenshots si hay cambios visuales
- Validación médica si aplica

### 8. Proceso de Revisión

- Un reviewer será asignado automáticamente
- Responde a comentarios y feedback constructivamente
- Realiza cambios solicitados
- Empuja cambios adicionales al mismo branch
- El PR será merged cuando reciba aprobación

## Estándares de Código

### General
- Código limpio y legible
- Nombres descriptivos para variables y funciones
- Evitar duplicación (DRY principle)
- Funciones pequeñas y con una sola responsabilidad
- Comentarios solo cuando sea necesario para explicar "por qué", no "qué"

### Python
```python
# Seguir PEP 8
# Usar type hints
def calcular_score_phq9(respuestas: List[int]) -> Dict[str, Any]:
    """
    Calcula el score del PHQ-9 para depresión.
    
    Args:
        respuestas: Lista de 9 respuestas (0-3 cada una)
        
    Returns:
        Dict con score total y nivel de severidad
        
    Raises:
        ValueError: Si las respuestas no son válidas
    """
    if len(respuestas) != 9:
        raise ValueError("PHQ-9 requiere exactamente 9 respuestas")
    
    score = sum(respuestas)
    return {
        'score': score,
        'severidad': _clasificar_severidad_phq9(score)
    }
```

### JavaScript/TypeScript
```javascript
// Usar TypeScript cuando sea posible
// Seguir Airbnb Style Guide

/**
 * Procesa respuestas del GAD-7 para ansiedad
 * @param {number[]} respuestas - Array de 7 respuestas (0-3)
 * @returns {Object} Score y clasificación
 */
function procesarGAD7(respuestas) {
  if (respuestas.length !== 7) {
    throw new Error('GAD-7 requiere exactamente 7 respuestas');
  }
  
  const score = respuestas.reduce((sum, r) => sum + r, 0);
  return {
    score,
    clasificacion: clasificarAnsiedadGAD7(score)
  };
}
```

### R
```r
# Seguir tidyverse style guide
# Documentar con roxygen2

#' Calcular Score de Escala de Hamilton para Depresión
#'
#' @param respuestas Numeric vector con respuestas del HAM-D
#' @return Lista con score y clasificación
#' @export
calcular_hamd <- function(respuestas) {
  if (length(respuestas) != 17) {
    stop("HAM-D-17 requiere 17 items")
  }
  
  score <- sum(respuestas)
  list(
    score = score,
    severidad = clasificar_hamd(score)
  )
}
```

## Estándares de Documentación

### README.md de Proyectos
Cada proyecto debe incluir:
- Título y descripción breve
- Contexto médico y propósito clínico
- Instalación y requisitos
- Uso y ejemplos
- Validación médica (si aplica)
- Limitaciones conocidas
- Licencia
- Cómo contribuir
- Contacto

### Documentación Médica
Para herramientas con aplicación clínica:
- Base científica (referencias a literatura)
- Población objetivo
- Casos de uso apropiados
- Limitaciones y contraindicaciones
- Advertencias importantes
- Validaciones realizadas

### Comentarios en Código
```python
# BUENO: Explica el "por qué"
# Usamos ventana de 5 días porque estudios muestran que síntomas
# de depresión son más estables en este período (Smith et al., 2020)
ventana_temporal = 5

# MALO: Explica el "qué" (obvio)
# Asigna 5 a ventana_temporal
ventana_temporal = 5
```

## Proceso de Revisión

### Para Revisores
- Sé respetuoso y constructivo
- Explica el razonamiento detrás de comentarios
- Distingue entre "debe cambiar" y "sugerencia"
- Aprueba cuando el código cumple estándares, aunque podrías hacerlo diferente
- Para cambios médicos, solicita validación del Comité Médico

### Para Autores
- Responde a todos los comentarios
- Pregunta si algo no está claro
- Mantén la mente abierta al feedback
- No tomes comentarios como personales
- Explica tu razonamiento si discrepas

## Consideraciones Médicas y Éticas

### Validación Médica
Contribuciones que afecten funcionalidad clínica requieren:
- Revisión por al menos un médico del equipo
- Referencias a literatura científica
- Documentación de limitaciones
- Aprobación del Comité de Ética y Validación Médica

### Privacidad y Seguridad
- NUNCA incluir datos reales de pacientes en código o tests
- Usar datos sintéticos o anonimizados para ejemplos
- Implementar medidas de seguridad apropiadas
- Seguir regulaciones aplicables (HIPAA, GDPR, etc.)

### Sesgos
- Considerar impacto en diferentes poblaciones
- Documentar sesgos conocidos
- Implementar tests de equidad cuando sea posible
- Buscar revisar con perspectivas diversas

### Responsabilidad
- Ser explícito sobre limitaciones
- No hacer afirmaciones médicas sin respaldo
- Documentar casos de uso apropiados e inapropiados
- Incluir disclaimers apropiados

## Tipos de Contribuciones Bienvenidas

### Código
- Nuevas funcionalidades
- Corrección de bugs
- Mejoras de performance
- Refactorización
- Tests adicionales

### Documentación
- Mejoras a README
- Tutoriales y guías
- Documentación de API
- Traducciones
- Ejemplos de uso

### Validación Médica
- Revisión de protocolos clínicos
- Validación de algoritmos
- Referencias bibliográficas
- Casos de uso clínicos

### Diseño y UX
- Mejoras de interfaz
- Diseño de experiencia de usuario
- Accesibilidad

### Investigación
- Propuestas de nuevos proyectos
- Análisis de necesidades clínicas
- Revisiones de literatura

## Preguntas y Soporte

Si tienes preguntas:
1. Revisa documentación existente y FAQs
2. Busca en issues cerrados
3. Pregunta en GitHub Discussions
4. Contacta a los mantenedores

## Reconocimiento

Valoramos todas las contribuciones. Los contribuidores serán:
- Listados en CONTRIBUTORS.md
- Reconocidos en releases notes
- Mencionados en publicaciones académicas cuando sea apropiado

## Licencia

Al contribuir, aceptas que tus contribuciones serán licenciadas bajo la misma licencia del proyecto (típicamente MIT License, ver LICENSE).

---

¡Gracias por contribuir a Git-MedUC y ayudarnos a mejorar la salud mental a través de la tecnología!
