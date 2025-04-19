# 📡 Modelo OSI – Glosario de Ciberseguridad

## 🧠 ¿Qué es el Modelo OSI?

El modelo **OSI (Open Systems Interconnection)** describe **cómo viajan los datos a través de una red**, dividiendo el proceso en **7 capas**. Cada capa tiene funciones específicas.

> 📦 Es como enviar un paquete por etapas: cada capa lo empaca o desempaca.

---

## 🧱 Las 7 Capas del Modelo OSI (de abajo hacia arriba)

| Nº | Capa                  | Función                                               | Ejemplos reales                      |
|----|------------------------|--------------------------------------------------------|--------------------------------------|
| 7️⃣ | **Aplicación**         | Interacción directa con el usuario final.              | HTTP, FTP, correo, navegador         |
| 6️⃣ | **Presentación**       | Traducción, cifrado y compresión de datos.             | SSL/TLS, codificación JPEG           |
| 5️⃣ | **Sesión**             | Control de conexión: inicio, mantenimiento, cierre.    | Logins persistentes, RPC             |
| 4️⃣ | **Transporte**         | Entrega confiable y ordenada de datos.                 | TCP, UDP                             |
| 3️⃣ | **Red**                | Enrutamiento: elige la mejor ruta para los datos.      | IP, Routers                          |
| 2️⃣ | **Enlace de datos**    | Comunicación dentro de la red local.                   | Ethernet, MAC, Switch                |
| 1️⃣ | **Física**             | Transmisión de bits por medios físicos.                | Cable UTP, WiFi, fibra óptica        |

---

## 🧠 Mnemotecnia

- **"Por Favor Señor, Tenga Su Pizza Lista Ayer"** (Física → Aplicación)
- **"Así Pasa Siempre Tener Redes Establece Fundación"** (Aplicación → Física)

---

## 🚀 Flujo de datos en la vida real (Ej: WhatsApp)

1. Aplicación: Escribes "Hola".
2. Presentación: Se cifra el mensaje.
3. Sesión: Se abre sesión con el servidor.
4. Transporte: Se divide en paquetes TCP.
5. Red: IP determina la mejor ruta.
6. Enlace de Datos: Agrega dirección MAC.
7. Física: Bits enviados por WiFi/cable.

Destino: proceso inverso. 🔄

---

## 🔐 Seguridad por capa

| Capa | Amenazas comunes                         |
|------|------------------------------------------|
| 7    | Phishing, XSS, ataques a APIs            |
| 6    | Ataques a SSL/TLS (SSL Stripping)        |
| 5    | Session Hijacking                        |
| 4    | DDoS, escaneo de puertos                 |
| 3    | IP Spoofing, rutas maliciosas            |
| 2    | Sniffing, MAC Spoofing                   |
| 1    | Interferencia electromagnética, cortes   |

---


# 🛡️ Reto 1 – Mapa de Amenazas por Capa OSI (con ejemplos técnicos)

Este reto te ayudará a entender cómo se manifiestan las amenazas en cada capa del modelo OSI, con ejemplos técnicos reales que podrías practicar en un entorno controlado.

| Capa | Amenaza                         | Descripción + Ejemplo técnico                          |
|------|----------------------------------|--------------------------------------------------------|
| 7️⃣ Aplicación | **Phishing**                        | El atacante clona un sitio como `facebook.com` y envía un link falso (`faceb00k-login.com`) por correo o mensaje. Cuando el usuario introduce sus datos, el atacante los recibe. <br> **Herramientas:** SET (Social-Engineer Toolkit), Gophish |
| 6️⃣ Presentación | **SSL Stripping**                  | El atacante intercepta la conexión y redirige de `https://` a `http://`, eliminando el cifrado. <br> **Ejemplo:** Ataque con `bettercap` o `mitmproxy` en una red local. |
| 5️⃣ Sesión | **Session Hijacking**              | Alguien roba la cookie de sesión de un usuario autenticado y la usa para suplantarlo. <br> **Ejemplo:** Usar Burp Suite o Wireshark para capturar cookies no cifradas. |
| 4️⃣ Transporte | **SYN Flood (DoS)**               | Enviar miles de paquetes TCP SYN falsos a un servidor, saturando su capacidad de respuesta. <br> **Ejemplo:** Ataque con `hping3 -S -p 80 -i u100 <ip>` o con `LOIC/HOIC`. |
| 3️⃣ Red | **IP Spoofing**                    | El atacante envía paquetes con una IP de origen falsificada, generalmente como parte de un ataque de suplantación o DDoS. <br> **Ejemplo:** `hping3 -a <ip_falsa> <ip_víctima>` |
| 2️⃣ Enlace de datos | **ARP Spoofing**                   | El atacante envía respuestas ARP falsas en la red local para posicionarse entre víctima y gateway (MITM). <br> **Ejemplo:** `arpspoof -i wlan0 -t <victima> <router>` con `dsniff`, `ettercap` o `bettercap`. |
| 1️⃣ Física | **Interferencia/Acceso físico** | Cortar un cable de red, desactivar un punto de acceso WiFi o capturar señales con una antena. <br> **Ejemplo:** Uso de antenas como Alfa AWUS036NHA con `airodump-ng`. |

---
Tema: Modelo OSI 
Semana: 2
Autor: Ricardo D. Villalobos
Actualizado: 2025-04-18