# OpenCode 2.2.5 para Termux

**Compilación nativa para Android · ARM64**

Testeado en un MI10T PRO android 12 y en un POCO X7 PRO android 16 podría tener algunos bugs en otros no testeados

OpenCode es un asistente de programación con IA que vive en la terminal. Esta
es una compilación de la versión **2.2.5** pensada para **Termux**, con la
interfaz completa y funcionando directamente sobre Android, sin capas de
emulación ni dependencias externas.

**Nota:**
Se compilo esta version con ayuda de opencode-termux 2.0.22 por falta de lanzamiento de versiones 2.2.x por parte de Hope2333, ya que las ultimas versiones tienes novedades interesantes como la opción `/goal`

---

## Ficha rápida

| | |
|---|---|
| Versión | OpenCode **2.2.5** |
| Línea | Nativa (Android / Bionic) |
| Interfaz | OpenTUI **0.8.0** |
| Arquitectura | ARM64 (aarch64) |
| Requisitos | Android 9 o superior + Termux |
| Descarga | ~53 MB |
| Base del proyecto | [`opencode-termux`](https://github.com/Hope2333/opencode-termux) de **Hope2333** |

---

## Tecnologías utilizadas

| Tecnología | Para qué se usó |
|---|---|
| **OpenCode 2.2.5** | La aplicación en sí: su código oficial es el punto de partida. |
| **OpenTUI 0.8.0** | La biblioteca que dibuja la interfaz de terminal (paneles, colores, entrada). |
| **Bun** | El motor de ejecución con el que se arma el programa final para Android. |
| **Zig** | Compiló la biblioteca de interfaz para Android, sin necesidad del kit oficial de desarrollo (NDK). |
| **Bionic** | La biblioteca base propia de Android, en lugar de la de Linux de escritorio. |
| **Termux + Clang** | El entorno donde se construyó todo y el complemento de compatibilidad. |
| **opencode-termux (Hope2333)** | La base de scripts y empaquetado que hace posible compilar OpenCode para Termux. |

---

## Cómo se construyó

1. **Punto de partida.** Se tomó el código oficial de OpenCode 2.2.5 y el
   proyecto **opencode-termux** de Hope2333, que aporta el proceso de
   compilación y empaquetado para Termux.

2. **Adaptación de la interfaz.** OpenTUI 0.8.0 se preparó especialmente para
   Android y se compiló con Zig. Ahí se resolvieron los detalles que hacen que
   la interfaz funcione en el sistema de Android (gestión de memoria, hilos y
   bibliotecas del sistema).

3. **Compilación del programa.** La aplicación completa se compiló con Bun para
   Android y se le integró la interfaz ya adaptada, de modo que todo viaje en un
   solo ejecutable.

4. **Empaquetado.** Se añadió una capa mínima de compatibilidad de seguridad y
   se generó el instalador para Termux, listo para usar.

---

## Qué incluye

- La interfaz completa de OpenCode 2.2.5, funcional en la terminal.
- Un ejecutable único: no requiere instalar bibliotecas aparte.
- Funcionamiento nativo en Android: sin glibc, sin emulación y sin NDK al
  instalar.
- Probado en dispositivo real: inicia, dibuja la interfaz y responde.

---

## Instalación

1. Descargá el instalador que acompaña a este archivo.
2. Instalalo con el gestor de paquetes de Termux (`dpkg -i` apuntando al
   archivo descargado).
3. Escribí `opencode` para comenzar.

> Si ya tenés otra versión instalada, el instalador la reemplaza. Guardá una
> copia del ejecutable anterior si querés volver atrás.

---

## Créditos

- **OpenCode** — proyecto original y su equipo de desarrollo.
- **OpenTUI** — biblioteca de interfaz de terminal.
- **Hope2333** — proyecto `opencode-termux`, base de esta compilación.
- **Bun** y **Zig** — herramientas de compilación y ejecución.

Esta compilación es un trabajo de empaquetado y adaptación para Termux sobre el
trabajo de los proyectos mencionados.
