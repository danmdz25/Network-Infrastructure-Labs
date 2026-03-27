# Network Infrastructure Labs 🌐🛡️

[For English version, click here](#english-version-section)

Bem-vindo ao meu repositório de laboratórios de infraestrutura de rede. Este espaço é dedicado à documentação e implementação de arquiteturas de rede fundamentais, servindo como base técnica para minha especialização em **Digital Forensics and Incident Response (DFIR)**.

> "Para investigar o que deu errado em uma rede, primeiro você deve ser capaz de construir e entender como ela funciona corretamente."

---

## 🎯 Objetivo
O foco deste repositório não é apenas configurar dispositivos, mas compreender a fundo o comportamento dos protocolos. Em segurança defensiva, o conhecimento de infraestrutura permite:
* **Identificar anomalias:** Diferenciar tráfego legítimo de protocolos mal-intencionados.
* **Mapear superfícies de ataque:** Entender como a segmentação protege ativos críticos.
* **Rastreabilidade:** Utilizar serviços como DHCP e Roteamento para reconstruir linhas do tempo (*timelines*) em incidentes.

---

### 🔹 [Lab 01: IPv6 & OSPFv3 Core](./Lab-01-IPv6-OSPFv3)
Implementação de um backbone de rede utilizando endereçamento IPv6 e roteamento dinâmico. 
* **Foco:** Interconectividade entre roteadores e redundância.
* **Visão DFIR:** Análise de integridade de tabelas de roteamento e prevenção de ataques de redirecionamento de tráfego.

### 🔹 [Lab 02: Enterprise Segmentation (VLAN + DHCP)](./Lab-02-VLAN-DHCP)
**Este é um projeto integrado** que simula uma rede corporativa completa com segmentação de departamentos e automação de endereçamento.
* **Foco:** Configuração de Switches (VLANs/Trunking) e Roteador (Router-on-a-Stick + DHCP Pool).
* **Visão DFIR:** Rastreabilidade de ativos através de logs DHCP e isolamento de incidentes via segmentação de Camada 2.

---

## 🛠️ Stack Tecnológica
* **Simuladores:** Cisco Packet Tracer.
* **Sistemas:** Cisco IOS.
* **Protocolos:** OSPFv3, IPv6, IEEE 802.1Q (Trunking), DHCP, ICMP.

---

## 🔍 Por que Redes para DFIR?
A compreensão profunda da infraestrutura permite que um analista de resposta a incidentes possa:
1. **Mapear o Fluxo:** Entender por onde o tráfego de um atacante passou.
2. **Coletar Evidências:** Saber quais dispositivos (Switches ou Roteadores) detêm as informações de conexão (ARP, MAC, DHCP Leases).
3. **Contenção:** Saber como isolar portas ou VLANs para impedir a propagação de malwares.

---
**Mantido por:** Daniel Mendes (@danmdz25)  
*Foco em Cibersegurança | IT Support | DFIR Student*

---

<br>

<a name="english-version-section"></a>
# Network Infrastructure Labs 🌐🛡️ (English Version) 🇺🇸

Welcome to my repository of network infrastructure labs. This space is dedicated to documenting and implementing fundamental network architectures, serving as the technical foundation for my specialization in **Digital Forensics and Incident Response (DFIR)**.

> “To investigate what went wrong in a network, you must first be able to build and understand how it works correctly.”

---

## 🎯 Objective
The focus of this repository is not just on configuring devices, but on deeply understanding protocol behavior. In defensive security, infrastructure knowledge allows you to:
* **Identify anomalies:** Distinguish legitimate traffic from malicious protocols.
* **Map attack surfaces:** Understand how segmentation protects critical assets.
* **Traceability:** Use services such as DHCP and Routing to reconstruct incident timelines.

---

### 🔹 [Lab 01: IPv6 & OSPFv3 Core](./Lab-01-IPv6-OSPFv3)
Implementation of a network backbone using IPv6 addressing and dynamic routing. 
* **Focus:** Interconnectivity between routers and redundancy.
* **DFIR Perspective:** Analysis of routing table integrity and prevention of traffic redirection attacks.

### 🔹 [Lab 02: Enterprise Segmentation (VLAN + DHCP)](./Lab-02-VLAN-DHCP)
**This is an integrated project** that simulates a complete corporate network with departmental segmentation and address automation.
* **Focus:** Switch configuration (VLANs/Trunking) and Router configuration (Router-on-a-Stick + DHCP Pool).
* **DFIR Perspective:** Asset traceability through DHCP logs and incident isolation via Layer 2 segmentation.

---

## 🛠️ Technology Stack
* **Simulators:** Cisco Packet Tracer.
* **Systems:** Cisco IOS.
* **Protocols:** OSPFv3, IPv6, IEEE 802.1Q (Trunking), DHCP, ICMP.

---

## 🔍 Why Networks for DFIR?
A deep understanding of the infrastructure allows an incident response analyst to:
1. **Map the Flow:** Understand where an attacker’s traffic has passed through.
2. **Collect Evidence:** Know which devices (switches or routers) hold connection information (ARP, MAC, DHCP leases).
3. **Containment:** Know how to isolate ports or VLANs to prevent the spread of malware.

---
**Maintained by:** Daniel Mendes (@danmdz25)  
*Focus on Cybersecurity | IT Support | DFIR Student*
