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
6. **Documentación del proyecto en 7 pasos:** requisitos, diseño (casos de uso, diagrama entidad relación, arquitectura y prototipos), manual técnico, manual de usuario, pruebas, instalación y despliegue, y control de versiones de la documentación.

## Estructura del repositorio

```
documentos/
  Trabajo_Integrador_2do_Cuatrimestre.pdf → trabajo completo
imagenes/
  diagrama_flujo_egreso_stock.png         → diagrama del apartado 3
  interfaz_movimientos_stock.png          → captura anotada del apartado 5
README.md
```

## Requisitos para correr el sistema

El sistema documentado es [SistemaPP](https://github.com/santycarnevaa/SistemaPP). Para poder abrirlo y ejecutarlo hace falta:

**Lenguajes y tecnologías usadas**

- C# con .NET 8 (`net8.0-windows`)
- Windows Forms para la interfaz
- SQL Server como base de datos, con T-SQL para las tablas y procedimientos almacenados
- Paquete NuGet `Microsoft.Data.SqlClient` para la conexión a la base (Visual Studio lo descarga solo al compilar)

**Programas necesarios**

- Windows 10 u 11, ya que Windows Forms solo funciona en Windows
- Visual Studio 2022 con la carga de trabajo "Desarrollo de escritorio de .NET" (incluye el SDK de .NET 8)
- SQL Server (la edición Express o Developer alcanza)
- SQL Server Management Studio (SSMS) para ejecutar el script de la base de datos
- Conexión a internet la primera vez que se compila, para descargar el paquete NuGet

**Pasos para ponerlo en marcha**

1. Clonar o descargar el repositorio de SistemaPP.
2. Abrir SSMS, conectarse al servidor local y ejecutar el archivo `BaseDeDatos.sql`. Ese script crea la base `SistemaUsuariosDB` con todas las tablas, procedimientos y datos iniciales, incluido el usuario `admin`.
3. Revisar la cadena de conexión en `WinFormsApp1/appsettings.json`. Por defecto apunta a `Server=localhost` con autenticación de Windows; si SQL Server se instaló con otro nombre de instancia (por ejemplo `localhost\SQLEXPRESS`), hay que cambiarlo ahí.
4. Para que funcione el envío de mails (recuperación de contraseña y códigos), copiar `mailsettings.example.json` como `mailsettings.json` en la carpeta del repositorio y completar el correo de Gmail y su contraseña de aplicación. Si no se configura, el resto del sistema funciona igual.
5. Abrir `SistemaPP.sln` en Visual Studio, dejar `CapaVista` como proyecto de inicio y ejecutar con F5.

## Imágenes

El diagrama de flujo (apartado 3) y la captura anotada de la interfaz (apartado 5) están dentro del documento PDF, junto con su explicación. También se pueden ver por separado en la carpeta `imagenes`.
