# Guía de Inicio Rápido - Git-MedUC

Esta guía te ayudará a comenzar rápidamente con Git-MedUC, ya sea que quieras proponer un nuevo proyecto, contribuir a uno existente, o simplemente entender cómo funciona nuestra organización.

## 🎯 ¿Qué quieres hacer?

### 1️⃣ Proponer un Nuevo Proyecto

**Pasos rápidos**:
1. Lee el [README.md](../README.md) para entender los principios de Git-MedUC
2. Usa la [plantilla de propuesta de proyecto](../templates/project-template/PROJECT_PROPOSAL.md)
3. Completa todas las secciones, especialmente:
   - Contexto médico/clínico
   - Base científica
   - Validación médica planificada
   - Consideraciones éticas
4. Crea un issue en este repositorio con tu propuesta
5. Espera feedback del Comité Directivo y Técnico

**Documentos a revisar**:
- ✅ [README.md](../README.md) - Visión general
- ✅ [GOVERNANCE.md](../GOVERNANCE.md) - Proceso de aprobación (Sección 5)
- ✅ [PROJECT_PROPOSAL.md](../templates/project-template/PROJECT_PROPOSAL.md) - Plantilla

### 2️⃣ Contribuir a un Proyecto Existente

**Pasos rápidos**:
1. Lee el [Código de Conducta](../CODE_OF_CONDUCT.md)
2. Revisa los [Lineamientos de Contribución](../CONTRIBUTING.md)
3. Busca issues etiquetados como `good-first-issue` o `help-wanted`
4. Comenta en el issue que quieres trabajar en él
5. Sigue el [flujo de trabajo](WORKFLOW.md) para hacer tu contribución

**Documentos a revisar**:
- ✅ [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md)
- ✅ [CONTRIBUTING.md](../CONTRIBUTING.md)
- ✅ [WORKFLOW.md](WORKFLOW.md) - Sección "Desarrollo"

### 3️⃣ Reportar un Bug

**Pasos rápidos**:
1. Busca si el bug ya fue reportado
2. Si no existe, usa la [plantilla de bug report](../templates/issue-templates/bug_report.md)
3. Completa toda la información solicitada
4. Si es un bug médico/clínico, marca su severidad claramente
5. Crea el issue

**Documentos a revisar**:
- ✅ [bug_report.md](../templates/issue-templates/bug_report.md) - Plantilla

### 4️⃣ Proponer una Nueva Funcionalidad

**Pasos rápidos**:
1. Busca si la funcionalidad ya fue propuesta
2. Si no existe, usa la [plantilla de feature request](../templates/issue-templates/feature_request.md)
3. Completa el contexto médico/clínico
4. Explica el impacto esperado
5. Considera aspectos éticos
6. Crea el issue

**Documentos a revisar**:
- ✅ [feature_request.md](../templates/issue-templates/feature_request.md) - Plantilla

### 5️⃣ Solicitar Validación Médica

**Pasos rápidos**:
1. Usa la [plantilla de validación médica](../templates/issue-templates/medical_validation.md)
2. Proporciona base científica completa
3. Define protocolo de validación
4. Considera aspectos éticos
5. Crea el issue
6. Espera asignación de revisor médico

**Documentos a revisar**:
- ✅ [medical_validation.md](../templates/issue-templates/medical_validation.md) - Plantilla
- ✅ [GOVERNANCE.md](../GOVERNANCE.md) - Comité de Ética (Sección 2.3)

### 6️⃣ Hacer un Pull Request

**Pasos rápidos**:
1. Asegúrate de que tu código sigue los estándares
2. Ejecuta todos los tests
3. Actualiza la documentación
4. Usa la [plantilla de PR](../templates/pull-request-template/PULL_REQUEST_TEMPLATE.md)
5. Completa todos los checklists
6. Crea el PR

**Documentos a revisar**:
- ✅ [PULL_REQUEST_TEMPLATE.md](../templates/pull-request-template/PULL_REQUEST_TEMPLATE.md) - Plantilla
- ✅ [CONTRIBUTING.md](../CONTRIBUTING.md) - Estándares de código
- ✅ [WORKFLOW.md](WORKFLOW.md) - Proceso de PR

## 📚 Mapa de Documentación

### Para Nuevos Colaboradores
```
1. README.md
   ↓
2. CODE_OF_CONDUCT.md
   ↓
3. CONTRIBUTING.md
   ↓
4. WORKFLOW.md
```

