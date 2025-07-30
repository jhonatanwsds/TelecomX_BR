# Análise Preditiva de Churn de Clientes - Telecom X

![Análise de Dados](https://img.shields.io/badge/Análise_de_Dados-Python-blue)
![Ciência de Dados](https://img.shields.io/badge/Ciência_de_Dados-Machine_Learning-orange)
![Business Intelligence](https://img.shields.io/badge/Business-Strategy-green)

---

## 1. Contexto de Negócio

A evasão de clientes, ou **Churn**, é uma das métricas mais críticas para empresas de serviços recorrentes. De acordo com estudos de gestão de negócios, o Custo de Aquisição de Cliente (CAC) é, em média, **5 a 25 vezes maior** do que o custo de retenção. Portanto, uma estratégia de negócio *data-driven* que visa minimizar o Churn tem um impacto direto e significativo na lucratividade da empresa.

Este projeto se propõe a resolver este problema através da aplicação de técnicas de **Análise de Dados** e **Ciência de Dados**, transformando dados brutos em insights estratégicos e acionáveis.

> **Objetivo Principal:** Identificar os principais fatores (drivers) que influenciam a decisão de um cliente cancelar o serviço, permitindo que a empresa passe de uma postura reativa para uma **estratégia de retenção proativa**.

---

## 2. Metodologia Aplicada

O projeto seguiu um pipeline estruturado de análise de dados, inspirado em metodologias padrão de mercado como o CRISP-DM.

### 2.1. Extração e Tratamento de Dados (Data Wrangling)
- **Normalização:** Utilização da biblioteca `pandas` para transformar a estrutura aninhada do JSON em um DataFrame tabular.
- **Limpeza de Dados (Data Cleaning):** Tratamento rigoroso de inconsistências, como a conversão de tipos de dados (`string` para `float`), e a remoção de registros com dados nulos ou vazios na variável-alvo (`Churn`).

### 2.2. Engenharia de Atributos (Feature Engineering)
- **`Contas_Diarias`:** Normalização da cobrança mensal para uma base diária.
- **`QuantidadeServicos`:** Agregação dos múltiplos serviços de valor adicionado em uma única métrica que representa o nível de "engajamento" do cliente.

### 2.3. Análise Exploratória de Dados (EDA)
- **Análise Descritiva:** Cálculo de medidas de tendência central (média, mediana) e dispersão (desvio padrão).
- **Análise Visual:** Uso de **Box Plots**, **Histogramas** e **Gráficos de Barras Agrupados** para visualizar a relação do Churn com as demais variáveis.

### 2.4. Análise de Correlação
- **Validação Numérica:** Utilização da matriz de correlação de Pearson para quantificar a força da relação linear entre as variáveis e o Churn. É crucial ressaltar que **"correlação não implica causalidade"**. Este gráfico valida os insights visuais e identifica preditores fortes para futuros modelos.

---

## 3. Principais Insights e Conclusões

A análise de dados permitiu a construção de um perfil claro do cliente com alta probabilidade de Churn:

> **O cliente com maior risco de evasão é aquele com baixo tempo de contrato (baixo `tenure`), que possui um contrato flexível (mês a mês) e paga uma mensalidade relativamente alta.**

A correlação negativa de **-0.35** entre `tenure` e `Churn` e a correlação positiva de **+0.41** entre `Contrato_Mês a Mês` e `Churn` são as evidências numéricas mais fortes que sustentam esta conclusão.

---

## 4. Recomendações Estratégicas

Com base nas evidências, as seguintes ações são recomendadas para a gestão de negócios da Telecom X:

1.  **Ações de Retenção Focadas:** Desenvolver campanhas de marketing direcionadas para clientes com menos de 10 meses de contrato e que possuam contrato "mês a mês", oferecendo um upgrade para um plano anual com benefícios tangíveis.
2.  **Revisão do Portfólio de Serviços:** Aprofundar a análise sobre a alta taxa de Churn em clientes de Fibra Óptica para determinar se a causa é uma questão de preço, qualidade ou suporte.
3.  **Desenvolvimento de um Modelo Preditivo:** Utilizar este dataset tratado como base para treinar um **modelo de classificação (como Regressão Logística ou Random Forest)**. Tal modelo poderia gerar um "score de risco de Churn" para cada cliente em tempo real, permitindo que a equipe de retenção atue de forma proativa.

---

## 5. Como Executar o Projeto

1.  **Clone este repositório:**
    ```bash
    git clone [https://docs.github.com/articles/referencing-and-citing-content](https://docs.github.com/articles/referencing-and-citing-content)
    ```
2.  **Instale as dependências:**
    ```bash
    pip install pandas requests matplotlib seaborn numpy
    ```
3.  **Execute o Notebook:**
    Abra o arquivo `TelecomX_BR.ipynb` em um ambiente Jupyter (Jupyter Notebook, Jupyter Lab ou Google Colab) e execute as células em ordem.

### Tecnologias Utilizadas
- **Linguagem:** Python 3
- **Bibliotecas:** Pandas, NumPy, Matplotlib, Seaborn, Requests
- **Ambiente:** Jupyter Notebook / Google Colab

---

## Autor

* **Jhonatan Willian**
* **LinkedIn:** `www.linkedin.com/in/jhonatan-willian-santana-5808ab172`
* **GitHub:** `https://github.com/jhonatanwsds`
