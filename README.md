# SOC Home Lab — IT/OT Security

![Status](https://img.shields.io/badge/Status-En%20progreso-yellow)
![SIEM](https://img.shields.io/badge/SIEM-Wazuh-blue)
![Attacker](https://img.shields.io/badge/Attacker-Kali%20Linux-red)

Proyecto personal de ciberseguridad donde simulo un entorno IT/OT para practicar
detección de amenazas y respuesta a incidentes.

---

## Arquitectura
[Kali Linux - 10.0.2.15] ── Atacante
│
[Red NAT - 10.0.2.0/24]
│
──────┴──────────────
│                   │
[Metasploitable 2]  [Ubuntu Server]
10.0.2.5            10.0.2.4
Víctima IT          Wazuh SIEM

---

## Tecnologías

| Herramienta | Rol |
|---|---|
| Kali Linux | Máquina atacante |
| Metasploitable 2 | Víctima IT vulnerable |
| Wazuh | SIEM |
| Nmap | Reconocimiento |
| Medusa | Fuerza bruta SSH |
| Wireshark | Análisis de tráfico |

---

## Contenido

| Carpeta | Descripción |
|---|---|
| `01-setup` | Configuración de VMs y red |
| `02-wazuh-siem` | Instalación y configuración de Wazuh |
| `03-ataques` | Ataques simulados y detección |
| `04-ot-modbus` | Pendiente — simulación entorno industrial |
| `05-informes` | Informes de incidentes |

---

## Autor

**Abdu** — ASIR, especialización ciberseguridad — IFP Barcelona
