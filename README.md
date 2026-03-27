# Network Infrastructure Labs 🌐🛡️

Este repositório contém documentações técnicas e laboratórios de configuração de redes, servindo como base fundamental para estudos em **Digital Forensics and Incident Response (DFIR)** e **Segurança de Rede**.

O objetivo aqui é documentar a implementação de protocolos de roteamento, segmentação de camada 2 e serviços de rede, compreendendo como o tráfego flui para melhor identificar anomalias e incidentes.



## 📁 Estrutura do Repositório

O projeto está dividido em módulos que cobrem desde a base do endereçamento até o roteamento dinâmico:

### 1. IPv6 & OSPFv3 Implementation
- **Foco:** Configuração de roteamento dinâmico em ambientes IPv6.
- **Destaque:** Implementação de Router IDs, interfaces Loopback e adjacências de rede.
- **Relevância para DFIR:** Entender a tabela de roteamento é crucial para identificar ataques de *Route Hijacking* ou desvios de tráfego maliciosos.

### 2. VLAN Segmentation & Access Control
- **Foco:** Criação de VLANs (Administração, Financeiro e RH) e atribuição de portas.
- **Destaque:** Configuração de portas de acesso e interfaces Trunk (802.1Q).
- **Relevância para DFIR:** A segmentação correta define o "Blast Radius" (raio de exposição) em um incidente. Investigar VLANs ajuda a mapear movimentos laterais de um atacante.

### 3. Inter-VLAN Routing & DHCP Services
- **Foco:** Configuração de subinterfaces (Router-on-a-Stick) e escopos DHCP.
- **Destaque:** Automação de endereçamento IP e roteamento entre redes distintas.
- **Relevância para DFIR:** Logs de DHCP são fontes de evidências críticas para correlacionar um endereço IP a um endereço MAC específico durante uma linha do tempo de ataque.

---

## 🛠️ Tecnologias e Ferramentas
- **Cisco IOS** (Comandos de configuração via CLI)
- **Protocolos:** OSPFv3, IPv6, IEEE 802.1Q (Trunking), DHCP.
- **Simuladores Sugeridos:** Cisco Packet Tracer / GNS3.

## 🚀 Como utilizar este material
Cada pasta contém um guia passo a passo com os comandos explicados. Você pode replicar as configurações em simuladores de rede para validar o comportamento do tráfego.

---

## 🔍 Conexão com Segurança e Forense
A base de qualquer investigação digital reside na compreensão da infraestrutura. Este repositório demonstra proficiência em:
- **Análise de Topologia:** Saber onde os ativos estão e como se comunicam.
- **Monitoramento de Fluxo:** Identificar pontos onde dispositivos de monitoramento (como IDS/IPS) devem ser posicionados.
- **Gestão de Evidências de Rede:** Compreender a origem de logs de roteadores e switches.

---
**Mantido por:** [Daniel Mendes/danmdz25]
*Foco em Cibersegurança | SOC Analyst | DFIR Student*
