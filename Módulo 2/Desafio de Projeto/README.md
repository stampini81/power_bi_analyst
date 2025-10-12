# Desafio de Projeto — Power BI (Módulo 2)

Replicar 2 páginas do relatório vistas no curso e criar uma 3ª página com os seguintes visuais:

- Mapa 1: Soma de Sales e Unidades Vendidas por País
- Mapa 2: Soma de Profit por País
- Pizza: Profit por Segment

Ao final, publicar o relatório e compartilhar como suplemento no PowerPoint (ou salvar o .pbix caso não tenha PowerPoint).

## Pré-requisitos
- Power BI Desktop (versão atual)
- Sample/dataset do repositório: https://github.com/julianazanelatto/power_bi_analyst
- Opcional: Conta Power BI Service para publicar
- Opcional: Microsoft PowerPoint para suplemento Power BI

## Dados
Você pode usar os arquivos de sample disponibilizados no repositório da instrutora (link acima) ou os datasets já presentes neste repositório em `dataset/`.

## Objetivos da 3ª página
1. Visual de mapa com Sales e Units por Country
2. Visual de mapa com Profit por Country
3. Visual de pizza com Profit por Segment
4. Ajustar nomes dos visuais e disposição
5. Configurar tooltips (dicas de ferramenta) relevantes
6. Publicar e compartilhar

## Critérios de aceitação
- Os três visuais existem e apresentam dados corretos
- Títulos e rótulos claros (ex.: "Vendas e Unidades por País", "Lucro por País", "Lucro por Segmento")
- Tooltips exibem métricas úteis (ex.: Sales, Units, Profit, Country/Segment)
- Relatório publicado no Power BI Service ou arquivo .pbix salvo no repositório
- Se possível, link ou captura de tela do relatório publicado

## Passo a passo resumido
1. Importar dados (Get Data) e carregar as tabelas (Sales, Countries/Geography, Segment, etc.)
2. Criar medidas DAX (se necessário):
   - Sales = SUM('Sales'[Sales])
   - Units = SUM('Sales'[Units])
   - Profit = SUM('Sales'[Profit])
3. Página 3 do relatório:
   - Mapa 1: usar Country como localização; usar Sales como bolha/tamanho; adicionar Units como valor adicional (exibir em Tooltip e/ou Size secundário se usar Mapas de Bolhas). Título: "Vendas e Unidades por País".
   - Mapa 2: usar Country como localização; usar Profit como tamanho. Título: "Lucro por País".
   - Pizza: usar Segment como Legenda e Profit como Valor. Título: "Lucro por Segmento".
4. Ajustar formatação e cores (pode usar os temas em `Módulo 2/Criando Dashborads/Theme.json` ou `Nowalls Analytics Theme.json`).
5. Revisar Tooltips: incluir Sales, Units e Profit conforme o contexto de cada visual.
6. Publicar (Home > Publish) e, no PowerPoint, inserir suplemento Power BI para incorporar o relatório publicado.

## Publicação e compartilhamento
1. Publicar no Power BI Service
   - No Power BI Desktop: Home > Publish > selecione o Workspace
   - Após publicar, abra o relatório no app.powerbi.com e copie a URL para entrega
2. Compartilhar como suplemento no PowerPoint
   - No PowerPoint: Inserir > Obter Complementos > instale "Power BI" (Microsoft)
   - Inserir > Meu Complemento > Power BI > Entrar > selecione o relatório publicado
   - Ajuste o tamanho do frame do relatório nos slides
3. Alternativa sem PowerPoint
   - Salve o arquivo .pbix (Arquivo > Salvar como) dentro deste repositório, por exemplo em `Módulo 2/Desafio de Projeto/entrega/`
   - Inclua também imagens (Prints) dos três visuais e o link publicado (se houver)

## Entrega
- Commitar este README, quaisquer medidas DAX exportadas (opcional), e opcionalmente capturas de tela dos visuais.
- Se publicar o relatório, inclua o link (URL) abaixo:

Link do relatório publicado: ...

## Referências
- Repositório de apoio: https://github.com/julianazanelatto/power_bi_analyst
- Documentação Power BI: https://learn.microsoft.com/power-bi/
