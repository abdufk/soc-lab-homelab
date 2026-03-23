# 🛡️ SOC Home Lab — IT/OT Security

![Status](https://img.shields.io/badge/Status-En%20progreso-yellow)
![SIEM](https://img.shields.io/badge/SIEM-Wazuh-blue)
![Attacker](https://img.shields.io/badge/Attacker-Kali%20Linux-red)
![OT](https://img.shields.io/badge/OT-Modbus%20%2F%20PyModbus-orange)

Proyecto personal de ciberseguridad donde simulo un entorno IT/OT real para practicar 
detección de amenazas, respuesta a incidentes y seguridad industrial.

Inspirado en el enfoque de empresas como **infraone**, especializadas en protección 
de infraestructuras críticas.

---

## 🎯 Objetivos

- Montar un lab funcional con zonas IT y OT separadas
- Detectar ataques reales usando un SIEM (Wazuh)
- Simular un entorno industrial con protocolo Modbus
- Documentar incidentes siguiendo un formato profesional SOC
- Entender las diferencias entre seguridad IT tradicional y entornos OT

---

## 🏗️ Arquitectura del lab
```
[Kali Linux] ──── Atacante
      │
  [Red NAT - VirtualBox - 10.0.2.0/24]
      │
   ───┴───────────────────────
   │                          │
[Metasploitable 2]     [Ubuntu Server]
  Víctima IT             Wazuh SIEM
                              │
                    [VM OT - PyModbus]
                     PLC simulado
```

---

## 🧰 Tecnologías utilizadas

| Herramienta | Rol | Categoría |
|---|---|---|
| Kali Linux | Máquina atacante | Offensive |
| Metasploitable 2 | Víctima IT vulnerable | Target |
| Wazuh | SIEM — correlación y alertas | Defensive |
| Nmap | Escaneo y reconocimiento | Recon |
| Hydra | Fuerza bruta SSH | Attack |
| Metasploit | Explotación controlada | Exploit |
| PyModbus | Simulación PLC/OT | Industrial |
| Wireshark | Análisis de tráfico | Forensics |

---

## 📁 Estructura del repositorio

| Carpeta | Contenido |
|---|---|
| `01-setup` | Configuración de VMs y red |
| `02-wazuh-siem` | Instalación y config de Wazuh |
| `03-ataques` | Simulación de ataques y capturas |
| `04-ot-modbus` | Entorno industrial simulado |
| `05-informes` | Informes de incidentes formato SOC |

---

## 📌 Estado del proyecto

- [x] Kali Linux configurado
- [x] Ubuntu Server (Wazuh) configurado
- [ ] Metasploitable 2 importado
- [ ] Red NAT configurada entre VMs
- [ ] Wazuh instalado y operativo
- [ ] Primer ataque simulado y detectado
- [ ] Entorno OT con Modbus funcional
- [ ] Informe de incidente documentado

---

## 👤 Autor

**Abdu** — Estudiante ASIR, especialización ciberseguridad  
IFP Barcelona
