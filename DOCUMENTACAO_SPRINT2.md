# DOCUMENTAÇÃO – SPRINT 2
## SimpleByte RFID | Disruptive Architectures: IoT, IoB & Generative AI

---

### 1. Introdução
O **SimpleByte RFID** é uma solução voltada à rastreabilidade e controle de materiais cirúrgicos (OPME e instrumentais) em hospitais.  
O sistema integra **RFID (IoT)**, **Analytics** e **IA Generativa**, permitindo inventário automatizado, auditoria inteligente e visibilidade ponta a ponta do estoque hospitalar.

Em muitos centros cirúrgicos, o controle de estoque ainda é manual ou baseado em código de barras, dificultando o acompanhamento de lotes, prazos de validade e movimentações de materiais entre o almoxarifado, as salas cirúrgicas e o CME.  
O SimpleByte busca solucionar esses desafios com um ecossistema conectado e inteligente.

---

### 2. Contexto e Problema
Os principais problemas identificados foram:
- **Falta de rastreabilidade**: não há registro automático de quem retirou o item, quando e para qual procedimento.  
- **Rupturas de estoque**: ausência de visibilidade em tempo real causa falta de materiais antes das cirurgias.  
- **Perdas por validade**: materiais vencem devido à falta de controle automatizado.  
- **Inventários lentos e manuais**: processos demorados e sujeitos a erros humanos.  
- **Pressão regulatória (ANVISA)**: necessidade de auditorias rápidas e confiáveis.  

O **SimpleByte RFID** surge para resolver esses pontos com automação e inteligência de dados.

---

### 3. Objetivo da Sprint 2
Desenvolver um **protótipo funcional** que demonstre o fluxo de leitura RFID em tempo real, utilizando **Node-RED** para simular a coleta, o processamento e a exibição das informações de forma automatizada.

---

### 4. Protótipo Desenvolvido
Foi implementado um **fluxo IoT completo** no **Node-RED**, responsável por simular leituras RFID e exibir os dados em um dashboard interativo.

**Fluxo criado:**
[Inject: Simular leitura RFID] → [Function: Acumular leituras] → [UI Table: Leituras RFID]

yaml
Copiar código

**Componentes:**
- **Inject:** gera dados simulados (tag, zona e hora);  
- **Function:** acumula as leituras recentes em um array e as envia para o painel;  
- **UI Table:** exibe as informações em tempo real no dashboard *SimpleByte RFID – Controle Cirúrgico*.

Cada clique no botão “Simular leitura RFID” adiciona uma nova leitura à tabela, demonstrando o conceito IoT e a atualização dinâmica dos dados.

---

### 5. Tecnologias Utilizadas
| Tecnologia | Função |
|-------------|--------|
| **Node-RED** | Criação do fluxo IoT e simulação das leituras |
| **Node-RED Dashboard** | Exibição visual das informações em tempo real |
| **node-red-node-ui-table** | Exibição de dados em formato de tabela |
| **JavaScript (Function Node)** | Lógica de armazenamento e processamento |
| **JSON** | Estrutura de comunicação dos dados |
| **IA Generativa (planejada)** | Explicação e auditoria automatizada em etapas futuras |

---

### 6. Funcionamento do Protótipo
1. O nó **Inject** simula a leitura de uma tag RFID contendo:
   - Código EPC da etiqueta;  
   - Zona de leitura (ex: Centro Cirúrgico);  
   - Horário do evento.
2. O nó **Function** processa e armazena as leituras em uma variável de fluxo.  
3. O nó **UI Table** atualiza automaticamente a interface visual, mostrando todas as leituras em tempo real.

**Dashboard:**  
- Título: *SimpleByte RFID – Controle Cirúrgico*  
- Grupo: *📡 Leituras em Tempo Real*  
- Colunas: *Tag (EPC)* | *Zona* | *Hora*  

---

### 7. Evidências
O painel e o fluxo do Node-RED foram capturados em três imagens:  
- `prints/dashboard.png` – Interface do painel com a tabela de leituras;  
- `prints/fluxo.png` – Estrutura completa do fluxo no Node-RED;  
- `prints/simulacao.png` – Leituras RFID sendo atualizadas em tempo real.  

Essas imagens comprovam o funcionamento do protótipo da Sprint 2.

---

### 8. Resultados Obtidos
- Protótipo IoT completo e funcional;  
- Dashboard estilizado com visual profissional;  
- Simulação de leituras RFID com atualização dinâmica;  
- Base técnica para integração com banco de dados e IA futura;  
- Entrega visual e prática da arquitetura IoT proposta.  

---

### 9. Conclusão
A Sprint 2 consolidou a etapa prática do projeto **SimpleByte RFID**, demonstrando o funcionamento de uma arquitetura IoT real com simulação de leituras RFID.  
O uso do **Node-RED** permitiu representar de forma clara a coleta, o processamento e a exibição das informações em tempo real.  
Com isso, a equipe validou a viabilidade técnica e apresentou um protótipo funcional alinhado aos objetivos da disciplina.

---

### 10. Integrantes

| Nome | RM |
|------|----|
| **Gabriel dos Santos** | 560812 |
| **Bruno Tizer** | 559999 |
| **Thomas Baute** | 560649 |

---

### 11. Referências
- [Node-RED](https://nodered.org/)  
- [Oracle Cloud Infrastructure](https://www.oracle.com/cloud/)  
- [Oracle IoT Services](https://www.oracle.com/internet-of-things/)  
- [W3C – Web A