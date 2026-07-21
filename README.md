# IASC Benchmarking & Analytics — Satisfação dos Consumidores (ANEEL)

Este repositório contém uma solução em Python para extração, tratamento, análise longitudinal e visualização de dados do **IASC (Índice ANEEL de Satisfação do Consumidor)**, cobrindo o período de 2016 a 2025.

O projeto realiza o benchmarking comparativo entre grandes distribuidoras de energia elétrica (**Copel-Dis**, **Enel SP**, **Energisa Sul-Sudeste** e **Neoenergia Coelba**), além de aprofundar a análise de produto na Copel-Dis para mapear perfis críticos de consumidores e quesitos de qualidade percebida.

---

## 📌 Funcionalidades

- **Pipeline de Carga Robusto**: Leitura automatizada de arquivos `.xlsm` da ANEEL com suporte a busca insensível a acentuação e caixa nas abas.
- **Benchmarking de Distribuidoras (2016–2025)**:
  - Evolução do índice IASC ao longo de 10 anos.
  - Comparativo detalhado dos quesitos de qualidade (Qualidade Percebida, Satisfação, Fidelidade, Valor e Confiança) e itens específicos de atendimento.
- **Painel Analítico Copel-Dis (Foco em Produto)**:
  - **Top 5 Perfis Críticos**: Mapeamento dos segmentos demográficos (Gênero, Faixa Etária, Escolaridade e Renda) com menor satisfação.
  - **Quesitos de Qualidade Percebida**: Diagnóstico dos pontos fortes e de atenção (Continuidade, Faturamento, Atendimento, Preço).
  - **Evolução Ano a Ano (2023–2025)**: Variação percentual longitudinal dos índices oficiais.
  - **Representatividade Geográfica**: Distribuição da amostra de respondentes por município paranaense.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Pandas**: Leitura, higienização, mapeamento de códigos técnicos para nomes de negócio e agregação de dados.
- **Matplotlib & Seaborn**: Construção de dashboards e painéis visuais customizados.
- **OpenPyXL**: Engine para processamento das planilhas em formato Excel (`.xlsm`).
- **Pathlib & Unicodedata**: Manipulação segura de caminhos de arquivos e normalização de texto.

---

## 📂 Estrutura do Repositório

```text
├── Dados/                                  # Pasta para armazenamento das bases oficiais (.xlsm)
│   ├── Dados_Copel_Dis_Dados_2025.xlsm
│   ├── Dados_Enel_São_Paulo_2025.xlsm
│   ├── Dados_Energisa_Sul_Sudeste_2025.xlsm
│   └── Dados_Neoenergia_Coelba_2025.xlsm
├── outputs/                                # Diretório de saída dos gráficos e painéis gerados
│   ├── dashboard_iasc_2025.png             # Dashboard comparativo de distribuidoras
│   └── iasc_copel_painel.png               # Painel analítico de produto Copel-Dis
├── dashboard_benchmarking.py              # Script de benchmarking entre distribuidoras
├── painel_copel_analytics.py              # Script de análise detalhada da Copel-Dis
└── README.md                               # Documentação do projeto
