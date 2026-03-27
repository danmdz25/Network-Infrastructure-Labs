# Lab 02: Enterprise Segmentation (VLAN + DHCP) 🛡️

[For English version, click here](#english-version-section)

## 🇧🇷 Português

### 📝 Descrição
Este laboratório apresenta uma solução integrada de rede corporativa. Ele demonstra a segmentação de departamentos (ADM, Financeiro e RH) através de **VLANs**, interconectadas por um roteador no modelo **Router-on-a-Stick**, que também atua como servidor **DHCP** para automatizar o endereçamento da rede.



### 🛠️ Tecnologias e Implementações
- **Camada 2 (Switch):** Criação de VLANs, nomeação e atribuição de portas de acesso. Configuração de porta **Trunk (802.1Q)** para comunicação com o roteador.
- **Camada 3 (Router):** Configuração de subinterfaces lógicas para roteamento inter-VLAN.
- **Serviços:** Implementação de múltiplos **DHCP Pools** com exclusão de endereços de gateway e definição de DNS.

### 🔍 Visão Forense (DFIR Perspective)
A integração de VLANs com DHCP é um ponto crítico para a perícia digital:
1. **Rastreabilidade IP vs MAC:** Os logs de concessão DHCP (*bindings*) permitem correlacionar um incidente ocorrido em um IP específico a um endereço físico (MAC) de uma máquina em um determinado departamento.
2. **Isolamento de Ameaças:** A segmentação por VLANs impede que um malware em uma sub-rede (ex: RH) se espalhe lateralmente para outra (ex: Financeiro) sem passar pelas regras de controle do roteador.
3. **Ponto de Captura:** O link Trunk é o local ideal para implementar um *Port Mirroring* (SPAN) para monitorar o tráfego de toda a empresa.

---

## 📂 Arquivos no Repositório
- `pool_dhcp_and_vlan - trunking.pkt`: Arquivo de simulação do Cisco Packet Tracer.
- `Relatório de Configuração: VLANs e Acesso de Portas (Switch)`: Comandos detalhados do Switch.
- `Relatório de Configuração: DHCP e Inter-VLAN Routing`: Comandos detalhados do Roteador.

---

<br>
<a name="english-version-section"></a>

## 🇺🇸 English Version

### 📝 Description
This lab presents an integrated corporate network solution. It demonstrates department segmentation (Admin, Finance, and HR) through **VLANs**, interconnected by a router using the **Router-on-a-Stick** model, which also acts as a **DHCP** server to automate network addressing.

### 🛠️ Technologies and Implementations
- **Layer 2 (Switch):** VLAN creation, naming, and access port assignment. **Trunk (802.1Q)** port configuration for router communication.
- **Layer 3 (Router):** Logical subinterface configuration for inter-VLAN routing.
- **Services:** Implementation of multiple **DHCP Pools** with gateway address exclusions and DNS definition.

### 🔍 DFIR Perspective
The integration of VLANs with DHCP is a critical point for digital forensics:
1. **IP vs MAC Traceability:** DHCP lease logs (*bindings*) allow correlating an incident on a specific IP to a physical address (MAC) of a machine in a specific department.
2. **Threat Isolation:** VLAN segmentation prevents malware in one subnet (e.g., HR) from spreading laterally to another (e.g., Finance) without passing through the router's control rules.
3. **Capture Point:** The Trunk link is the ideal location to implement *Port Mirroring* (SPAN) to monitor traffic across the entire company.

---
## 📂 Files in the Repository
- `pool_dhcp_and_vlan - trunking.pkt`: Cisco Packet Tracer simulation file.
- `Configuration Report: VLANs and Port Access (Switch)`: Detailed switch commands.
- `Configuration Report: DHCP and Inter-VLAN Routing`: Detailed router commands.
---

**Mantido por / Maintained by:** Daniel Mendes (@danmdz25)
