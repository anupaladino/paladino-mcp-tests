# PALADINO — Design System (fase de teste)

## Status
Testando o pipeline Figma → código pela primeira vez. O arquivo de origem
(TMS Marketing, Figma) é um template comprado, usado agora como scaffold
estrutural — não necessariamente como identidade visual final.

## Tipografia e cor
Ver @context/tokens.md — valores reais extraídos do Figma via Styles.
A tipografia (DM Sans + escala) pode ser tratada como confirmada.
A paleta (preto/branco/escala de cinza) ainda não foi confrontada com o
off-white/near-black já usado no sistema HTML existente do Paladino —
tratar como referência estrutural, não como decisão final de cor.

## Padrão estrutural
Componentes do arquivo de origem seguem 3 variantes tonais: light, gray, dark.
Preservar essa lógica em qualquer código gerado.

## Conteúdo de teste
Ver @content/test-copy.md — usar esse texto no lugar de lorem ipsum ou
texto genérico ao gerar componentes de teste.

## Logo
assets/logo/ — versões white e black, SVG.

## Não fazer
- Não gerar componentes além do que foi pedido no prompt.
- Não inventar cor, peso de fonte ou espaçamento fora do que está em tokens.md.
- Não tratar a paleta preto/branco/cinza como definitiva sem confirmação.
