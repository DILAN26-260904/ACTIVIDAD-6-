# 🛡️ Actividad 6 — Tus Dispositivos y Tu Seguridad
DILAN FELIPE LAGOS JIMENEZ 

# 📝 Punto 1 — Resumen de la Guía

---

## 📌 Resumen de lo Entendido

La guía **"Tus Dispositivos y Tu Seguridad"** aborda la importancia de proteger nuestros equipos y la información que manejamos, así como el uso de **máquinas virtuales** como herramienta segura para probar sistemas operativos, aplicaciones y configuraciones sin poner en riesgo nuestro equipo principal.

### 🗝️ Puntos clave:

- ✅ **Protección de datos:** Mantener actualizados el sistema operativo, el antivirus y realizar copias de seguridad periódicas.
- ✅ **Uso de máquinas virtuales:** Permiten crear entornos aislados donde se pueden instalar sistemas operativos adicionales sin modificar el equipo físico.
- ✅ **Aislamiento de riesgos:** Si una máquina virtual se infecta o falla, no afecta al sistema principal ni a otras máquinas virtuales.
- ✅ **Pruebas seguras:** Ideal para aprender, probar software o analizar archivos sospechosos de forma controlada.
- ✅ **Recursos compartidos:** Las máquinas virtuales utilizan parte de la memoria, procesador y almacenamiento del equipo físico, por lo que se debe planificar bien la asignación de recursos.

---

## 📸 Pantallazos del Paso a Paso

> **Instrucción para ti:** A continuación se describen los pasos generales. En tu repositorio, crea una carpeta llamada **`imagenes/`** y guarda allí tus capturas de pantalla con los nombres que se indican:

| Paso | Descripción | Nombre del archivo |
|------|-------------|--------------------|
| **Paso 1** | Descarga e instalación del software de virtualización (por ejemplo, VirtualBox) | `imagenes/paso1_instalacion.jpg` |
| **Paso 2** | Creación de una nueva máquina virtual — asignación de nombre y sistema operativo | `imagenes/paso2_nombre_so.jpg` |
| **Paso 3** | Asignación de memoria RAM al sistema virtual | `imagenes/paso3_memoria_ram.jpg` |
| **Paso 4** | Creación del disco duro virtual | `imagenes/paso4_disco_virtual.jpg` |
| **Paso 5** | Configuración de red y ajustes del sistema | `imagenes/paso5_config_red.jpg` |
| **Paso 6** | Instalación del sistema operativo dentro de la máquina virtual | `imagenes/paso6_instalacion_so.jpg` |
| **Paso 7** | Inicio del sistema y verificación de funcionamiento | `imagenes/paso7_funcionando.jpg` |

> 💡 **Nota:** Sube tus capturas reales a la carpeta `imagenes/` de tu repositorio para completar esta sección.

# 💻 Punto 2 — Herramientas de Virtualización

---

## 📋 Cuadro Comparativo General

| Característica | VirtualBox | WSL | VMware Workstation | QEMU | KVM |
|----------------|-----------|-----|-------------------|------|-----|
| **Desarrollador** | Oracle | Microsoft | VMware Inc. | Comunidad open-source | Red Hat / Comunidad Linux |
| **Licencia** | Gratuito (con restricciones) | Gratuito | Gratuito / Versión Pro de pago | Libre y gratuita | Libre y gratuita |
| **Tipo** | Hipervisor tipo 2 | Subsistema Linux sobre Windows | Hipervisor tipo 2 | Emulador y virtualizador | Hipervisor tipo 1 (integrado en Linux) |
| **Sistema anfitrión** | Windows, Linux, macOS | Windows 10/11 | Windows, Linux | Windows, Linux, macOS | Linux |
| **Emulación** | Virtualización nativa | Compatibilidad binaria | Virtualización nativa | Emulación completa + virtualización | Virtualización nativa |
| **Rendimiento** | Bueno | Excelente | Muy bueno | Variable (emulación más lenta) | Excelente |