### Para Líderes de Proyecto
```
1. README.md
   ↓
2. GOVERNANCE.md
   ↓
3. PROJECT_PROPOSAL.md
   ↓
4. WORKFLOW.md (sección Release)
```

### Para Revisores Médicos
```
1. GOVERNANCE.md (Sección 2.3)
   ↓
2. medical_validation.md
   ↓
3. CONTRIBUTING.md (Consideraciones Médicas)
```

## 🔑 Conceptos Clave

### Gobernanza
- **Qué es**: Estructura organizacional y proceso de toma de decisiones
- **Dónde encontrar**: [GOVERNANCE.md](../GOVERNANCE.md)
- **Cuándo necesito**: Al proponer proyectos, entender jerarquía

### Lineamientos de Contribución
- **Qué es**: Cómo contribuir código, documentación, y validación
- **Dónde encontrar**: [CONTRIBUTING.md](../CONTRIBUTING.md)
- **Cuándo necesito**: Antes de hacer cualquier contribución

### Flujo de Trabajo
- **Qué es**: Proceso detallado de desarrollo, desde idea hasta deployment
- **Dónde encontrar**: [docs/WORKFLOW.md](WORKFLOW.md)
- **Cuándo necesito**: Durante desarrollo activo

### Validación Médica
- **Qué es**: Proceso para validar que las soluciones son médicamente correctas
- **Dónde encontrar**: 
  - [GOVERNANCE.md](../GOVERNANCE.md) - Sección 2.3
  - [medical_validation.md](../templates/issue-templates/medical_validation.md)
  - [CONTRIBUTING.md](../CONTRIBUTING.md) - Sección Consideraciones Médicas
- **Cuándo necesito**: Para funcionalidades con aplicación clínica

## ⚡ Comandos Rápidos

### Configurar Entorno
```bash
# Clonar repo
git clone https://github.com/Git-MedUC/[nombre-proyecto].git
cd [nombre-proyecto]

# Instalar dependencias (ejemplo Python)
pip install -r requirements.txt

# Ejecutar tests
pytest
```

### Crear Branch de Feature
```bash
git checkout -b feature/mi-funcionalidad
```

### Hacer Commit
```bash
git add .
git commit -m "feat: Descripción breve del cambio"
```

### Crear PR
```bash
git push origin feature/mi-funcionalidad
# Luego ir a GitHub y crear PR con la plantilla
```

## ❓ Preguntas Frecuentes

### ¿Dónde empiezo si soy nuevo?
1. Lee el [README.md](../README.md)
2. Revisa el [Código de Conducta](../CODE_OF_CONDUCT.md)
3. Busca issues con etiqueta `good-first-issue`
4. Comenta que quieres trabajar en uno

### ¿Cómo propongo un proyecto?
Usa la [plantilla de propuesta](../templates/project-template/PROJECT_PROPOSAL.md) y créala como issue.

### ¿Todos los proyectos necesitan validación médica?
Solo aquellos con aplicación clínica directa. Para duda, consulta en el issue.

### ¿Puedo contribuir si no soy médico?
¡Absolutamente! Valoramos contribuciones técnicas, de diseño, documentación, etc. Solo asegúrate de consultar con el equipo médico para funcionalidades clínicas.

### ¿Cómo se manejan los datos de pacientes?
Nunca incluyas datos reales de pacientes. Siempre usa datos sintéticos o anonimizados. Ver [CONTRIBUTING.md](../CONTRIBUTING.md) sección Privacidad y Seguridad.

### ¿Qué licencia usamos?
Por defecto MIT License. Ver [GOVERNANCE.md](../GOVERNANCE.md) sección 6.1.

## 📞 ¿Necesitas Ayuda?

- **Issues**: Reporta problemas o pregunta
- **Discussions**: Para discusiones generales
- **Comités**: Ver [GOVERNANCE.md](../GOVERNANCE.md) para contactos

## ✅ Checklist para Tu Primera Contribución

- [ ] He leído el README.md
- [ ] He leído y acepto el CODE_OF_CONDUCT.md
- [ ] He leído CONTRIBUTING.md
- [ ] He encontrado un issue para trabajar o creé uno nuevo
- [ ] He comentado en el issue que voy a trabajar en él
- [ ] He creado mi branch de feature
- [ ] He hecho mis cambios siguiendo los estándares
- [ ] He escrito tests
- [ ] He actualizado la documentación
- [ ] Todos los tests pasan
- [ ] He creado mi PR usando la plantilla
- [ ] He solicitado review

---

**¡Bienvenido a Git-MedUC!** Estamos emocionados de tenerte en nuestro equipo.
