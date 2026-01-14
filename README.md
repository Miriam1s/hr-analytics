# 📊 Análise de RH – Produtividade, Satisfação e Risco de Churn

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo analisar dados de Recursos Humanos para compreender os fatores que influenciam a **satisfação**, **produtividade** e o **risco de saída (churn)** dos funcionários. A análise busca gerar **insights acionáveis** que possam apoiar decisões estratégicas do RH.

---

## 📂 Dataset

* **Fonte:** Kaggle
* **Contexto:** Dados sintéticos de RH
* **Formato:** CSV
* **Observação:** O dataset não contém churn real. Foi criada uma **variável proxy de risco de churn** baseada na taxa de satisfação.

### Principais variáveis:

* `age` – idade do funcionário
* `department` – departamento
* `position` – cargo
* `salary` – salário
* `projects_completed` – projetos concluídos
* `productivity_percent` – produtividade (%)
* `satisfaction_rate_percent` – satisfação (%)
* `feedback_score` – avaliação de feedback
* `joining_date` – data de entrada na empresa

---

## 🗂️ Estrutura do Projeto

```
analise-rh/
├── data/
│   ├── raw/              # dados brutos
│   └── processed/        # dados tratados
├── notebooks/
│   └── 01_eda.ipynb      # análise exploratória e modelagem
├── reports/
│   └── figures/          # gráficos gerados
├── src/                  # scripts auxiliares (futuro)
├── requirements.txt
└── README.md
```

---

## 🔍 Metodologia

1. **Limpeza e padronização dos dados**

   * Padronização de nomes de colunas
   * Conversão de datas no formato original (`Jan-20`)

2. **Análise Exploratória de Dados (EDA)**

   * Estatísticas descritivas
   * Análise de satisfação e produtividade
   * Comparações por departamento
   * Relação entre tempo de empresa, salário e satisfação

3. **Dashboards Analíticos**

   * KPIs gerais
   * Satisfação por departamento
   * Produtividade × Satisfação
   * Tempo de empresa × Satisfação

4. **Modelo de Risco de Churn (Proxy)**

   * Definição de risco com base em satisfação < 50%
   * Regressão Logística
   * Avaliação com métricas de classificação

---

## 📈 Principais Insights

* A correlação entre **produtividade e satisfação é muito fraca**, indicando que funcionários produtivos não são necessariamente mais satisfeitos.
* A **satisfação varia significativamente entre departamentos**, sugerindo oportunidades de ações direcionadas de RH.
* O **tempo de empresa não apresenta relação linear forte com satisfação**, indicando possíveis fatores externos como cultura, liderança e reconhecimento.
* O modelo de churn indica que **satisfação e feedback** têm maior impacto no risco de saída do que produtividade isolada.

---

## 🤖 Modelo de Machine Learning

* **Tipo:** Classificação binária
* **Modelo:** Regressão Logística
* **Variável alvo:** `churn_risk` (proxy)
* **Principais features:**

  * satisfação
  * feedback
  * tempo de empresa
  * salário

O modelo foi escolhido por sua **interpretabilidade**, fundamental em contextos de RH.

---

## 🛠️ Tecnologias Utilizadas

* Python 3.11
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 🚀 Como Executar o Projeto

```bash
pip install -r requirements.txt
jupyter notebook
```

Abra o notebook `01_eda.ipynb` para visualizar toda a análise.

---

## 📌 Próximos Passos

* Criar um dashboard interativo (Power BI / Streamlit)
* Testar outros modelos de churn
* Incluir variáveis de clima organizacional

---

## 📬 Contato

Projeto desenvolvido para fins de estudo e portfólio em **Análise de Dados**.
