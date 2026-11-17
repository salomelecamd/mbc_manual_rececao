# Manual da receção — Novigest

Manual da equipa da Mariluz Bioclinic, feito em Quarto e publicado em HTML.

## Estrutura

```
manual-rececao/
├── _quarto.yml          configuração (tema, índice, pasta de saída)
├── index.qmd            o texto do manual — é aqui que se edita
├── estilo.css           cores e aspeto
├── imagens/             prints do Novigest
├── manual-rececao.Rproj projeto RStudio
└── docs/                site gerado (é isto que o GitHub Pages publica)
```

## Atualizar no RStudio

1. Abrir `manual-rececao.Rproj`.
2. Editar `index.qmd` (texto) ou acrescentar prints em `imagens/`.
3. Carregar em **Render** (ou na consola: `quarto::quarto_render()`).
4. Abrir `docs/index.html` para ver o resultado.

Não editar nada dentro de `docs/`: é apagado e gerado de novo em cada render.

Um print novo entra no texto assim:

```markdown
![](imagens/nome_do_print.png){fig-alt="Descrição do que o print mostra"}
```

## Publicar no GitHub Pages

1. Criar um repositório no GitHub e enviar esta pasta (incluindo `docs/`).
2. No repositório: **Settings → Pages → Build and deployment**:
   *Source* = "Deploy from a branch", *Branch* = `main`, pasta `/docs`.
3. Depois de cada alteração: Render → commit → push. O site atualiza-se em 1–2 minutos.

**Atenção:** um site do GitHub Pages é público para qualquer pessoa com o link,
mesmo que o repositório seja privado (exceto em contas GitHub Enterprise).
