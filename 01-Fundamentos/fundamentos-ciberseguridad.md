- [CIA Triad](#cia-triad)
# 🛡️ Glosario de Ciberseguridad – Semana 1

## 🔐 CIA Triad

| Elemento            | Definición                                                                 | Ejemplo                         |
|---------------------|---------------------------------------------------------------------------|---------------------------------|
| **Confidencialidad** | Proteger la información para que solo personas autorizadas la vean.       | Encriptar datos, usar HTTPS.   |
| **Integridad**       | Garantizar que los datos no sean modificados sin autorización.            | Firmas digitales, hash.        |
| **Disponibilidad**   | Asegurar el acceso a los datos y sistemas cuando se necesiten.            | Backups, protección DDoS.      |

---

## ☠️ Amenazas Comunes

| Amenaza              | Descripción                                                                 | Ejemplo                           |
|----------------------|------------------------------------------------------------------------------|-----------------------------------|
| **Malware**           | Software malicioso que daña, roba o interfiere con sistemas.                | Virus, troyanos, ransomware.      |
| **Phishing**          | Engaño que busca robar datos haciéndose pasar por alguien de confianza.     | Email falso del "banco".          |
| **MITM (Man-In-The-Middle)** | Intercepta la comunicación entre dos partes.                         | Espiar tráfico en WiFi pública.   |
| **Ransomware**        | Secuestra tus archivos y pide un rescate.                                   | WannaCry, REvil.                  |
| **Ingeniería Social** | Engañar a humanos para obtener acceso o información.                        | Falsos técnicos o llamadas falsas.|

---

## ⚖️ Vulnerabilidad vs Amenaza vs Riesgo

| Concepto         | Definición                                                                  | Ejemplo                                               |
|------------------|-----------------------------------------------------------------------------|-------------------------------------------------------|
| **Vulnerabilidad** | Debilidad del sistema.                                                    | Contraseña débil, software sin actualizar.            |
| **Amenaza**        | Actor o evento que puede explotar una vulnerabilidad.                     | Hacker, malware, incendio.                           |
| **Riesgo**         | Probabilidad de daño por una amenaza que explota una vulnerabilidad.      | App desactualizada accesible desde Internet.         |

> 🎯 Analogia: Una puerta sin llave (**vulnerabilidad**) con ladrones cerca (**amenaza**) = alto **riesgo**.

---

## 🔐 Autenticación vs Autorización

| Concepto           | ¿Qué verifica?                  | Ejemplo                              |
|--------------------|----------------------------------|--------------------------------------|
| **Autenticación**   | Verifica si eres quien dices ser. | Ingresar usuario y contraseña.       |
| **Autorización**    | Verifica si puedes hacer cierta acción. | Acceder a configuración de admin.    |

> 📌 Primero te autenticas, luego te autorizan.  
> 🔑 Analogia: Entras a un edificio (autenticación), y luego te indican qué puertas puedes abrir (autorización).

---

## 👨‍💻 Roles en Ciberseguridad

| Rol                    | Descripción                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| **Pentester**          | Realiza pruebas de intrusión para encontrar vulnerabilidades.               |
| **Analista SOC**       | Monitorea alertas y eventos de seguridad en tiempo real.                    |
| **Red Team**           | Simula ataques reales para probar defensas.                                 |
| **Blue Team**          | Defiende y responde a incidentes de seguridad.                              |
| **Purple Team**        | Une al Red y Blue Team para mejorar continuamente la seguridad.             |
| **Ingeniero de Seguridad** | Diseña arquitecturas seguras y medidas preventivas.                   |
| **CISO**               | Lidera la estrategia de ciberseguridad en la organización.                  |


---
Tema: Fundamentos de Ciberseguridad
Semana: 1
Autor: Ricardo D. Villalobos
Actualizado: 2025-04-16
---
