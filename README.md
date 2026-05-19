# Sales Dashboard — Aditivos & Lubrificantes

Dashboard de vendas desenvolvido no **Power BI** para uma empresa nacional do setor de aditivos e lubrificantes, cobrindo o período de **2023 a 2025**.

---

## Live Dashboard

[![Sales Dashboard Preview](assets/screenshots/dashboard_preview.png)](https://app.powerbi.com/view?r=eyJrIjoiNDFiN2RjNzgtNzllYi00MTBiLWE5ZDktOWU2YzU2M2QzMjc0IiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)

> **[Acessar o Dashboard Publicado](https://app.powerbi.com/view?r=eyJrIjoiNDFiN2RjNzgtNzllYi00MTBiLWE5ZDktOWU2YzU2M2QzMjc0IiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)**

---

## Sobre o Projeto

Este projeto transforma uma planilha de vendas bruta em um dashboard analítico interativo. O objetivo é fornecer visibilidade sobre o desempenho comercial da empresa, com navegação intuitiva, drill-through para detalhamento e uma identidade visual personalizada.

---

## Stack & Ferramentas

| Ferramenta     | Uso                                      |
|----------------|------------------------------------------|
| Power BI Desktop | Modelagem, DAX, visualizações e design |
| Microsoft Excel  | Fonte de dados bruta (Sales_2023_2025) |
| Power Query      | ETL e transformação dos dados           |

---

## Estrutura do Repositório

```
sales-dashboard-powerbi/
├── dados/
│   └── Sales_2023_2025.xlsx      # Planilha de dados brutos
├── assets/
│   └── screenshots/              # Capturas de tela do dashboard
├── salesdashboard.pbix           # Arquivo Power BI Desktop
└── README.md
```

---

## Processo de Desenvolvimento

### 1. Importação dos Dados
- Dados importados diretamente do **Microsoft Excel** (`dados/Sales_2023_2025.xlsx`)
- Conexão via Power Query Editor para carregamento e transformação inicial

### 2. Primeiros Gráficos e Objetos Visuais
- Criação dos primeiros visuais exploratórios para entender a distribuição dos dados
- Identificação das principais métricas de negócio: faturamento, volume, clientes

### 3. Tratamento e Tipagem dos Dados
- Correção dos tipos de dados: campos de texto incorretamente classificados como número e vice-versa
- Padronização de cabeçalhos e nomes de colunas
- Limpeza de valores nulos e inconsistências na fonte

### 4. Design Personalizado
- Criação de um tema visual customizado alinhado à identidade da empresa
- Paleta de cores definida, fontes padronizadas e layout organizado por hierarquia de informação

### 5. Medidas DAX e Organização
- Criação de medidas DAX para KPIs principais (faturamento, ticket médio, variação YoY, etc.)
- Organização das medidas em uma **tabela de medidas dedicada** (`_Measures`) separada das tabelas de dados
- Essa estrutura evita medidas implícitas e permite reutilização em outros relatórios

### 6. Tabela de Medidas
- Criação de uma tabela de medidas central para organização e governança das métricas DAX
- Medidas agrupadas por categoria (Vendas, Clientes, Comparativos)

### 7. Ajuste de Design do Dashboard
- Refinamento do layout após a criação das medidas
- Alinhamento de visuais, espaçamento e hierarquia visual revisados

### 8. Menu Flutuante
- Implementação de um **menu de navegação flutuante** com botões de página
- Melhora significativa na usabilidade e experiência de navegação entre abas

### 9. Formatação de Valores das Medidas
- Formatação dos valores: R$ para moeda, % para percentuais, separadores de milhar
- Unidades abreviadas (K, M) para grandes valores nos visuais de cartão

### 10. Drill-through
- Configuração de **drill-through** para permitir análise detalhada por dimensão
- O usuário pode clicar com o botão direito em qualquer visual e acessar uma página de detalhamento filtrada pelo contexto selecionado

### 11. Ícones e Tooltip Personalizada
- Adição de ícones para enriquecer a identidade visual e guiar o usuário
- Criação de uma **tooltip personalizada** com informações adicionais ao passar o mouse sobre os visuais

### 12. Publicação
- Dashboard publicado no **Power BI Service** com link de acesso público
- Embed disponível via iframe para incorporação em portfólios e sites

---

## Dados Brutos

A planilha de dados cobre o período de 2023 a 2025 e contém informações de:

- Data e período das vendas
- Produtos (aditivos e lubrificantes)
- Clientes e regiões
- Valores de faturamento e quantidade

> O arquivo `Sales_2023_2025.xlsx` está disponível na pasta `dados/` para replicação e auditoria.

---

## Como Abrir o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/douglaspiangers/sales-dashboard-powerbi.git
   ```
2. Abra o arquivo `salesdashboard.pbix` no **Power BI Desktop**
3. Caso necessário, atualize o caminho da fonte de dados apontando para `dados/Sales_2023_2025.xlsx`

---

## Autor

**Douglas Mengue**  
Data Analyst | Power BI | SQL | Python  
[LinkedIn](https://linkedin.com/in/douglasmengue) · [GitHub](https://github.com/douglaspiangers)
