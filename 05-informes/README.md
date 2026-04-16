# Informes de incidentes
# Incidente 01 — Ataque de fuerza bruta SSH

**Fecha:** 24/03/2026  
**Hora de detección:** 17:17  
**Severidad:** Media  
**Estado:** Contenido  

---

## Descripción

Ataque de fuerza bruta contra el servicio SSH del host 10.0.2.5 
(Metasploitable2) originado desde 10.0.2.15 (kali-atacante).
La herramienta utilizada fue Medusa con el diccionario rockyou.txt.

---

## Indicadores de Compromiso (IOCs)

| IOC | Valor |
|---|---|
| IP atacante | 10.0.2.15 |
| IP víctima | 10.0.2.5 |
| Puerto | 22 (SSH) |
| Usuario objetivo | msfadmin |
| Herramienta | Medusa v2.3 |

---

## Eventos detectados por Wazuh

| Rule ID | Descripción | Nivel |
|---|---|---|
| 5503 | PAM: User login failed | 5 |
| 5557 | unix_chkpwd: Password check failed | 5 |

---

## Cronología

- **17:17:18** — Primeros intentos fallidos de autenticación SSH
- **17:17:24** — Wazuh registra múltiples eventos PAM fallidos
- **17:17:25** — Acceso exitoso obtenido (contraseña encontrada)

---

## Acciones de contención

- Identificada IP atacante 10.0.2.15
- En entorno real: bloqueo inmediato de IP en firewall
- En entorno real: deshabilitar autenticación por contraseña en SSH, usar claves

---

## Recomendaciones

1. Implementar fail2ban para bloquear IPs tras N intentos fallidos
2. Deshabilitar autenticación por contraseña en SSH
3. Cambiar puerto SSH por defecto (22)
4. Usar autenticación por clave pública
