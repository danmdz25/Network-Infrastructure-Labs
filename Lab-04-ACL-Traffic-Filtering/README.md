# Lab 04: Inter-Network Traffic Control with Standard ACLs 🛡️🚦

[For English version, click here](#english-version-section)

## 🇧🇷 Português

### 📝 Descrição
Este laboratório foca na implementação de **ACLs Standard (Listas de Controle de Acesso Padrão)** para gerenciar a comunicação entre diferentes segmentos de uma rede interna. O cenário demonstra como restringir o acesso de hosts específicos de uma sub-rede (192.168.1.0/24) ao tentar alcançar um destino em outra sub-rede (192.168.2.0/24), utilizando políticas de filtragem aplicadas no roteador.

### 🛠️ Tecnologias e Implementações
* **ACL Standard (Lista 1):** Configurada para realizar filtragem seletiva baseada no endereço IP de origem.
* **Restrição de Acesso Inter-Redes:** Implementação do comando `deny host` para vetar a comunicação do host **192.168.1.2** com a rede de destino, enquanto permite o acesso do host **192.168.1.3** via comando `permit host`.
* **Posicionamento Estratégico:** A ACL foi aplicada no sentido `out` da interface **GigabitEthernet 0/2** (interface de saída para a rede de destino), seguindo a boa prática de colocar ACLs Standard o mais próximo possível do destino.
* **Documentação In-Line:** Uso do comando `remark` para identificação clara da política de segurança no arquivo de configuração.
* **Verificação de Interface:** Uso do comando `show ip interface Gig0/2` para validar a aplicação da lista de acesso de saída.

### 🔍 Visão de Cibersegurança
A filtragem de tráfego inter-redes é um pilar da micro-segmentação:
1. **Zonamento de Segurança:** Permite isolar departamentos ou dispositivos sensíveis, garantindo que apenas hosts autorizados atravessem as fronteiras do roteador.
2. **Prevenção de Movimentação Lateral:** Limitar quem pode comunicar com redes críticas reduz o raio de alcance de um potencial invasor em caso de comprometimento de um host local.

---

## 📂 Arquivos no Repositório
* `Lab-04_ACL.pkt`: Arquivo de simulação do Cisco Packet Tracer.
* `Lab-04-Topology.png`: Diagrama visual da rede detalhando as interfaces Gig0/1 e Gig0/2.
* `Relatorio_ACL_InterRedes_Lab04_ACL_InterNetwork_Report_Lab04.pdf`: Relatório técnico detalhado com comandos e evidências de verificação (Bilingue).

---

<br>

<a name="english-version-section"></a>

## 🇺🇸 English Version

### 📝 Description
This lab focuses on the implementation of **Standard ACLs (Access Control Lists)** to manage communication between different internal network segments. The scenario demonstrates how to restrict access from specific hosts in one subnet (192.168.1.0/24) when attempting to reach a destination in another subnet (192.168.2.0/24), using filtering policies applied on the router.

### 🛠️ Technologies and Implementations
* **Standard ACL (List 1):** Configured for selective filtering based on the source IP address.
* **Inter-Network Access Restriction:** Implementation of the `deny host` command to veto communication from host **192.168.1.2** to the target network, while allowing host **192.168.1.3** via the `permit host` command.
* **Strategic Placement:** The ACL was applied in the `out` direction of the **GigabitEthernet 0/2** interface (the exit interface to the destination network), following the best practice of placing Standard ACLs as close to the destination as possible.
* **In-Line Documentation:** Use of the `remark` command to clearly identify the security policy within the configuration file.
* **Interface Verification:** Use of the `show ip interface Gig0/2` command to validate the outbound access-list application.

### 🔍 Cybersecurity Perspective
Inter-network traffic filtering is a cornerstone of micro-segmentation.
1. **Security Zoning:** Allows isolating departments or sensitive devices, ensuring only authorized hosts cross router boundaries.
2. **Lateral Movement Prevention:** Limiting who can communicate with critical networks reduces the blast radius of a potential attacker.

---

## 📂 Repository Files
* `Lab-04_ACL.pkt`: Cisco Packet Tracer simulation file.
* `Lab-04-Topology.png`: Visual network diagram detailing Gig0/1 and Gig0/2 interfaces.
* `Relatorio_ACL_InterRedes_Lab04_ACL_InterNetwork_Report_Lab04.pdf`: Detailed technical report with commands and verification evidence (Bilingual).

---

**Mantido por / Maintained by:** Daniel Mendes (@danmdz25)
