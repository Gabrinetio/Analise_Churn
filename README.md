# Análise Preditiva de Churn de Clientes de Telecomunicações

Este repositório contém uma análise completa e aprofundada sobre a previsão de churn (cancelamento) de clientes para uma empresa de telecomunicações, desenvolvida em notebooks do Google Colab. O projeto evolui de uma análise exploratória e modelagem inicial para análises preditivas avançadas, com foco em extrair insights acionáveis para o negócio.

## 🎯 Objetivo do Projeto

O objetivo principal é ir além da simples previsão de "quem vai cancelar" e responder a perguntas de negócio mais estratégicas, como:

* **Porquê** os clientes cancelam? (Análise de Fatores de Risco)
* **Quando** são mais propensos a cancelar? (Análise de Sobrevivência)
* Qual o **impacto financeiro** do churn? (Análise de Receita e Custo de Aquisição)
* Quais clientes **priorizar** nas ações de retenção? (Previsão de Valor do Cliente - CLV)
* Como podemos **agir proativamente**? (Previsão de Demanda de Suporte e Propensão a Downgrade)

## 📂 Estrutura do Repositório

* `WA_Fn-UseC_-Telco-Customer-Churn.csv`: O conjunto de dados original utilizado em todas as análises.
* `Analise_Churn.ipynb`: O primeiro notebook, que realiza a limpeza dos dados, tradução, treino de modelos de classificação (como Random Forest e XGBoost) e avaliação de performance inicial.
* `Analise_Churn_Avancada.ipynb`: O notebook principal e mais completo, que integra todas as análises avançadas.
* `Relatorio_Final_Completo.html`: O relatório final interativo, gerado pelo notebook avançado, consolidando todas as descobertas.
* `Relatorio_Completo_Churn.md`: Uma versão em Markdown do relatório final.

## 🚀 Análises Realizadas

O projeto é dividido em várias análises preditivas e financeiras:

1.  **Modelagem de Churn (Classificação):**
    * Treinamento de um modelo `RandomForestClassifier` para calcular a **probabilidade de churn** de cada cliente.

2.  **Análise Financeira:**
    * **Custo de Aquisição de Cliente (CAC) vs. Payback Period:** Simulação do impacto financeiro de clientes que cancelam antes de a empresa recuperar o investimento de aquisição.
    * **Churn de Receita (MRR Churn Rate):** Cálculo da percentagem de receita mensal recorrente perdida devido aos cancelamentos, uma métrica mais crítica do que a taxa de churn de clientes.

3.  **Análise de Sobrevivência (Previsão de "Quando"):**
    * **Curva de Kaplan-Meier:** Visualização exploratória da taxa de retenção de clientes ao longo do tempo.
    * **Modelo de Riscos Proporcionais de Cox:** Modelo preditivo que identifica os principais **fatores que aceleram ou previnem o churn** e permite prever a curva de sobrevivência individual de cada cliente.

4.  **Previsão de Valor do Cliente (CLV):**
    * Treinamento de um modelo `RandomForestRegressor` para prever o **valor total que cada cliente trará para a empresa**, usando a `Cobrança_Total` como proxy.

5.  **Segmentação de Clientes de Alto Risco:**
    * Uso do algoritmo **K-Means** para agrupar clientes com alta probabilidade de churn em **3 perfis (personas)** distintos, permitindo a criação de estratégias de retenção personalizadas.

6.  **Análises de Oportunidade:**
    * **Propensão a Downgrade:** Previsão de clientes com alta probabilidade de reduzir o seu plano, um indicador precoce de risco.
    * **Demanda de Suporte Técnico:** Identificação de clientes que provavelmente precisarão de suporte, permitindo uma abordagem proativa para melhorar a experiência e vender serviços adicionais.

## 🛠️ Como Executar

1.  **Ambiente:** O projeto foi desenvolvido para ser executado no **Google Colab**.
2.  **Ficheiros:** Faça o upload do ficheiro `WA_Fn-UseC_-Telco-Customer-Churn.csv` para o ambiente do Colab.
3.  **Notebook:** Abra o ficheiro `Analise_Churn_Avancada.ipynb`.
4.  **Execução:** Execute as células em ordem sequencial.
    * A célula final irá gerar os relatórios `Relatorio_Final_Completo.html` e `Relatorio_Completo_Churn.md`, que podem ser descarregados.

## 📊 Principais Resultados e Relatórios

Ao final da execução do notebook `Analise_Churn_Avancada.ipynb`, são gerados dois relatórios completos que consolidam todos os insights, incluindo:

* **Resumo executivo** com os principais indicadores financeiros.
* Listas de clientes prioritários (maior valor em risco, maior propensão a downgrade).
* Gráficos interativos sobre os perfis de risco e a curva de sobrevivência.
* Identificação clara dos principais fatores que levam ao cancelamento.

Estes relatórios servem como uma ferramenta poderosa para as equipas de marketing, retenção e produto tomarem decisões informadas e baseadas em dados.
