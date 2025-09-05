# lab-red-seguridad
Laboratorio de seguridad en redes con VirtualBox (Kali + Ubuntu)
# 🔐 Laboratorio de Red y Seguridad (VirtualBox)
## 🎯 Objetivo
- Simular red interna con Kali (auditor) y Ubuntu (servidor).
- Medir superficie de ataque antes y después de aplicar hardening.

## 🖥️ Topología
Kali (192.168.56.20) ── Host-Only ── Ubuntu (192.168.56.10)

```mermaid
graph LR
[Kali 192.168.56.20] ---|Host-Only| B[Ubuntu 192.168.56.10]

📝 Pasos
Instalación de VMs y red Host-Only en VirtualBox.

Configuración inicial de Ubuntu (SSH, Nginx, UFW).

Escaneo inicial con Nmap desde Kali.

Hardening del servidor (UFW, cambio de puerto SSH, fail2ban, servicios mínimos).

Escaneo final y comparación de resultados.

📊 Resultados esperados

Antes: puertos 22/tcp y 80/tcp abiertos.

Después: puerto 2222/tcp abierto, 80/tcp cerrado, root login deshabilitado.

🛠️ Herramientas

Windows 11 (host)

VirtualBox

Kali Linux

Ubuntu Server

Nmap

UFW

Fail2ban
