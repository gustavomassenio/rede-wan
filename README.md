# rede-wan
Uma rede WAN entre São Paulo e Rio de Janeiro e depois uma rede mais complexa ligando multiplos estados.


# 🌐 Projeto de Rede WAN com Múltiplas Filiais

## 📌 Descrição

Este projeto simula a comunicação entre diferentes unidades de uma empresa distribuídas geograficamente, utilizando uma infraestrutura de rede **WAN (Wide Area Network)**.

A topologia representa uma **matriz localizada em São Paulo** e diversas **filiais interligadas por enlaces seriais**, simulando conexões reais entre cidades/estados.

O ambiente foi desenvolvido no **Cisco Packet Tracer**, com foco em roteamento, segmentação de rede e comunicação entre LANs remotas.

---

## 🏗️ Topologia da Rede

A rede é composta por:

* 5 roteadores interligados via conexões seriais
* 5 redes locais (LANs), uma em cada unidade
* Switches para distribuição local
* Hosts (PCs) para testes de conectividade

### 🔗 Estrutura:

* **Router SP (Matriz)**

  * LAN: `192.168.10.0/24`
* **Router RJ**

  * LAN: `192.168.90.0/24`
* **Router MG**

  * LAN: `192.168.80.0/24`
* **Router BA**

  * LAN: `192.168.70.0/24`
* **Router AC**

  * LAN: `192.168.60.0/24`

---

## 🌍 Comunicação WAN

Os roteadores estão conectados por interfaces seriais utilizando redes ponto-a-ponto:

| Link    | Rede       |
| ------- | ---------- |
| SP ↔ RJ | 20.0.0.0/8 |
| RJ ↔ MG | 30.0.0.0/8 |
| MG ↔ BA | 40.0.0.0/8 |
| BA ↔ AC | 50.0.0.0/8 |

Cada enlace possui controle de clock (DCE/DTE) e limitações de banda simuladas:

* 256 kbps
* 128 kbps
* 512 kbps

---

## ⚙️ Tecnologias Utilizadas

* Roteadores Cisco (modelo 2621XM)
* Switches 2960
* Endereçamento IPv4
* Máscara /24 para LANs
* Máscara /8 para enlaces WAN
* Interfaces seriais (DCE/DTE)
* Simulação no Cisco Packet Tracer

---

## 🔁 Funcionamento

Cada filial possui sua própria rede local (LAN), e a comunicação entre elas ocorre através dos roteadores utilizando a WAN.

Exemplo:

* Um computador na rede `192.168.10.0/24` (SP) pode se comunicar com outro na rede `192.168.60.0/24` (AC) através dos roteadores intermediários.

---

## 🧪 Testes Realizados

* ✔️ Ping entre todas as redes
* ✔️ Verificação de rotas
* ✔️ Teste de conectividade ponta a ponta
* ✔️ Simulação de latência via controle de banda

---

## 📷 Topologia




## 📷 Topologia

![Topologia WAN](redewancompleta.png)


---

## 🚀 Possíveis Melhorias

* Implementar protocolos de roteamento dinâmico (OSPF, RIP ou EIGRP)
* Adicionar redundância de links
* Implementar VLANs nas LANs
* Aplicar QoS (Quality of Service)
* Simular falhas de link

---

## 📚 Objetivo Acadêmico

Este projeto tem como objetivo demonstrar:

* Funcionamento de redes WAN
* Interligação de múltiplas LANs
* Configuração básica de roteadores
* Comunicação entre diferentes localidades

---

## 👨‍💻 Autor

Projeto desenvolvido para fins de estudo em redes de computadores.
