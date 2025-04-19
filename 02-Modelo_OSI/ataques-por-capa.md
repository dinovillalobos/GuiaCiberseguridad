# 🌐 Mapa Interactivo: Modelo OSI + Ataques Cibernéticos Relacionados

## 🧭 Modelo OSI – Capas + Ataques

### 7️⃣ Capa de Aplicación

- Protocolos: HTTP, HTTPS, FTP, DNS, SMTP
- ⚠️ Amenazas:
  - Phishing
  - SQL Injection
  - DNS Spoofing
  - XSS (Cross-Site Scripting)
  - Remote Code Execution (RCE)

📌 *Ejemplo:*  
Un atacante envía un link `http://fakebank.com` simulando una página de login real. Cuando la víctima introduce sus credenciales, estas son enviadas al atacante.  
➡️ Herramientas: Gophish, SEToolkit

### 6️⃣ Capa de Presentación

- Funciones: cifrado/descifrado, compresión, traducción de datos
- ⚠️ Amenazas:
  - SSL Stripping
  - Downgrade Attacks
  - Fallas de configuración TLS

📌 *Ejemplo:*  
Un proxy malicioso fuerza el uso de HTTP en lugar de HTTPS eliminando la seguridad de la capa de presentación.  
➡️ Herramientas: Bettercap, mitmproxy

### 5️⃣ Capa de Sesión

- Funciones: manejo de sesiones, autenticación, control de diálogo
- ⚠️ Amenazas:
  - Session Hijacking
  - Session Fixation

📌 *Ejemplo:*  
Un atacante roba cookies de sesión no cifradas para entrar a una cuenta sin necesidad de login.  
➡️ Herramientas: Wireshark, Burp Suite

### 4️⃣ Capa de Transporte

- Protocolos: TCP, UDP
- ⚠️ Amenazas:
  - SYN Flood
  - Port Scanning
  - TCP Reset Attacks

📌 *Ejemplo:*  
Un SYN flood genera miles de conexiones incompletas al puerto 80 de un servidor para saturarlo.  
➡️ Herramientas: hping3, LOIC

### 3️⃣ Capa de Red

- Protocolos: IP, ICMP
- ⚠️ Amenazas:
  - IP Spoofing
  - ICMP Flood (Ping of Death)
  - Routing Table Poisoning

📌 *Ejemplo:*  
Ataque DoS mediante paquetes ICMP falsos enviados desde direcciones IP falsas.  
➡️ Herramientas: hping3, Scapy

### 2️⃣ Capa de Enlace de Datos

- Protocolos: Ethernet, ARP, PPP
- ⚠️ Amenazas:
  - ARP Spoofing
  - MAC Flooding
  - Switch Spoofing

📌 *Ejemplo:*  
El atacante se hace pasar por el router para interceptar tráfico local mediante ARP Poisoning.  
➡️ Herramientas: Bettercap, Ettercap

### 1️⃣ Capa Física

- Tecnologías: cables, WiFi, hardware, señales
- ⚠️ Amenazas:
  - Sniffing de señales
  - Jamming (interferencias)
  - Acceso físico a equipos

📌 *Ejemplo:*  
Un atacante usa una antena Alfa para interceptar tráfico WiFi o deshabilitar un punto de acceso.  
➡️ Herramientas: Airodump-ng, Wireshark


---

## 🧠 ¿Cómo usar este diagrama?

1. Repásalo una vez al día durante 1 semana.
2. Intenta recordar al menos:
   - 1 protocolo por capa
   - 2 ataques comunes
   - 1 herramienta de ataque por caso
3. Evalúate con flashcards o prueba escrita.

---
Tema:Ataques por capa 
Semana: 2
Autor: Ricardo D. Villalobos
Actualizado: 2025-04-18