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

## Capturas
- `01-nat-network.png` — Creación de SOC-LAB-NET por CMD
<img width="969" height="398" alt="{FE83A923-EA67-463E-AC8F-6F4CD1A7F32E}" src="https://github.com/user-attachments/assets/a0d2ff56-3e59-4bee-aa33-716d4f04dc48" />
- `02-network-config.png` — Configuración de red en ambas VMs
<img width="857" height="294" alt="{7EBBEA40-FAA2-499B-A1CD-BA86B2B56DA7}" src="https://github.com/user-attachments/assets/a5723900-459d-4b8c-ba22-cd04cd56fa24" />
<img width="861" height="260" alt="{8120736B-6833-4381-B3EE-1D2B671833B3}" src="https://github.com/user-attachments/assets/b1e394ef-2415-4615-a5a1-73cc7ff543ea" />
- `03-ip-kali.png` — IP asignada a Kali (10.0.2.15)
<img width="623" height="267" alt="{629B4457-6AAD-4D83-8844-25A35EA0FBD8}" src="https://github.com/user-attachments/assets/6e89f50d-5071-443a-b5d1-18ee9d7f0568" />
- `04-ip-wazuh.png` — IP asignada a Wazuh-Server (10.0.2.4)
<img width="848" height="237" alt="{2B00E905-AA4C-4DBD-A9DA-98D0F8E6CFFB}" src="https://github.com/user-attachments/assets/edbd43ee-3fea-4803-970a-f14c63914d4c" />
- `05-ping.png` — Verificación de conectividad entre VMs
<img width="540" height="203" alt="{62E625EB-4A09-495B-89C0-B8EF3FAF5584}" src="https://github.com/user-attachments/assets/9d511980-df5b-4af5-adf1-77de585d17b8" />







