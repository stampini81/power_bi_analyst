# Especificação dos Visuais — Página 3

Este guia descreve como montar a terceira página do relatório conforme o desafio.

## Medidas DAX sugeridas
Se as colunas já forem aditivas, use-as diretamente. Caso prefira medidas explícitas, crie:

- Sales = SUM('Sales'[Sales])
- Units = SUM('Sales'[Units])
- Profit = SUM('Sales'[Profit])

Ajuste nomes de tabela/coluna conforme seu dataset (ex.: 'FactSales'[SalesAmount], etc.).

## Mapa 1 — Vendas e Unidades por País
- Visual: Map (bolhas) ou Filled Map (dependendo do dataset e preferência). Para comparações por valor, Map de bolhas é recomendado.
- Campos:
  - Location: Country (País)
  - Size: Sales (Soma)
  - Tooltip: Country, Sales, Units
- Formatação:
  - Title: "Vendas e Unidades por País"
  - Data colors: usar tema do repositório (opcional)
  - Bubbles: manter transparência ~70-80% para sobreposições
  - Labels: ativar se preferir destacar valores principais

## Mapa 2 — Lucro por País
- Visual: Map ou Filled Map
- Campos:
  - Location: Country
  - Size/Color: Profit (Soma)
  - Tooltip: Country, Profit, Sales (opcional para contexto)
- Formatação:
  - Title: "Lucro por País"
  - Escala de cores: verde para positivos; opcionalmente, use divergente se houver perdas (negativos)

## Pizza — Lucro por Segmento
- Visual: Pie chart
- Campos:
  - Legend: Segment
  - Values: Profit (Soma)
  - Tooltip: Segment, Profit, Sales (opcional)
- Formatação:
  - Title: "Lucro por Segmento"
  - Data labels: Percentages On; Category + Value (se houver espaço)
  - Sort: por Profit desc

## Disposição sugerida (layout)
- Grade 2 colunas x 2 linhas:
  - Linha 1: Mapa 1 (esquerda), Mapa 2 (direita)
  - Linha 2: Pizza centralizada (largura média)
- Margens: manter respiro visual; alinhar cabeçalhos

## Nomes dos visuais
- Mapa 1: "Vendas e Unidades por País"
- Mapa 2: "Lucro por País"
- Pizza: "Lucro por Segmento"

## Tooltips customizados (opcional)
- Crie uma página de Tooltip com layout pequeno e adicione cartões para Sales, Units e Profit.
- Nos visuais, em Tooltip > Page, selecione a página de tooltip.

## Tema do relatório
- Em View > Themes > Browse for themes, selecione um dos temas em `Módulo 2/Criando Dashborads/Theme.json` ou `Nowalls Analytics Theme.json`.

## Validações finais
- Conferir filtros e slicers aplicados
- Checar integridade geográfica (resolver países não reconhecidos via Data Category = Country/Region)
- Verificar que as medidas somam corretamente e títulos estão claros
