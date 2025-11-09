# SimpleByte RFID – Sprint 2
### FIAP | Disruptive Architectures: IoT, IoB & Generative AI

---

## 🎯 Objetivo
Apresentar o protótipo funcional do **SimpleByte RFID**, demonstrando a leitura simulada de etiquetas RFID através do **Node-RED** e um dashboard interativo que representa o fluxo IoT da aplicação.

---

## 🧠 Contexto
O **SimpleByte RFID** surgiu da necessidade de aprimorar o controle de materiais cirúrgicos (OPME e instrumentais) em hospitais.  
Hoje, muitas instituições ainda utilizam inventários manuais ou baseados em código de barras, o que dificulta:
- A rastreabilidade de lotes e validade;
- O controle de movimentações e uso por procedimento;
- A redução de perdas e desvios;
- A visibilidade de estoque em tempo real.

O projeto une **IoT, IA Generativa e Analytics**, oferecendo um ecossistema inteligente que integra sensores RFID, base de dados Oracle e visualizações interativas.

---

## ⚙️ Tecnologias Utilizadas
- **Node-RED** – construção do fluxo IoT e simulação das leituras RFID  
- **Node-RED Dashboard** – painel visual interativo  
- **node-red-node-ui-table** – exibição das leituras em tabela  
- **JavaScript (Function Node)** – lógica de armazenamento e processamento  
- **JSON** – estrutura dos dados simulados  

---

## 🧩 Estrutura do Protótipo

[Inject: Simular leitura RFID] → [Function: Acumular leituras] → [UI Table: Leituras RFID]

yaml
Copiar código

- **Simular leitura RFID:** gera eventos com tag, zona e hora.  
- **Acumular leituras:** armazena as últimas leituras e envia ao painel.  
- **UI Table:** exibe os dados em tempo real no dashboard *SimpleByte RFID – Controle Cirúrgico*.

---

## 💻 Como Executar

1. Instale o **Node-RED** (https://nodered.org/)  
2. Execute o comando:
   ```bash
   node-red
Acesse no navegador:

bash
Copiar código
http://localhost:1880/ui
Clique no botão “Simular leitura RFID” para gerar novas leituras.

Cada clique adiciona uma linha com os campos:

Tag (EPC)

Zona

Hora

📊 Evidências
As capturas de tela estão disponíveis na pasta /prints:

dashboard.png – painel funcionando

fluxo.png – fluxo Node-RED completo

simulacao.png – leituras RFID sendo exibidas

📎 Estrutura do Repositório
css
Copiar código
simplebyte-rfid-sprint2/
│
├── README.md
├── DOCUMENTACAO_SPRINT2.md
│
├── node-red/
│   └── fluxo_simplebyte.json
│
├── prints/
│   ├── dashboard.png
│   ├── fluxo.png
│   └── simulacao.png
│
└── video.txt

👨‍💻 Integrantes
Nome	             RM
Gabriel dos Santos	560812
Bruno Tizer	        559999
Thomas Baute	    560649

🏁 Conclusão
O protótipo SimpleByte RFID demonstra, de forma funcional e visual, a arquitetura IoT proposta para rastreabilidade de materiais cirúrgicos.
Através do Node-RED, foi possível simular leituras RFID e exibi-las em tempo real, consolidando a etapa prática da Sprint 2 com êxito.