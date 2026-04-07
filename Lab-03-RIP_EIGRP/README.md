# Lab 03: Dynamic Routing Protocols (RIPv2 + EIGRP) 🌐🛡️

[For English version, click here](#english-version-section)

## 🇧🇷 Português

### 📝 Descrição
Este laboratório foca na implementação e comparação de protocolos de roteamento dinâmico em uma infraestrutura IPv4. A topologia utiliza três roteadores interconectados para demonstrar a convergência de rede, a seleção do melhor caminho e a convivência de múltiplos protocolos (**RIPv2** e **EIGRP**) em um mesmo ambiente.

### 🛠️ Tecnologias e Implementações
* **RIPv2 (Routing Information Protocol):** Configuração de roteamento baseado em vetor de distância, utilizando a Versão 2 para suporte a VLSM e redes sem classe.
* **EIGRP (Enhanced Interior Gateway Routing Protocol):** Implementação de um protocolo avançado com Sistema Autônomo (**AS 100**), destacando sua métrica composta (banda e atraso) e convergência rápida.
* **Seleção de Rota & AD:** Demonstração prática do conceito de **Distância Administrativa (AD)**. O comando `show ip route` revela que o roteador prioriza o **EIGRP (AD 90)** sobre o **RIP (AD 120)** por ser considerado um protocolo mais confiável.
* **Conectividade IPv4:** Endereçamento de interfaces GigabitEthernet e simulação de redes locais (LANs) em cada roteador.

### 💡 Desafios e Aprendizados Técnicos
* **Persistência de Dados:** Importância da execução do comando `copy running-config startup-config` para evitar a perda de configurações após reinicializações.
* **Interpretação da Tabela de Roteamento:** Identificação de rotas diretamente conectadas (**C**), locais (**L**) e aprendidas dinamicamente via EIGRP (**D**).
* **Convergência Dinâmica:** Observação das mensagens de log `%DUAL-5-NBRCHANGE` que confirmam a formação de adjacência imediata entre vizinhos EIGRP.

### 🔍 Visão Forense (DFIR Perspective)
A análise de protocolos de roteamento dinâmico é essencial para a segurança e investigação:
1.  **Envenenamento de Rotas (Route Poisoning):** A falta de autenticação robusta nativa no RIPv2 pode permitir que um atacante insira rotas falsas para desviar o tráfego (*Man-in-the-Middle*).
2.  **Análise de Adjacência:** Logs de EIGRP (*Neighbor Change*) são evidências valiosas para identificar quando um novo dispositivo tentou se conectar à infraestrutura.
3.  **Mapeamento de Topologia:** Tabelas de roteamento permitem que investigadores reconstruam a topologia lógica da rede durante a análise de um incidente de movimentação lateral.

---

## 📂 Arquivos no Repositório
* `RIP_EIGRP.pkt`: Arquivo de simulação do Cisco Packet Tracer.
* `Lab-03-RIP_EIGRP.png`: Diagrama visual da topologia da rede.
* `Relatório_Configuração_RIP_EIGRP.md`: Documento com os comandos detalhados e tabelas de roteamento formatadas.

---

<br>

<a name="english-version-section"></a>

## 🇺🇸 English Version

### 📝 Description
This lab focuses on the implementation and comparison of dynamic routing protocols within an IPv4 infrastructure. The topology utilizes three interconnected routers to demonstrate network convergence, best-path selection, and the coexistence of multiple protocols (**RIPv2** and **EIGRP**) in the same environment.

### 🛠️ Technologies and Implementations
* **RIPv2 (Routing Information Protocol):** Configuration of distance-vector routing, using Version 2 for VLSM support and classless networks.
* **EIGRP (Enhanced Interior Gateway Routing Protocol):** Implementation of an advanced protocol with Autonomous System (**AS 100**), highlighting its composite metric and fast convergence.
* **Route Selection & AD:** Practical demonstration of the **Administrative Distance (AD)** concept. The `show ip route` command reveals that the router prioritizes **EIGRP (AD 90)** over **RIP (AD 120)**.
* **IPv4 Connectivity:** Configuration of GigabitEthernet interfaces and Local Area Network (LAN) simulation for each router.

### 🔍 DFIR Perspective
Analyzing dynamic routing protocols is essential for network security and investigations:
1.  **Route Poisoning:** Lack of robust native authentication in RIPv2 can allow an attacker to inject false routes to redirect traffic.
2.  **Adjacency Analysis:** EIGRP logs (*Neighbor Change*) are valuable evidence to identify unauthorized infrastructure changes.
3.  **Topology Mapping:** Routing tables allow investigators to reconstruct the logical network topology during incident analysis.

---

**Mantido por / Maintained by:** Daniel Mendes (@danmdz25)