---

## 🔍 Detalle de Cada Tecnología

---

### 🟦 VirtualBox

> **¿Qué es?** Es un software de virtualización de código abierto que permite crear y ejecutar máquinas virtuales en un solo equipo físico. Desarrollado originalmente por Sun Microsystems, hoy pertenece a Oracle.

**Características:**
- ✅ Soporte para múltiples sistemas operativos: Windows, Linux, macOS, Solaris, FreeBSD
- ✅ Interfaz gráfica intuitiva y versión de línea de comandos
- ✅ Soporte para USB, carpetas compartidas y red adaptable
- ✅ Instantáneas: guardar el estado de la máquina en cualquier momento

**Ventajas:**
- ✅ Multiplataforma — funciona en los principales SO
- ✅ Fácil de usar y aprender
- ✅ Amplia documentación y comunidad
- ✅ Versión básica gratuita

**Desventajas:**
- ⚠️ Menor rendimiento comparado con soluciones de pago o de tipo 1
- ⚠️ Algunas funciones avanzadas requieren el paquete de extensión

**Aplicaciones:**
- Laboratorios de aprendizaje
- Prueba de sistemas operativos
- Entornos de desarrollo aislados
- Análisis seguro de software

---

### 🟩 WSL — Windows Subsystem for Linux

> **¿Qué es?** Es una característica de Windows que permite ejecutar un entorno Linux directamente sobre Windows, **sin necesidad de crear una máquina virtual completa ni reiniciar el equipo**.

**Características:**
- ✅ Integración total entre archivos de Windows y Linux
- ✅ Acceso a la red del anfitrión directamente
- ✅ Inicio en segundos — sin arranque de sistema completo
- ✅ Soporte para interfaz gráfica de aplicaciones Linux (WSL 2)

**Ventajas:**
- ✅ Muy ligero — consume pocos recursos
- ✅ Excelente rendimiento
- ✅ Comandos Linux disponibles sin salir de Windows
- ✅ Fácil instalación desde la tienda de Microsoft

**Desventajas:**
- ⚠️ Solo disponible en Windows 10 versión 2004+ y Windows 11
- ⚠️ No reemplaza una máquina virtual completa para todos los usos
- ⚠️ No es ideal para entornos gráficos completos de escritorio

**Aplicaciones:**
- Desarrollo de software
- Uso de herramientas de línea de comandos de Linux
- Programación, scripting y administración de servidores
- Aprendizaje de Linux sin particionar el disco

---

### 🟧 VMware Workstation (Player / Pro)

> **¿Qué es?** Es uno de los softwares de virtualización más reconocidos del mercado. Existen dos versiones principales: **Workstation Player** (gratuito para uso personal) y **Workstation Pro** (de pago, con funciones avanzadas).

**Características:**
- ✅ Alto rendimiento y estabilidad
- ✅ Soporte para redes complejas y clonación de máquinas
- ✅ Integración con vSphere (plataforma empresarial de VMware)
- ✅ Instantáneas múltiples y gestión avanzada de recursos

**Ventajas:**
- ✅ Excelente rendimiento
- ✅ Más funciones avanzadas que VirtualBox
- ✅ Compatibilidad con formatos industriales
- ✅ Soporte técnico oficial en versión Pro

**Desventajas:**
- ⚠️ La versión completa es de pago
- ⚠️ Menos ligero que otras alternativas
- ⚠️ Requiere más recursos del sistema

**Aplicaciones:**
- Entornos profesionales de desarrollo
- Capacitación laboral
- Prueba de aplicaciones en diferentes sistemas
- Laboratorios de ciberseguridad

---

### 🟨 QEMU — Quick EMUlator

> **¿Qué es?** Es una herramienta de software libre que puede funcionar como **emulador completo** o como **virtualizador**. Como emulador, puede ejecutar sistemas operativos compilados para una arquitectura diferente a la del equipo anfitrión.

