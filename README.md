Análise de Segmentação de Clientes com RFM

1. Visão Geral do Projeto

Este projeto realiza uma análise de segmentação de clientes para uma empresa de varejo online fictícia. Utilizando o modelo RFM (Recência, Frequência, Valor Monetário), o objetivo é identificar diferentes perfis de consumidores com base em seu comportamento de compra.

O resultado final é um conjunto de segmentos acionáveis (ex: "Clientes Campeões", "Clientes em Risco", "Novos Clientes") que permitem ao time de marketing criar campanhas personalizadas e mais eficazes.

2. Valor Comercial

A segmentação RFM permite que a empresa:

Maximize o ROI de Marketing: Focando os esforços e investimentos nos clientes mais valiosos e com maior probabilidade de compra.

Aumente a Retenção: Identificando clientes "fiéis" (que precisam de um agrado) ou clientes "adormecidos" (que precisam de uma campanha de reativação).

Personalize a Comunicação: Enviando a mensagem certa para o cliente certo, aumentando o engajamento.

Tome Decisões Estratégicas: Obtendo uma visão clara da saúde da base de clientes e da eficácia das estratégias de aquisição e retenção.

3. Tecnologias Utilizadas

Linguagem: Python

Bibliotecas de Análise: pandas, numpy

Bibliotecas de Visualização: matplotlib, seaborn

Ambiente: Jupyter Notebook

Ferramenta de BI: Power BI

4. O Projeto em Etapas

A análise foi dividida no seguinte fluxo de trabalho:

Coleta e Limpeza de Dados:

Os dados brutos foram carregados (dataset Online Retail da UCI).

Foi realizado um tratamento de valores ausentes (remoção de CustomerID nulos), remoção de duplicatas e tratamento de dados inválidos (como devoluções com quantidade negativa).

Engenharia de Atributos (Cálculo do RFM):

Recência (R): Calculado como o número de dias desde a última compra do cliente.

Frequência (F): Calculado como o número total de transações (faturas únicas) de cada cliente.

Monetário (M): Calculado como o valor total gasto por cada cliente.

Cálculo de Pontuação (Scoring):

Cada cliente foi pontuado de 1 a 4 para cada métrica (R, F e M) com base em quartis.

Por exemplo, clientes com maior recência (compraram há menos tempo) recebem pontuação 4. Clientes com maior frequência e gasto também recebem pontuação 4.

Segmentação:

As pontuações foram combinadas para criar um RFM_Score (ex: '444').

Com base nesses scores, os clientes foram agrupados em segmentos nomeados, como:

Campeões: (444, 344) - Nossos melhores clientes. Compram recente, com frequência e gastam muito.

Clientes Fiéis: (144, 244) - Compram com frequência, mas não o fazem há algum tempo. Precisam de atenção.

Hibernando: (111, 121) - Clientes antigos, com baixa frequência e baixo gasto. Risco de churn.

Novos Clientes: (411, 412) - Compraram recentemente, mas poucas vezes. Potencial para se tornarem fiéis.

5. Resultados e Dashboard

Os segmentos e métricas foram consolidados em um dashboard interativo.

O dashboard permite à equipe de negócio:

Visualizar a distribuição de clientes por segmento.

Analisar o valor total e o ticket médio de cada segmento.

Filtrar clientes por perfil para ações de marketing direcionadas.

<img width="1524" height="808" alt="image" src="https://github.com/user-attachments/assets/f4e8ed04-90e9-43dc-82ae-26ed3d3f7490" />
<img width="1544" height="807" alt="image" src="https://github.com/user-attachments/assets/ab7d9d9e-da4c-4e62-b6e1-7844e45004a8" />
<img width="1512" height="785" alt="image" src="https://github.com/user-attachments/assets/8bb85077-77a9-4381-9dc8-631a220cd829" />



