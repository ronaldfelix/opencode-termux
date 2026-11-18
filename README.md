# OpenCode  para Termux

Compilación nativa para Android · ARM64

Testeado en un MI10T PRO android 12 y en un POCO X7 PRO android 16 podría tener algunos bugs en otros no testeados

OpenCode es un asistente de programación con IA que vive en la terminal. Esta es una compilación de la versión 2.3.0 pensada para Termux, con la interfaz completa y funcionando directamente sobre Android, sin capas de emulación ni dependencias externas.

Nota: Se compilo esta version con ayuda de opencode-termux 2.x por falta de lanzamiento de versiones 2.x por parte de Hope2333, ya que las ultimas versiones tienes novedades interesantes como la opción /goal

---

## Ficha rápida

| | |
|---|---|
| Versión | OpenCode **2.3.2** |
| Línea | Nativa (Android / Bionic) |
| Interfaz | OpenTUI **0.8.4** |
| Arquitectura | ARM64 (aarch64) |
| Requisitos | Android 9 o superior + Termux |
| Instalador | ~56 MB |
| Fecha de compilación | 17 de noviembre de 2026 |
| Base del proyecto | [`opencode-termux`](https://github.com/Hope2333/opencode-termux) de **Hope2333** |

---

## Timeline en este repo

| Versión | Interfaz | Fecha | Instalador |
|---|---|---|---|
| 2.2.5 | OpenTUI 0.8.0 | 30/10/2026 | 55,7 MB |
| 2.2.7 | OpenTUI 0.8.1 | 11/11/2026 | 56,5 MB |
| 2.3.0 | OpenTUI 0.8.4 | 16/11/2026 | 56,5 MB |
| **2.3.2** | **OpenTUI 0.8.4** | **17/11/2026** | **56,5 MB** |


---

## Tecnologías utilizadas

| Tecnología | Para qué se usó |
|---|---|
| **OpenCode 2.3.2** | La aplicación en sí: su código oficial es el punto de partida. |
| **OpenTUI 0.8.4** | La biblioteca que dibuja la interfaz de terminal (paneles, colores, entrada). |
| **Bun** | El motor de ejecución con el que se arma el programa final para Android. |
| **Zig** | Compiló la biblioteca de interfaz para Android, sin necesidad del kit oficial de desarrollo (NDK). |
| **Bionic** | La biblioteca base propia de Android, en lugar de la de Linux de escritorio. |
| **Termux + Clang** | El entorno donde se construyó todo y el complemento de compatibilidad. |
| **opencode-termux (Hope2333)** | La base de scripts y empaquetado que hace posible compilar OpenCode para Termux. |


## Qué incluye

- La interfaz completa de OpenCode 2.3.2, funcional en la terminal.
- Un ejecutable único: no requiere instalar bibliotecas aparte.
- Funcionamiento nativo en Android: sin glibc, sin emulación y sin NDK al
  instalar.
- Probado en dispositivo real: inicia, dibuja la interfaz y responde.


## Instalación

1. Descargar el instalador que acompaña a este archivo
   (`opencode_2.3.2_aarch64.deb`).
2. Instalalo con el gestor de paquetes de Termux:

   ```bash
   dpkg -i opencode_2.3.2_aarch64.deb
   ```

3. Escribir `opencode` para comenzar.

> Si ya tienes otra versión instalada, el instalador la reemplaza. Guardar una
> copia del ejecutable anterior si quieres volver atrás.

---

## Créditos

- **OpenCode** — proyecto original y su equipo de desarrollo.
- **OpenTUI** — biblioteca de interfaz de terminal.
- **Hope2333** — proyecto `opencode-termux`, base de esta compilación.
- **Bun** y **Zig** — herramientas de compilación y ejecución.

Esta compilación es un trabajo de empaquetado y adaptación para Termux sobre el
trabajo de los proyectos mencionados.
