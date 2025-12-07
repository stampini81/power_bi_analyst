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

## Guia rápido para entregar na DIO

Use esta lista como roteiro para replicar o projeto no seu ambiente, publicar e enviar o link no desafio da DIO.

1) Preparar o arquivo
- Baixe/clone este repositório (ou faça fork do repositório da instrutora para manter referência) e abra no Power BI Desktop.
- Conecte-se à sample financials: use os CSVs em `dataset/` ou importe direto do repositório da instrutora.
- Aplique um dos temas em `Módulo 2/Criando Dashborads/Theme.json` (ou `Nowalls Analytics Theme.json`).

2) Construir as páginas
- Páginas 1 e 2: replique a estrutura vista nas aulas (layout, botões de navegação, segmentadores, indicadores para alternar visuais). Certifique-se de que os botões navegam entre as páginas.
- Página 3 (nova): inclua os três visuais solicitados neste README (dois mapas e uma pizza) com títulos claros, tooltips ricos e disposição organizada.

3) Navegação e segmentadores
- Crie botões de navegação entre páginas e associe imagens quando fizer sentido.
- Use indicadores + botões para alternar visuais sobre o mesmo assunto, seguindo o padrão da aula.
- Adicione segmentadores principais (ex.: Ano, Segment, Country) e formate-os de forma consistente.

4) Publicar
- No Power BI Desktop: Home > Publish > escolha o workspace no Power BI Service.
- No Power BI Service: abra o relatório publicado, valide filtros e navegação. Copie a URL pública (ou de acesso interno, se for o caso) para entrega.
- Opcional: insira o relatório no PowerPoint via suplemento Power BI e exporte um PDF com capturas (útil para anexar no repositório).

5) Entregar no GitHub/DIO
- No repositório, adicione em `Módulo 2/Desafio de Projeto/entrega/`:
   - O arquivo `.pbix` final (se permitido pelo tamanho), e/ou
   - Um `LINK.md` com a URL publicada do relatório, e
   - Capturas de tela dos visuais (PNG/JPG) para evidência.
- Atualize o campo "Link do relatório publicado" acima com a URL copiada do Power BI Service.
- Faça commit/push das evidências e envie o link do repositório na submissão da DIO.

Checklist final antes de enviar
- [ ] Páginas 1 e 2 replicadas com layout e botões funcionais
- [ ] Segmentadores e botões com imagens/estados configurados
- [ ] Página 3 com mapas (Sales/Units, Profit) e pizza (Profit por Segment)
- [ ] Tooltips conferidos (Sales, Units, Profit, Country/Segment)
- [ ] Tema aplicado e títulos claros
- [ ] Relatório publicado e link adicionado neste README
- [ ] Evidências salvas em `entrega/`
