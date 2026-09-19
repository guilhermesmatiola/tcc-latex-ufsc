# Instruções para o agente de IA responsável pela conversão

## Objetivo

Converter o TCC de Geologia escrito no Google Docs para o projeto existente em `latex/`, preservando integralmente o conteúdo acadêmico aprovado e a estrutura editorial do documento. O agente deve atuar como conversor e assistente técnico, não como autor oculto do trabalho.

## Prompt inicial recomendado

Copie o texto abaixo para o agente de IA e anexe a versão mais recente do TCC exportada do Google Docs em `.docx`, juntamente com a pasta `latex/` deste repositório.

```text
Você é responsável por converter um Trabalho de Conclusão de Curso de Graduação em Geologia da UFSC, escrito no Google Docs e exportado em DOCX, para o template LaTeX fornecido.

Use o DOCX como fonte editorial do conteúdo e a pasta latex/ como autoridade para estrutura, comandos, estilo e compilação. Preserve o significado, a ordem argumentativa, os títulos, as citações, as legendas, as fontes de figuras e tabelas e os dados técnicos. Não invente texto, resultados, referências, coordenadas, unidades, datas, autores ou informações institucionais. Quando algo estiver ausente, ambíguo ou incompatível, marque como pendência e faça uma pergunta objetiva.

Distribua o conteúdo nos arquivos existentes do projeto LaTeX. Atualize dados.tex com os metadados confirmados; converta os elementos pré-textuais para pre-textuais/; converta os capítulos para capitulos/; registre referências em referencias.bib; coloque imagens em figuras/; e use pos-textuais/ para apêndices e anexos. Não altere o arquivo de estilo apenas para acomodar conteúdo comum.

Converta estilos do DOCX semanticamente: títulos principais em capítulos, títulos de segundo nível em seções e títulos de terceiro nível em subseções. Use os comandos e ambientes já existentes no template para figuras, quadros, tabelas, coordenadas e dados estruturais. Preserve itálico, negrito, listas e notas somente quando tiverem função acadêmica clara.

Para cada citação, associe uma chave BibTeX verificável. Se os dados bibliográficos estiverem incompletos, não complete por suposição: crie uma pendência. Garanta que todas as citações tenham entrada em referencias.bib e que nenhuma entrada não citada seja incluída sem motivo.

Antes de concluir, compile main.tex, corrija erros e avisos relevantes e confira o PDF inteiro. Verifique capa, folha de rosto, resumo, abstract, sumário, hierarquia de seções, referências cruzadas, figuras, tabelas, quadros, equações, unidades, referências, apêndices e anexos. Entregue um relatório curto das alterações e uma lista separada de pendências que exigem decisão humana.
```

## Mapeamento entre Docs e LaTeX

| Conteúdo no Docs | Destino no projeto LaTeX |
|---|---|
| Dados de autoria, título, banca e defesa | `latex/dados.tex` |
| Dedicatória, agradecimentos e epígrafe | `latex/pre-textuais/` |
| Resumo, palavras-chave, abstract e keywords | `latex/pre-textuais/resumo.tex` e `latex/pre-textuais/abstract.tex` |
| Introdução e objetivos | `latex/capitulos/01-introducao.tex` |
| Área de estudo e contexto geológico | `latex/capitulos/02-area-estudo-contexto-geologico.tex` |
| Materiais e métodos | `latex/capitulos/03-materiais-metodos.tex` |
| Resultados | `latex/capitulos/04-resultados.tex` |
| Discussão | `latex/capitulos/05-discussao.tex` |
| Conclusões | `latex/capitulos/06-conclusoes.tex` |
| Referências bibliográficas | `latex/referencias.bib` |
| Imagens, mapas, perfis e diagramas | `latex/figuras/` |
| Apêndices e anexos | `latex/pos-textuais/` |

## Regras que o agente deve obedecer

1. Não inventar conteúdo científico nem completar lacunas por plausibilidade.
2. Não alterar números, unidades, coordenadas, atitudes estruturais ou resultados sem autorização explícita.
3. Não fabricar referências ou chaves BibTeX.
4. Diferenciar apêndice, produzido pela autora, de anexo, produzido por terceiros.
5. Preservar a distinção entre observação, resultado e interpretação geológica.
6. Manter nomes científicos, símbolos, fórmulas e unidades com grafia e formatação adequadas.
7. Registrar toda dúvida em uma lista de pendências, indicando o trecho e a decisão necessária.
8. Evitar editar `latex/estilo/tcc-geologia-ufsc.sty`; mudanças de estilo exigem justificativa e validação separadas.
9. Nunca considerar a conversão concluída sem compilar e revisar o PDF gerado.
10. Confirmar as normas institucionais vigentes antes da versão de depósito.

## Checklist de validação

- [ ] Os metadados de `dados.tex` correspondem à versão aprovada no Docs.
- [ ] A hierarquia de capítulos, seções e subseções foi preservada.
- [ ] Nenhum parágrafo, tabela, figura, nota ou legenda foi omitido.
- [ ] Todas as figuras têm legenda, fonte e referência no texto.
- [ ] Mapas apresentam os elementos cartográficos necessários.
- [ ] Todas as citações resolvem para entradas válidas em `referencias.bib`.
- [ ] Não há referências inventadas ou campos bibliográficos preenchidos por suposição.
- [ ] Unidades, coordenadas, símbolos e notações geológicas foram conferidos.
- [ ] Sumário e listas foram atualizados pela compilação.
- [ ] O PDF foi revisado página por página.
- [ ] As pendências humanas foram documentadas separadamente.