**Características:**
- ✅ Emula diferentes arquitecturas: x86, ARM, RISC-V, PowerPC
- ✅ Funciona sin necesidad de extensiones de virtualización del procesador
- ✅ Se combina con KVM para aceleración nativa
- ✅ Versátil y muy ligero en su versión básica

**Ventajas:**
- ✅ Multiplataforma y de código abierto
- ✅ Puede ejecutar sistemas para otras arquitecturas
- ✅ Muy flexible — se adapta a diferentes necesidades
- ✅ No requiere procesador con virtualización habilitada

**Desventajas:**
- ⚠️ Como emulador puro, es más lento
- ⚠️ Sin interfaz gráfica oficial — suele usarse con herramientas como Virt-Manager o máquinas gráficas de terceros
- ⚠️ Curva de aprendizaje mayor

**Aplicaciones:**
- Desarrollo para dispositivos embebidos (Raspberry Pi, etc.)
- Investigación de arquitecturas diferentes
- Virtualización ligera en servidores
- Plataformas de emulación

---

### 🟪 KVM — Kernel-based Virtual Machine

> **¿Qué es?** Es una tecnología de virtualización integrada directamente en el núcleo de **Linux**. Convierte al sistema operativo en un hipervisor de tipo 1, permitiendo ejecutar máquinas virtuales con rendimiento casi igual al del equipo físico.

**Características:**
- ✅ Virtualización nativa — el kernel de Linux gestiona directamente los recursos
- ✅ Cada máquina virtual es un proceso normal del sistema Linux
- ✅ Soporte completo para hardware con extensiones Intel VT-x y AMD-V
- ✅ Se gestiona con herramientas como Virt-Manager, libvirt o desde línea de comandos

**Ventajas:**
- ✅ Excelente rendimiento — casi igual al equipo físico
- ✅ Gratuito y parte de Linux estándar
- ✅ Seguridad mejorada — aislamiento entre máquinas
- ✅ Base de soluciones empresariales (OpenStack, Proxmox, etc.)

**Desventajas:**
- ⚠️ Solo disponible en sistemas Linux
- ⚠️ Requiere procesador con virtualización habilitada
- ⚠️ Sin interfaz gráfica por defecto — necesita instalar herramientas adicionales

**Aplicaciones:**
- Servidores y centros de datos
- Alojamiento de múltiples sistemas en un solo equipo
- Infraestructura en la nube
- Virtualización de alto rendimiento

  ```
## 📊 Resumen Visual

```

TIPO DE VIRTUALIZACIÓN

┌─────────────────────────────────────────────┐
│                                               │
│  TIPO 1 — Hipervisor en el hardware           │
│    └─ KVM  ✅ Más rápido y eficiente          │
│                                               │
│  TIPO 2 — Sobre un sistema operativo         │
│    ├─ VirtualBox  ✅ Fácil y multiplataforma │
│    ├─ VMware      ✅ Profesional y completo   │
│    └─ QEMU + KVM  ✅ Combinación potente      │
│                                               │
│  ESPECIALIZADO                                │
│    └─ WSL         ✅ Linux sobre Windows      │
│       sin máquina virtual completa            │
│                                               │
└─────────────────────────────────────────────┘

📄 Archivo: `03_Arquitecturas_Redes.md`

```
# 🌐 Punto 3 — Arquitecturas de Red: Explicación y Simulación

---

## 📌 Conceptos Previos

Una **arquitectura de red** define cómo se organizan y conectan los dispositivos para compartir información y recursos. Cada diseño tiene características, ventajas y escenarios de uso específicos.

---

## 🏗️ Principales Arquitecturas de Red

### 🔹 1. Red Punto a Punto

> **Concepto:** Conexión directa entre dos dispositivos únicamente. No hay dispositivos intermedios.

```

