# NodoSkill

Plataforma B2B2C que transforma aportaciones corporativas en acceso verificable a cursos y certificaciones para estudiantes.

NodoSkill conecta empresas, instituciones educativas y estudiantes mediante un ecosistema cerrado de **SkillCredits**. Las empresas pueden medir el impacto de sus aportaciones, las escuelas validan a sus estudiantes y los beneficiarios utilizan los créditos exclusivamente dentro de un marketplace educativo.

## Demo frontend

Este repositorio contiene un prototipo funcional del portal corporativo. Utiliza datos simulados y no requiere backend, base de datos ni instalación de dependencias.

La demo permite:

- Consultar métricas de aportaciones, estudiantes y certificaciones.
- Revisar la trazabilidad agregada de los fondos.
- Explorar estudiantes, instituciones y progreso académico.
- Buscar y filtrar cursos del marketplace.
- Asignar cursos y descontar SkillCredits del saldo disponible.
- Registrar aportaciones corporativas simuladas.
- Consultar comprobantes fiscales y certificados de impacto.
- Navegar desde computadoras, tabletas y dispositivos móviles.

## Ejecución

La opción más sencilla es abrir `index.html` directamente en un navegador moderno.

También puede utilizarse un servidor local:

```bash
npx serve .
```

Después, abre la dirección indicada por el servidor, normalmente `http://localhost:3000`.

> La demo carga las tipografías DM Sans y Manrope desde Google Fonts. Si no hay conexión a internet, utilizará la tipografía alternativa del sistema.

## Recorrido sugerido

1. En **Resumen**, revisa los principales indicadores y la distribución de habilidades.
2. En **Impacto**, consulta cómo avanzan los recursos desde la aportación hasta el logro verificado.
3. En **Estudiantes**, utiliza el buscador y filtra por estado.
4. En **Marketplace**, selecciona una categoría y asigna un curso a un estudiante.
5. Comprueba que el saldo de SkillCredits disminuye después de la asignación.
6. En **Aportaciones**, registra una nueva aportación simulada.
7. Consulta el nuevo movimiento y su documentación en **Comprobantes**.

## Módulos

| Módulo | Función |
| --- | --- |
| Resumen | Vista ejecutiva con KPIs, gráficas y actividad reciente. |
| Impacto | Indicadores de activación, finalización y trazabilidad de fondos. |
| Estudiantes | Búsqueda, filtrado y seguimiento anonimizado de beneficiarios. |
| Marketplace | Catálogo de cursos y asignación mediante SkillCredits. |
| Aportaciones | Registro simulado e historial de aportaciones corporativas. |
| Comprobantes | Consulta simulada de CFDI y certificados de impacto. |

## Estructura

```text
NodoSkill/
├── index.html   # Estructura base y navegación
├── styles.css   # Sistema visual y diseño responsive
├── app.js       # Vistas, datos mock e interacciones
└── README.md    # Documentación del proyecto
```

## Datos y persistencia

Todos los datos son mocks definidos en `app.js`. Las operaciones modifican el estado únicamente durante la sesión actual del navegador. Al recargar la página se restauran los valores iniciales.

No se procesan pagos, no se generan documentos fiscales reales y no se envía información a servicios externos.

## Concepto de producto

### Problema

- Los estudiantes carecen de liquidez para pagar formación extracurricular.
- Las empresas tienen poca visibilidad sobre el impacto real de sus donaciones.
- Las alternativas tradicionales suelen tener procesos lentos y trazabilidad limitada.

### Propuesta de valor

Para empresas:

> Transformamos tus obligaciones fiscales en habilidades medibles, con trazabilidad peso por peso.

Para estudiantes:

> Una billetera educativa que financia cursos y certificaciones por ser estudiante activo.

### Modelo operativo

1. Una empresa realiza una aportación.
2. NodoSkill convierte los recursos disponibles en SkillCredits.
3. Una institución valida que el beneficiario sea estudiante activo.
4. El estudiante o administrador selecciona formación dentro del marketplace.
5. NodoSkill paga al aliado educativo y descuenta los créditos utilizados.
6. La empresa consulta resultados agregados y verificables.

## Consideraciones para producción

El prototipo cubre exclusivamente la experiencia frontend. Una implementación productiva requeriría:

- Autenticación y permisos para empresas, escuelas y estudiantes.
- API y base de datos con auditoría de movimientos.
- Integración segura con sistemas escolares.
- Conexión con aliados educativos y proveedores de pago.
- Generación y validación de CFDI.
- Protección de datos personales y consentimiento informado.
- Alianza con una Donataria Autorizada o estructura fiscal equivalente.
- Pruebas automatizadas, monitoreo y controles de ciberseguridad.

## Tecnologías

- HTML5
- CSS3
- JavaScript sin frameworks
- Google Fonts

## Estado

Prototipo navegable para validación de concepto, presentaciones y pruebas de experiencia de usuario. No representa una plataforma fiscal o financiera operativa.

## Licencia

Antes de publicar el repositorio, define la licencia adecuada para el proyecto. Para código abierto permisivo puede considerarse MIT; si el proyecto será privado o comercial, conviene mantener los derechos reservados hasta definir la estrategia legal.
