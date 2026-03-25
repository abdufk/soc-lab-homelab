# 02 — Wazuh SIEM — Instalación y configuración

## Descripción
Instalación del stack completo de Wazuh en Ubuntu Server y conexión 
del agente en Kali Linux.

## Componentes instalados
| Componente | Versión | Función |
|---|---|---|
| Wazuh Indexer | 4.11.2 | Base de datos de alertas |
| Wazuh Manager | 4.11.2 | Motor de detección |
| Wazuh Dashboard | 4.11.2 | Interfaz web |
| Wazuh Agent | 4.11.2 | Agente en Kali |

## Agente conectado
| Nombre | IP | OS | Estado |
|---|---|---|---|
| kiali-atacante | 10.0.2.15 | Kali GNU/Linux 2026.1 | ✅ Active |

## Vulnerabilidades detectadas automáticamente
- 🔴 1 Critical — CVE-2025-43859
- 🟠 12 High
- 🔵 13 Medium

---

## Capturas

**Dashboard de Wazuh operativo:**

![Dashboard](https://github.com/user-attachments/assets/5d134362-2b8c-493f-bece-502355d26507)

**Asistente de deploy del agente:**

![Deploy Agent](https://github.com/user-attachments/assets/9047f3ae-121b-4b25-a22a-5e73e4b9168b)

**Instalación del agente en Kali:**

![Agent Install](https://github.com/user-attachments/assets/f4ab3452-e715-4985-a455-c64c8aa8caad)

**Agente activo (active running):**

![Agent Active](https://github.com/user-attachments/assets/d879b6bd-7d62-40ee-a8e0-60cc71ecefcb)

**Dashboard con agente kiali-atacante conectado:**

![Agent Connected](https://github.com/user-attachments/assets/0c180921-8b91-43f1-b1e6-b5983790a2bf)

**Agente kiali-atacante — detalle:**

![Agent Detail](https://github.com/user-attachments/assets/107791c3-925a-4abf-89c8-6869320bd50a)

**Vulnerability Detection — CVEs detectados:**

![Vulnerabilities](https://github.com/user-attachments/assets/750d8385-9780-4d8e-8bad-6b0cadfcfe97)

**MITRE ATT&CK — Tácticas detectadas:**

![MITRE](https://github.com/user-attachments/assets/4ffd1e60-2e27-40bf-8c13-bdd1a94c2ac9)

**Threat Hunting — Eventos en tiempo real:**

![Threat Hunting](https://github.com/user-attachments/assets/4449e1ba-a1d7-4467-a76b-f821953cb8b9)
