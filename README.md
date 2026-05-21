# Telco Customer Churn Analysis & Retention Strategy

##  Contexto do Projeto
Este projeto consiste em uma **Análise Regida por Dados (Data-Driven)** baseada no *dataset* de Telecomunicações da IBM. O objetivo principal foi identificar quais variáveis demográficas, financeiras e comportamentais possuem maior correlação com a evasão de clientes (*Churn*) e, a partir disso, desenhar estratégias preventivas para mitigar essa perda de receita recorrente.

---

##  Pipeline de Dados & Engenharia de Dados (ETL)


1. **Análise de Integridade e Limpeza (Microsoft Excel):**
   * Auditoria inicial dos dados brutos e identificação de registros inconsistentes.
   * Isolamento de lacunas e células vazias na coluna `TotalCharges` (clientes recém-adquiridos com faturas ainda não geradas).

2. **Extração, Transformação e Carga - ETL (Power Query):**
   * **Tratamento de Localidade:** Correção de conflitos de idioma (padrão americano de pontos como decimais vs. padrão brasileiro de vírgulas), evitando a corrupção e inflação artificial dos valores.
     
   * **Correção de Tipagem:** Conversão da coluna `tenure` (Tempo de Permanência) de Texto para Número Inteiro.
     
   * **Tratamento de Nulos:** Substituição de espaços em branco por `0` na coluna de faturamento total para garantir a integridade matemática dos cálculos.


---

## Principais Insights de Negócio & Matemática dos Dados

O painel foi estruturado para responder a 4 perguntas cruciais que impactam diretamente o P&L (Lucros e Perdas) da organização:

### 1. Qual é o impacto do tipo de contrato na taxa de evasão?
* **A Matemática:** O contrato mensal (*Month-to-month*) possui **42,7%** de Churn (1.655 cancelamentos em 3.875 clientes), enquanto o contrato bianual registra apenas **2,83%** (48 cancelamentos em 1.695 clientes).
* **O Insight:** Clientes com contratos mensais são **15 vezes mais propensos a cancelar** do que os clientes com contratos estáveis de dois anos.
<br>
<img width="471" height="356" alt="image" src="https://github.com/user-attachments/assets/5c49968b-c91f-4081-8363-ab28cc124e26" />
<br>


### 2. O tempo de fidelidade (*Tenure*) determina quando o cliente desiste?
* **A Matemática:** A análise temporal revelou uma curva com um **pico  de evasão entre os meses 1 e 10**.
* **O Insight:** Existe uma falha crítica na experiência inicial do cliente (*Onboarding*). Clientes que superam a barreira dos 12 primeiros meses aumentam seu *Lifetime Value (LTV)* e tornam-se extremamente estáveis.
<br>
<img width="410" height="351" alt="image" src="https://github.com/user-attachments/assets/527ca5e5-b573-439a-84b3-b981e9852bbf" />
<br>

### 3. Clientes com Serviço de Suporte Técnico são mais fiéis?
* **A Matemática:** Clientes **sem suporte técnico** registram **41,64%** de Churn, enquanto aqueles que contratam ou possuem o suporte têm a taxa reduzida para **15,17%**.
* **O Insight:** O suporte técnico atua diretamente contra o cancelamento. A ausência de auxílio técnico em momentos de instabilidade do serviço aumenta o risco de perda do cliente.
<br>
<img width="420" height="387" alt="image" src="https://github.com/user-attachments/assets/c97cb547-2f13-474d-b602-73a828621f1e" />
<br>

### 4. Existe relação entre o valor da mensalidade e a saída do cliente?
* **A Matemática:** Agrupando os valores em faixas (*Bins* de R$ 20), observou-se uma explosão na densidade de Churn na janela de **R$ 70,00 a R$ 100,00**.
* **O Insight:** Acima de R$ 70,00, o cliente torna-se extremamente crítico e, se a percepção de valor/qualidade não for impecável, ele migra para a concorrência.
<br>
<img width="444" height="378" alt="image" src="https://github.com/user-attachments/assets/9c4309fe-d9a1-48a8-8e3b-1fc059e1c002" />
<br>

---

##  Arquitetura do Dashboard Interativo


* **Camada de KPIs (Topo):** 4 cartões estruturados.
  <br>
  * **Total de Clientes:** 7.043
  * **Total de Cancelamentos:** 1.869
  * **Taxa de Cancelamentos:** 26,54%
  * **Ticket Médio:** R$ 59,77
  <br>
  
   <img width="1277" height="715" alt="image" src="https://github.com/user-attachments/assets/fa421df7-41e1-4126-8f64-eca7032fe22b" />




---

##  Plano de Ação Recomendado 

Com base nas evidências analíticas, as seguintes ações foram propostas para a mesa diretora:

1. **Campanha de Migração de Portfólio:** Criar gatilhos de marketing para oferecer upgrades de velocidade gratuitos ou descontos temporários para clientes do plano Mensal migrarem para os contratos Anual/Bianual.
2. **Onboarding (Primeiros 90 dias):** Implementar réguas de relacionamento automáticas (Customer Success) logo após a instalação, garantindo que o cliente saiba utilizar o serviço e mitigando o pico de churn inicial.
3. **Ancoragem com Suporte Técnico:** Reempacotar os planos na faixa crítica de R$ 70 - R$ 100 para incluir o Suporte Técnico de forma nativa como um benefício de "valor agregado", mascarando o custo e blindando o cliente.

---


## 👤 Autor
* **Anthony Augusto da Silva**
* Graduando em Análise e Desenvolvimento de Sistemas — Instituto Federal de São Paulo (IFSP)
  <br>
  
## Entre em contato:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anthony-augusto-silva-a42617279)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Anthony-As-2004)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:anthonyaugustosilva.2004@gmail.com)
