# 📊 Análise de Conciliação Contábil com Python

Este projeto realiza a **análise e conciliação de dados contábeis** utilizando **Python e Pandas**, automatizando a comparação entre valores de **débito e crédito** a partir de planilhas Excel.

O objetivo é identificar registros em que os valores **conferem entre si** e destacar essas linhas automaticamente em um arquivo Excel final.

---

# 🚀 Tecnologias Utilizadas

- Python
- Pandas
- XlsxWriter
- Jupyter Notebook / Script Python
- Excel

---

# 📂 Estrutura dos Dados

O projeto utiliza uma planilha contendo as seguintes colunas principais:

| Coluna | Descrição |
|------|------|
| DATA | Data do lançamento |
| Nº DA CONTA | Número da conta contábil |
| CC. | Centro de custo |
| DESCRIÇÃO DA CONTA | Descrição da conta |
| DESCRIÇÃO DA CONTA.1 | Histórico ou identificação da nota |
| DÉBITO (+) | Valor debitado |
| CRÉDITO (+) | Valor creditado |
| SALDO ATUAL | Saldo após lançamento |
| HISTÓRICO | Histórico do lançamento |

---

# ⚙️ Funcionamento do Projeto

O script executa as seguintes etapas:

### 1️⃣ Leitura da planilha Excel

Os dados são carregados para um **DataFrame do Pandas**.

### 2️⃣ Tratamento dos dados

- Conversão das colunas de **débito e crédito para valores numéricos**
- Limpeza de possíveis inconsistências

### 3️⃣ Agrupamento de créditos

Os valores de crédito são agrupados por:

- `DATA`
- `DESCRIÇÃO DA CONTA.1`

Somando os valores correspondentes.

### 4️⃣ Comparação de valores

O sistema verifica se:

Quando os valores são iguais, a linha é marcada como **conferida**.

### 5️⃣ Geração do relatório Excel

O script gera um **arquivo Excel final** onde:

- As linhas que conferem são **destacadas em amarelo**
- Facilita a análise contábil e auditoria dos dados

---

# 📈 Exemplo de Resultado

| DATA | DESCRIÇÃO | DÉBITO | CRÉDITO | STATUS |
|-----|-----|-----|-----|-----|
| 01/01/2024 | NF 12345 | 1500 | 1500 | ✅ Conferido |
| 02/01/2024 | NF 67890 | 2000 | 1500 | ❌ Divergente |

As linhas **conferidas aparecem destacadas em amarelo no Excel**.

---

# ▶️ Como Executar o Projeto

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/Kennedy7Sa/seu-projeto.git


2️⃣ Instale as dependências
pip install pandas xlsxwriter openpyxl
3️⃣ Execute o script
python analise_conciliacao.py
📁 Saída do Projeto

O sistema gera automaticamente o arquivo:

resultado_conferencia.xlsx

Esse arquivo contém:

Todos os registros analisados

Linhas destacadas quando débito = crédito

🎯 Objetivo do Projeto

Este projeto demonstra como Python pode ser utilizado para automação de processos contábeis e análise de dados, reduzindo o trabalho manual e aumentando a confiabilidade das conferências financeiras.

📚 Aprendizados

Durante o desenvolvimento foram aplicados conceitos de:

Manipulação de dados com Pandas

Agrupamento de dados (groupby)

Comparação entre DataFrames

Geração automatizada de relatórios em Excel

Automação de análise contábil

👨‍💻 Autor

Desenvolvido por Kennedy S. Arruda

Python Developer

Data Analysis Enthusiast



