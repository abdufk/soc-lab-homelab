# SOC Home Lab — IT/OT Security

Proyecto personal de ciberseguridad donde simulo un entorno IT/OT para practicar
detección de amenazas y respuesta a incidentes.

---

## Arquitectura

| Máquina | IP | Rol |
|---|---|---|
| Kali Linux | 10.0.2.15 | Atacante |
| Ubuntu Server | 10.0.2.4 | Wazuh SIEM |
| Metasploitable 2 | 10.0.2.5 | Víctima IT |

Red NAT aislada: 10.0.2.0/24

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
| 01-setup | Configuración de VMs y red |
| 02-wazuh-siem | Instalación y configuración de Wazuh |
| 03-ataques | Ataques simulados y detección |
| 04-ot-modbus | Pendiente — simulación entorno industrial |
| 05-informes | Informes de incidentes |

---

## Autor

**Abdu** — ASIR, especialización ciberseguridad — IFP Barcelona
