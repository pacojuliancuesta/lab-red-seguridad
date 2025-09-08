<<<<<<< HEAD
\# 🔐 Laboratorio de Redes y Seguridad en VirtualBox



\## 🎯 Objetivo

Este proyecto simula un entorno de red aislado para practicar técnicas de escaneo de seguridad y hardening de servidores, utilizando VirtualBox en Windows 11.

\## 📋 Componentes

Sistema Anfitrión: Windows 11



Hipervisor: VirtualBox 7.0+



Máquina Atacante: Kali Linux 2023.4



Servidor Objetivo: Ubuntu Server 24.04.3 LTS



\## 🛠️ Herramientas Utilizadas

Nmap - Escaneo de red y puertos



UFW (Uncomplicated Firewall) - Cortafuegos



Fail2Ban - Protección contra ataques de fuerza bruta



Nginx - Servidor web



OpenSSH - Acceso remoto seguro



\## 📊 Resultados

Antes del Hardening

Puertos abiertos: 22/tcp (SSH), 80/tcp (HTTP)



Servicios detectados: OpenSSH 8.9p1, Nginx 1.18.0



Vulnerabilidades: Detalles en escaneos/pre-hardening/



Después del Hardening

Puertos abiertos: 80/tcp (HTTP), 2222/tcp (SSH)



Servicios detectados: Nginx 1.18.0 (sin banners)



Medidas implementadas:



SSH en puerto no estándar (2222)



Login root deshabilitado



Fail2Ban protegiendo SSH



UFW bloqueando tráfico no esencial



\## 📁 Estructura del Proyecto

text

lab-red-seguridad/

├── diagramas/                 # Diagramas de red y topología

├── escaneos/                  # Resultados de escaneos Nmap

│   ├── pre-hardening/         # Escaneos antes del hardening

│   └── post-hardening/        # Escaneos después del hardening

├── servidor/                  # Configuraciones del servidor Ubuntu

├── kali/                      # Comandos y configuraciones de Kali

├── evidencias/                # Capturas de pantalla y evidencias

├── README.md                  # Este archivo

└── .gitignore                 # Archivos ignorados por Git

\## 🚀 Guía de Implementación

1\. Preparación del Entorno

Instalar Git for Windows



Instalar VirtualBox y Extension Pack



Crear repositorio en GitHub y clonarlo localmente



2\. Configuración de VirtualBox

Crear red Host-Only (vboxnet0)



Configurar máquinas virtuales con adaptador Host-Only



3\. Instalación y Configuración

Instalar Ubuntu Server 24.04.3 con IP estática 192.168.56.10



Instalar Kali Linux con IP estática 192.168.56.20



Configurar servicios básicos en Ubuntu (SSH, Nginx, UFW)



4\. Escaneos Iniciales

Realizar escaneos Nmap desde Kali



Documentar servicios y puertos abiertos



5\. Hardening del Servidor

Cambiar puerto SSH a 2222



Configurar UFW para permitir sólo puertos esenciales



Instalar y configurar Fail2Ban



Aplicar medidas de seguridad en Nginx



6\. Escaneos Finales

Realizar escaneos post-hardening



Comparar resultados con línea base



\## ⚠️ Consideraciones Éticas

Este laboratorio se ha realizado en un entorno completamente aislado y controlado. Todas las técnicas y herramientas se han utilizado exclusivamente con fines educativos en sistemas de propia propiedad.


\## 👨‍💻 Autor

Francisco Julián Cuesta - www.linkedin.com/in/franciscojuliáncuesta-bbbb25296



=======
# lab-red-seguridad
Laboratorio de seguridad en redes con VirtualBox (Kali + Ubuntu)
# 🔐 Laboratorio de Red y Seguridad (VirtualBox)
## 🎯 Objetivo
- Simular red interna con Kali (auditor) y Ubuntu (servidor).
- Medir superficie de ataque antes y después de aplicar hardening.

## 🖥️ Topología
Kali (192.168.56.20) ── Host-Only ── Ubuntu (192.168.56.10)

## 📝 Pasos
Instalación de VMs y red Host-Only en VirtualBox.

Configuración inicial de Ubuntu (SSH, Nginx, UFW).

Escaneo inicial con Nmap desde Kali.

Hardening del servidor (UFW, cambio de puerto SSH, fail2ban, servicios mínimos).

Escaneo final y comparación de resultados.

## 📊 Resultados esperados

Antes: puertos 22/tcp y 80/tcp abiertos.

Después: puerto 2222/tcp abierto, 80/tcp cerrado, root login deshabilitado.

## 🛠️ Herramientas

Windows 11 (host)

VirtualBox

Kali Linux

Ubuntu Server

Nmap

UFW

Fail2ban
>>>>>>> b3c2c197d04ca11053f2e10a250a8a5cd71a0ad9
