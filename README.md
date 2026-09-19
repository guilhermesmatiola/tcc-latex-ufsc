# Template de TCC em LaTeX — Geologia UFSC

Modelo limpo e modular para o Trabalho de Conclusão de Curso de Graduação em Geologia da Universidade Federal de Santa Catarina.

## Começo rápido

1. Edite `dados.tex` com seus dados.
2. Substitua o conteúdo dos arquivos em `pre-textuais/` e `capitulos/`.
3. Adicione as referências em `referencias.bib`.
4. Coloque mapas, perfis, fotografias e demais imagens em `figuras/`.
5. Compile `main.tex` no Overleaf ou localmente.

No Overleaf, selecione XeLaTeX. Para compilar localmente com uma distribuição TeX completa:

```text
latexmk -xelatex main.tex
```

Também é possível usar Tectonic:

```text
tectonic main.tex
```

## Organização

- `main.tex`: ordem do documento.
- `dados.tex`: metadados preenchidos uma única vez.
- `estilo/tcc-geologia-ufsc.sty`: formatação e comandos reutilizáveis.
- `pre-textuais/`: dedicatória, agradecimentos, epígrafe, resumo, abstract, siglas e símbolos.
- `capitulos/`: conteúdo textual do TCC.
- `pos-textuais/`: apêndices e anexos.
- `referencias.bib`: base bibliográfica.
- `figuras/`: imagens e identidade visual.

## Recursos para Geologia

- `\figuratcc`: mapas, fotografias, perfis e diagramas com legenda, fonte e rótulo.
- `\figuraplaceholder`: espaço temporário para uma figura ainda não finalizada.
- `\dadoestrutural`: notação consistente para atitude de estruturas.
- `\coordenadas`: apresentação uniforme de coordenadas.
- ambiente `quadro`: conteúdo textual com lista própria.
- ambiente `paisagem`: mapas e tabelas em orientação horizontal.

Leia os comentários nos arquivos `.tex`: eles indicam onde substituir conteúdo sem poluir o PDF final.

> Atenção: normas do curso e da Biblioteca Universitária podem mudar. Antes da entrega, confirme a versão vigente com a Coordenação de Geologia e com a BU/UFSC.

