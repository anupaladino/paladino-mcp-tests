# PALADINO — Design System (fase de teste)

## Status
Pipeline Figma → HTML validado em três rodadas (componente único, brief
sintético, conteúdo real denso) — todas com pelo menos um bug real
encontrado e corrigido, não entregas sem fricção. Escrita nativa em Figma
via `use_figma` (código → Figma) também validada.

## Tipografia e cor
Ver @context/tokens.md — valores reais extraídos do Figma via Styles.
Tipografia (DM Sans + escala) e paleta (preto/branco/escala de cinza)
confirmadas como definitivas do Paladino.

## Padrão estrutural
Componentes do arquivo de origem seguem 3 variantes tonais: light, gray, dark.
Preservar essa lógica em qualquer código gerado.

## Investigando componentes no Figma
Ao checar o que um componente é capaz de fazer, inspecionar direto as
páginas de Components/Variables — variantes e props reais — não só como
ele foi usado nos frames de exemplo já montados. Um frame de exemplo pode
nunca ter demonstrado uma variante que existe e resolveria o problema
(caso confirmado: `Timeline1` com `Active=True/False`, nunca usado nos
exemplos, mas exatamente o que resolvia destaque de etapa).

## Figma ↔ código: direções e limites
- Código → Figma (`use_figma`): funciona bem. Reconstrói a estrutura a
  partir do HTML/CSS-fonte como frames/auto-layout nativos — não é
  captura de pixel renderizado.
- Captura de página renderizada → Figma (`generate_figma_design` ou
  equivalente): **não disponível neste setup**. Limitação arquitetural
  confirmada — o sandbox da Plugin API não tem acesso a rede externa pra
  renderizar uma URL. Não é configuração pra destravar; não retentar sem
  essa capacidade estar realmente conectada.

## Convenções de output
- HTML de teste vai em `docs/`, não `output/` — bate com o que o GitHub
  Pages serve.
- Repositório de teste (`paladino-mcp-tests`) é separado do repositório
  de produção.

## Conteúdo de teste
Ver @content/test-copy.md — usar esse texto no lugar de lorem ipsum ou
texto genérico ao gerar componentes de teste.

## Logo
assets/logo/ — versões white e black, SVG.

## Não fazer
- Não gerar componentes além do que foi pedido no prompt.
- Não inventar cor, peso de fonte ou espaçamento fora do que está em tokens.md.
