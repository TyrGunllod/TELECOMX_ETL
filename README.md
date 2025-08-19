
# 📊 Análise de Evasão de Clientes (Churn)

[![Python](https://img.shields.io/badge/Python-3.10+-blue)](https://www.python.org/) 
[![Plotly](https://img.shields.io/badge/Plotly-Interativo-orange)](https://plotly.com/python/) 
[![Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)  

---

## 🔹 Descrição do Projeto
Este projeto analisa a evasão de clientes (churn) em uma base de dados de uma empresa de serviços. O objetivo é identificar fatores que influenciam a retenção, utilizando **variáveis categóricas** (perfil do cliente e serviços contratados) e **variáveis numéricas** (tempo de contrato, valores de cobrança e uso diário).  

O resultado inclui **tabelas, gráficos interativos e conclusões** que ajudam a orientar ações estratégicas para redução de churn.

---

## 🔹 Tecnologias Utilizadas
- **Python 3.10+** – linguagem principal  
- **pandas** – manipulação e análise de dados  
- **plotly** – visualizações interativas  
- **Google Colab** – ambiente de execução do notebook  

---

## 🔹 Estrutura do Projeto
```
/churn-analysis
│
├─ df_base_util.csv             # Base de dados utilizada
├─ TelecomX_BR.ipynb			# Notebook com análise e gráficos interativos
├─ README.md                    # Este arquivo
```

---

## 🔹 Objetivos da Análise
1. Explorar a distribuição de **churn** entre clientes.  
2. Identificar variáveis **categóricas** associadas à evasão:  
   - `contract`, `paymentmethod`, `internetservice`, `partner`, `dependents`  
3. Avaliar variáveis **numéricas** relacionadas à evasão:  
   - `tenure`, `chargesmonthly`, `chargestotal`, `contas_diarias`, `seniorcitizen`  
4. Gerar gráficos interativos e tabelas de resumo.  
5. Elaborar **insights, conclusões e recomendações estratégicas**.

---

## 🔹 Principais Insights

### Variáveis Categóricas
| Variável | Categoria | Taxa de Evasão (%) |
|----------|----------|------------------|
| Contract | month-to-month | 42,7 |
| Paymentmethod | electronic_check | 45,3 |
| Internetservice | fiber_optic | 41,9 |
| Partner | 0 (sem parceiro) | 33,0 |
| Dependents | 0 (sem dependentes) | 31,3 |

**Interpretação:**  
- Contratos curtos e métodos de pagamento eletrônicos aumentam churn.  
- Clientes sem parceiros ou dependentes cancelam mais.  
- Serviços de fibra óptica apresentam maior evasão.

### Variáveis Numéricas
| Variável | Média Churn=1 | Média Churn=0 | Observação |
|----------|---------------|---------------|------------|
| tenure | 17,98 meses | 37,57 meses | Clientes que cancelaram permanecem menos tempo |
| chargesmonthly | 74,44 | 61,27 | Cobrança mensal mais alta aumenta churn |
| chargestotal | 1531,80 | 2555,34 | Apesar do menor tempo, gasto total menor |
| contas_diarias | 2,48 | 2,04 | Clientes mais ativos diariamente tendem a cancelar |
| seniorcitizen | 0,25 | 0,13 | Clientes idosos apresentam maior churn relativo |

**Interpretação:**  
- Tempo de contrato curto aumenta risco de evasão.  
- Cobrança mensal alta pode impactar negativamente a retenção.  
- Clientes mais ativos e idosos têm maior probabilidade de churn.

---

## 🔹 Gráficos Interativos
Todos os gráficos do projeto são gerados **diretamente no notebook** com Plotly:  
- Barras horizontais de **churn por categoria**  
- Boxplots comparando **variáveis numéricas por churn**  
- Ferramenta totalmente interativa para explorar os dados  

> Exemplo de visualização:  
> ![Exemplo de gráfico Plotly](https://plotly.com/~empet/1527.png)  

---

## 🔹 Conclusões e Recomendações
- **Churn prevalente:** contratos curtos, pagamentos via electronic_check, internet fibra óptica.  
- **Maior risco:** clientes sem parceiros ou dependentes, idosos e muito ativos.  
- **Recomendações estratégicas:**  
  1. Incentivar contratos anuais ou de dois anos com benefícios.  
  2. Revisar políticas de cobrança e métodos de pagamento.  
  3. Criar campanhas específicas para clientes solos ou sem dependentes.  
  4. Monitorar clientes ativos e idosos para suporte personalizado.

---

## 🔹 Como Executar
1. Abra o notebook [TelecomX_BR.ipynb](./TelecomX_BR.ipynb) no **Google Colab**.  
2. Certifique-se de ter a base `TelecomX_Data.json` disponível.  
3. Execute todas as células para visualizar **tabelas, gráficos interativos e insights**.

---

## 🔹 Licença
Projeto educacional, aberto para uso e aprendizado.  
