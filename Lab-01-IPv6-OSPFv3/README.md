# Lab 01: IPv6 & OSPFv3 Core Architecture 🌐

[For English version, click here](#english-version)

## 🇵🇹 Português

### 📝 Descrição
Este laboratório foca-se na implementação de uma infraestrutura de rede utilizando **IPv6** e o protocolo de roteamento dinâmico **OSPFv3**. O cenário simula a interconectividade de um backbone onde a redundância e a rápida convergência são essenciais.



### 🛠️ Configurações Realizadas
- **Endereçamento IPv6:** Implementação de prefixos `/126` para links ponto-a-ponto e `/128` para interfaces Loopback.
- **OSPFv3:** Ativação do processo de roteamento, definição de **Router IDs** e associação de interfaces à **Área 0 (Backbone)**.
- **Interfaces Loopback:** Configuradas para garantir a estabilidade do Router ID e acessibilidade de gestão.

### 🔍 Visão Forense (DFIR Perspective)
Como analista forense, a compreensão deste laboratório permite:
1. **Verificação de Adjacência:** Monitorizar se novos vizinhos OSPF foram adicionados indevidamente (potencial *Rogue Router*).
2. **Análise de Tabela de Roteamento:** Identificar rotas injetadas que podem desviar o tráfego para um ponto de interceção (*Man-in-the-Middle*).
3. **Integridade do Router ID:** Confirmar se os IDs de roteador correspondem ao inventário oficial da rede durante a análise de logs.

---

## 📂 Arquivos no Repositório
- `router_ipv6 - OSPF.pkt`: Arquivo do Cisco Packet Tracer.
- `Relatório de Configuração_ Topologia IPv6 com OSPFv3 _ Configuration Report_ IPv6 Topology with OSPFv3.pdf`: Relatório de todos os comandos utilizados.

---

<br>
<a name="english-version"></a>

## 🇺🇸 English Version

### 📝 Description
This lab focuses on implementing a network infrastructure using **IPv6** and the **OSPFv3** dynamic routing protocol. The scenario simulates a backbone interconnectivity where redundancy and fast convergence are essential.

### 🛠️ Configurations Implemented
- **IPv6 Addressing:** Implementation of `/126` prefixes for point-to-point links and `/128` for Loopback interfaces.
- **OSPFv3:** Activation of the routing process, definition of **Router IDs**, and association of interfaces with **Area 0 (Backbone)**.
- **Loopback Interfaces:** Configured to ensure Router ID stability and management accessibility.

### 🔍 DFIR Perspective
As a forensic analyst, understanding this lab allows for:
1. **Adjacency Verification:** Monitoring if new OSPF neighbors were improperly added (potential *Rogue Router*).
2. **Routing Table Analysis:** Identifying injected routes that could divert traffic to an interception point (*Man-in-the-Middle*).
3. **Router ID Integrity:** Confirming if router IDs match the official network inventory during log analysis.

---
## 📂 Files in the Repository
- `router_ipv6 - OSPF.pkt`: Cisco Packet Tracer file.
- `Relatório de Configuração_ Topologia IPv6 com OSPFv3 _ Configuration Report_ IPv6 Topology with OSPFv3.pdf`: Report of all commands used.
---

**Mantido por / Maintained by:** Daniel Mendes (@danmdz25)
