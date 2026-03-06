# 3-fase-2-Telecom-X-Analise-de-Evasao de Clientes Churn-Parte-1
# Telecom X - Análise de Evasão de Clientes

Objetivo
O objetivo deste projeto é analisar os fatores que influenciam a evasão (churn) de clientes da empresa **Telecom X**, utilizando técnicas de análise de dados para identificar padrões, tendências e insights que possam ajudar a reduzir cancelamentos.

**Tecnologias Utilizadas**
  ➢ Python 3.x  
  ➢ Pandas  
  ➢ NumPy  
  ➢ Matplotlib  
  ➢ Seaborn  
 
**Etapas do Projeto**

### 1. Extração de Dados
  ➢ Dados extraídos via API em JSON.  
  ➢ Normalização das colunas aninhadas usando `pd.json_normalize()`.

### 2. Limpeza e Tratamento
  ➢  Remoção de valores nulos e duplicados.  
  ➢  Conversão de tipos de dados (ex.: `Charges.Total` para float).  
  ➢ Criação da coluna **Contas_Diarias** a partir de `Charges.Monthly`.  
  ➢  Padronização das colunas binárias (`Yes/No` → `1/0`, `Female/Male` → `0/1`) **sem gerar warnings**.

### 3. Análise Exploratória de Dados (EDA)

  **Análise descritiva**
  ➢ média, mediana, desvio padrão, mínimo e máximo das variáveis numéricas.
  
 **Distribuição do churn**:
 
  ➢ 7043 clientes analisados:
  ➢ 5174 clientes permaneceram (~73,5%)  
  ➢ 1869 clientes cancelaram (~26,5%)
    
 **Churn por tipo de contrato**:
 
  ➢ Month-to-month → ~42% cancelaram  
  ➢ One year → ~11% cancelaram  
  ➢ Two year → ~3% cancelaram  

- **Tempo médio de permanência**:
  
  ➢ Clientes que cancelaram → ~18 meses  
  ➢ Clientes ativos → ~37 meses

- **Gasto médio mensal**:
  
  ➢ clientes que cancelaram apresentam tendência de gastar mais mensalmente.
 
 ### 4. Visualização
  ➢ Gráficos de barras para **churn por gênero, tipo de contrato e método de pagamento**.  
  ➢ Boxplots para **tenure** e **Charges.Total** versus churn.  
  ➢ Matriz de correlação para identificar relações entre variáveis.  
  ➢ Gráfico de correlação específica das variáveis com churn.

### 5. Insights
  ➢ Clientes com **contratos mensais** e **pouco tempo de permanência** têm maior tendência a cancelar.  
  ➢ Valor mensal gasto pode influenciar a decisão de churn.  
  ➢ Serviços adicionais e contratos mais longos aumentam a fidelidade.

### 6. Recomendações
  ➢ Incentivar **contratos de longo prazo**.  
  ➢ Criar **programas de retenção para clientes novos**.  
  ➢ Oferecer **benefícios ou descontos progressivos** para clientes de menor tempo de permanência.  
  ➢ Monitorar e analisar **métodos de pagamento** e valores de mensalidade para reduzir churn.


## Dados Exportados

Foram gerados arquivos CSV durante a análise:

| Arquivo | Conteúdo |
|---------|----------|
| telecomx_dados_tratados.csv | Dataset final tratado com todas as colunas e transformações |
| clientes_churn.csv | Apenas clientes que cancelaram o serviço |
| matriz_correlacao.csv | Correlação entre todas as variáveis numéricas |
