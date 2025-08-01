# 🛡️ Audit-SecurityStack-Windows

Script por lotes (`.bat`) para realizar una auditoría rápida del stack de seguridad en sistemas Windows. Este script permite identificar configuraciones del firewall, presencia de antivirus, procesos relacionados con herramientas de seguridad, estado de Sysmon, y exclusiones activas en Windows Defender.

## 🎯 Objetivo

Proporcionar un método rápido y portable para realizar **reconocimiento de defensas** en entornos Windows, útil en escenarios:

- 🔍 Auditoría defensiva
- 🛠️ Preparación para pruebas Red Team
- 🧪 Investigaciones forenses o de hardening
- 🧱 Post-explotación (según autorización)

## 🔍 ¿Qué analiza el script?

1. **Configuración del firewall** (`netsh advfirewall`)
2. **Presencia de Windows Defender** (`sc query windefend`)
3. **Procesos relacionados con AV/EDR conocidos** (`tasklist + findstr`)
4. **Detección de Sysmon a nivel de driver** (`fltmc`)
5. **Software antivirus registrado vía WMI** (`wmic /Namespace:\\root\SecurityCenter2`)
6. **Exclusiones activas en Windows Defender** (`wmic MSFT_MpPreference`)

## 🚀 Cómo ejecutar

1. Abre una consola CMD con privilegios de **Administrador**
2. Navega al directorio donde se encuentra el script
3. Ejecuta:

```cmd
Audit-SecurityStack-Windows.bat
````

> ⚠️ El script muestra la información en consola. Puedes redirigir la salida a un archivo si lo deseas:
>
> ```cmd
> Audit-SecurityStack-Windows.bat > reporte_defensas.txt
> ```

## ✅ Requisitos

* Windows 10/11 o Windows Server 2016+
* Consola `cmd.exe`
* Permisos de administrador (recomendado)

## 💡 Uso ético

Este script está diseñado con fines educativos, defensivos y profesionales. No debe utilizarse sin la debida autorización en entornos productivos o ajenos.

## 🧑‍💻 Autor

ErickO.
🔗 GitHub: [@NoTrustedx](https://github.com/NoTrustedx)

## 📄 Licencia

MIT License – Libre para usar, modificar y compartir bajo los términos de la licencia.

```
¿Deseas que te prepare también una versión que guarde todo en un archivo de salida (`.txt`) y que tenga colores si se ejecuta desde PowerShell? Puedo ayudarte a convertirlo también en `.ps1`.
```
