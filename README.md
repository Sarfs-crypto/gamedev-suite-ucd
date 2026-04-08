# Gamedev Suite – Diagrama de Casos de Uso

**Autor: Santiago Jose Morales
**Fecha: 7 Abril 2026  

## Descripción del Proyecto

Gamedev Suite es un sistema integral de gestión para la industria de desarrollo de videojuegos, diseñado para empresas como *Mundos Virtuales S.A.* Cubre desde la planificación de tareas, control de calidad (bugs, testeo), gestión de assets gráficos, versiones de prueba, hasta la publicación en distribuidoras digitales (Steam, Epic Games Store) y análisis de ROI.

## Estructura Modular

El sistema se compone de dos módulos principales:

### 1. Módulo de Autenticación y Control de Acceso (RBAC)
- Registro y gestión de usuarios
- Inicio de sesión con autenticación en dos pasos (opcional)
- Control de acceso basado en roles (Administrador, Productor, Líder Técnico, Desarrollador, Tester, Artista)
- Auditoría completa de acciones críticas

### 2. Módulo de Gestión de Desarrollo (Core)
- Gestión de tareas de desarrollo (CRUD, dependencias, avance)
- Reporte y seguimiento de bugs (severidad, prioridad, notificaciones)
- Gestión de assets gráficos (versiones, aprobaciones)
- Organización de código fuente por módulos
- Generación de versiones de prueba
- Procesos de testeo (funcional, rendimiento, compatibilidad)
- Publicación en distribuidoras digitales
- Dashboards y reportes de calidad, productividad y rentabilidad

## Actores del Sistema

| Actor | Tipo | Responsabilidad |
|-------|------|----------------|
| Administrador | Primario | Configuración global, usuarios, respaldos |
| Productor | Primario | Planificación, recursos, reportes ejecutivos |
| Líder Técnico | Primario | Código, versiones, compilaciones |
| Desarrollador | Primario | Tareas, código, bugs |
| Tester | Primario | Bugs, testeo, verificación |
| Artista | Primario | Assets gráficos |
| Cliente/Inversor | Primario | Reportes, KPIs |
| Distribuidora | Secundario | API de precios, versiones |
| Usuario Final | Secundario | Perfil, juegos |
| Git | Secundario | Control de versiones |

## Relaciones UML Destacadas

- `<<include>>` – Reportar bug siempre requiere verificar credenciales
- `<<include>>` – Generar versión de prueba siempre requiere validar compilación
- `<<extend>>` – Devolver asset puede extender notificación al artista (si es rechazado)
- `<<extend>>` – Publicar distribución puede extender alerta por baja valoración
- **Generalización** – Gestionar usuario se especializa en registrar/modificar/eliminar

## Herramienta Utilizada

- Draw.io (diagrams.net) – Versión web

## Instrucciones de Uso del Repositorio

1. Clonar el repositorio
2. Abrir la carpeta `/diagramas`
3. Visualizar `diagrama_casos_uso.png` o `diagrama_casos_uso.pdf`
4. (Opcional) Revisar `/docs/especificacion_casos_uso.md` para detalles de flujos alternos

## Validación de Requisitos Técnicos

   
 Relaciones `<<include>>`, `<<extend>>` y generalización  
 Límite del sistema definido  
 Diagrama exportado en PNG/PDF  
 