┌──────────┐                    ┌──────────┐
│ Equipo A │◄──────────────────►│ Equipo B │
└──────────┘      Cable         └──────────┘

```
**Características:**
- ✅ Conexión directa — sin equipos intermedios
- ✅ Fácil de configurar
- ⚠️ Limitada — solo dos dispositivos
- ⚠️ Si falla la conexión, se pierde comunicación completamente

**Uso:** Conexión directa entre dos equipos, enlaces de fibra entre sedes, copia rápida de archivos.

---

### 🔹 2. Red en Estrella

> **Concepto:** Todos los dispositivos se conectan a un punto central (switch o router). Es la arquitectura más utilizada hoy en día.

```

┌─────────────┐
│   SWITCH    │
│  (Central)  │
└───┬─────┬───┘
│     │
┌─────────┼─────┼─────────┐
│         │     │         │
┌───┴───┐ ┌───┴───┐ ┌───┴───┐ ┌───┴───┐
│ PC 1  │ │ PC 2  │ │ PC 3  │ │ PC 4  │
└───────┘ └───────┘ └───────┘ └───────┘

```
*Características:**
- ✅ Si un cable falla, solo afecta a ese dispositivo
- ✅ Fácil de añadir o quitar equipos
- ⚠️ Si falla el dispositivo central, toda la red cae

**Uso:** Oficinas, salas de informática, hogares, edificios corporativos.

---

### 🔹 3. Red en Bus

> **Concepto:** Todos los dispositivos se conectan a un único cable principal llamado "bus" o "canal de transmisión".

```

┌───────┐    ┌───────┐    ┌───────┐    ┌───────┐
│ PC 1  │────│ PC 2  │────│ PC 3  │────│ PC 4  │
└───────┘    └───────┘    └───────┘    └───────┘
▲═══════════════════════════════▲
Cable principal (bus)

```
**Características:**
- ✅ Económica — poco cableado
- ⚠️ Si falla el cable principal, toda la red falla
- ⚠️ El rendimiento disminuye a medida que hay más dispositivos

**Uso:** Redes antiguas, conexiones temporales — hoy en desuso.

---

### 🔹 4. Red en Anillo

> **Concepto:** Cada dispositivo se conecta a los dos dispositivos vecinos, formando un círculo cerrado. La información viaja de un equipo a otro hasta llegar al destino.

```

┌───────┐
│ PC 1  │
└───┬───┘
│
┌───────┬───────┐
│ PC 4  │       │ PC 2  │
└───────┴───────┘
┌───┬───┐
│ PC 3  │
└───────┘

```
**Características:**
- ✅ Rendimiento constante
- ⚠️ Si un equipo o cable falla, se rompe el anillo y cae la red
- ✅ Existe la versión de doble anillo para mayor redundancia

**Uso:** Redes metropolitanas, fibra óptica en campus universitarios, infraestructuras críticas.

---

### 🔹 5. Red de Malla

> **Concepto:** Los dispositivos se conectan entre sí de múltiples formas, creando varias rutas posibles para enviar información.

```

┌───────┐    ┌───────┐    ┌───────┐
│ Nodo A│◄──►│ Nodo B│◄──►│ Nodo C│
└───┬───┘    └───┬───┘    └───┬───┘
│            │            │
│     ┌──────┼──────┐     │
│     │ Nodo D │     │
│     └────────────┘     │
┌───▼───┐    ┌──────┼──────┐    ┌──▼───┐
│ Nodo E │◄──►│ Nodo F │◄──►│ Nodo G │
└───────┘    └────────────┘    └───────┘

**Características:**
- ✅ Alta redundancia — si una ruta falla, se usa otra
- ✅ Resistencia a fallos
- ⚠️ Mayor costo y complejidad

**Uso:** Internet, redes inalámbricas de sensores, telecomunicaciones militares, IoT.

---

## 🛠️ Simulación en Cisco Packet Tracer

### 📌 Ejemplo: Red en Estrella
