# 01 — Setup del entorno

## Descripción
Configuración de las máquinas virtuales y la red aislada para el lab de ciberseguridad IT/OT.

## VMs creadas

| VM | OS | RAM | IP |
|---|---|---|---|
| kali-linux-2025.4 | Kali Linux 2025.4 | 4GB | 10.0.2.15 |
| Wazuh-Server | Ubuntu Server 22.04 | 4GB | 10.0.2.4 |
| Metasploitable2 | Ubuntu 8.04 (vulnerable) | 512MB | 10.0.2.5 |

## Red NAT — SOC-LAB-NET
Red NAT personalizada creada con VBoxManage para aislar el lab del resto de la red física.

- Red: `10.0.2.0/24`
- Gateway: `10.0.2.1`
- DHCP: activo
- Herramienta: `VBoxManage natnetwork add`

## Verificación de conectividad
Ping entre Kali y Wazuh-Server: ✅ 0% packet loss  
Ping entre Kali y Metasploitable: ✅ 0% packet loss

---

## Capturas

**Creación de SOC-LAB-NET:**

![NAT Network](https://github.com/user-attachments/assets/a0d2ff56-3e59-4bee-aa33-716d4f04dc48)

**Configuración de red en ambas VMs:**

![Network Config](https://github.com/user-attachments/assets/a5723900-459d-4b8c-ba22-cd04cd56fa24)

**IP asignada a Kali (10.0.2.15):**

![IP Kali](https://github.com/user-attachments/assets/6e89f50d-5071-443a-b5d1-18ee9d7f0568)

**IP asignada a Wazuh-Server (10.0.2.4):**

![IP Wazuh](https://github.com/user-attachments/assets/edbd43ee-3fea-4803-970a-f14c63914d4c)

**Verificación de conectividad:**

![Ping](https://github.com/user-attachments/assets/9d511980-df5b-4af5-adf1-77de585d17b8)







