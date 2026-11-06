# Trabajo Integrador 2do Cuatrimestre

**Materia:** Modelo y Sistemas, 7mo Año, Escuela Técnica  
**Alumno:** Tomas Chandler  
**Profesor:** Gian Franco Denaro  
**Fecha de entrega:** 13/11/2026

## De qué se trata

Este repositorio tiene el Trabajo Integrador Individual de la materia. La consigna pedía armar la documentación técnica y de usuario de un sistema real. Elegí la opción C, usando SistemaPP, el sistema que hicimos en Prácticas Profesionalizantes ([repositorio del sistema](https://github.com/santycarnevaa/SistemaPP)).

SistemaPP es una aplicación de escritorio en C# (Windows Forms) con base de datos SQL Server. Maneja usuarios y seguridad, y un módulo de catálogo y stock con movimientos, scrap, kardex, reportes y auditoría. Para la parte práctica del trabajo tomé como proceso central el **registro de un egreso de stock**, que es donde el sistema hace más controles antes de guardar.

## Contenido del trabajo

1. **Marco conceptual y clasificación:** diferencia entre documentación de usuario y técnica, y clasificación de los dos ejemplos de la consigna.
2. **Documentación paso a paso:** instructivo para registrar un egreso de stock, con prerrequisitos, pasos, resultado esperado y errores posibles.
3. **Diagrama de flujo:** lógica de validación del egreso, con los caminos de error.
4. **Caso de uso formal:** CU-01 Registrar egreso de stock, con flujo principal y flujos alternativos.
5. **Captura anotada:** pantalla de Movimientos de Stock con referencias numeradas.

## Estructura del repositorio

```
documentos/
  Trabajo_Integrador_Tomas_Chandler.pdf   → trabajo completo
imagenes/
  diagrama_flujo_egreso_stock.png         → diagrama del apartado 3
  interfaz_movimientos_stock.png          → captura anotada del apartado 5
README.md
```

## Imágenes

El diagrama de flujo (apartado 3) y la captura anotada de la interfaz (apartado 5) están dentro del documento PDF, junto con su explicación. También se pueden ver por separado en la carpeta `imagenes`.
