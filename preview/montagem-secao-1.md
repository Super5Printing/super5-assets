# Montagem nativa da seção 1 — Wix Studio

Site: **superfiveprinting** · ID `3328108e-da15-4c4f-b03d-431ff5a0a8a0`
Canvas de referência: **1920 × 1047 px** (breakpoint Desktop)

Todas as medidas abaixo já estão convertidas do PDF para pixels nesse canvas. Se o seu editor
estiver em outra largura, os valores escalam proporcionalmente — mas monte no Desktop primeiro.

---

## Passo 1 — Preparar a seção

1. Abra o editor do site e apague qualquer seção que tenha vindo por padrão.
2. Adicione uma seção nova e renomeie para `Hero — Kit Start` (clique com o botão direito na
   seção → Rename, ou pelo painel de Layers).
3. Na aba de tamanho da seção, defina altura **fixa de 1047 px**. Não deixe em "Auto" —
   o posicionamento absoluto das camadas depende de a altura ser conhecida.
4. Cor de fundo da seção: `#3B2775`. Isso só aparece se alguma imagem falhar ao carregar,
   mas evita um flash branco.
5. Ative **Overflow: Hidden** na seção. Três imagens passam das bordas de propósito e precisam
   ser cortadas.

## Passo 2 — Posicionamento absoluto

Antes de arrastar qualquer imagem: selecione a seção e mude o layout para **Absolute** (no painel
de layout do Studio, a opção que libera posicionar elementos por coordenada em vez de empilhar).

Sem isso, o Studio vai tentar organizar os elementos em fluxo e as coordenadas abaixo não colam.

## Passo 3 — As sete camadas de imagem

Adicione uma a uma, **nesta ordem** (a ordem define quem fica na frente de quem — a primeira
fica atrás de todas). Todas vêm do Media Manager, em Uploads do site.

| # | Arquivo | X | Y | Largura | Altura |
|---|---|---|---|---|---|
| 1 | `s1-01-fundo-roxo.jpg` | 0 | −171 | 1920 | 1288 |
| 2 | `s1-03-modelo-polo.png` | 195 | −213 | 898 | 1628 |
| 3 | `s1-02-glow-azul.png` | 1484 | 198 | 300 | 293 |
| 4 | `s1-02-glow-azul.png` (de novo) | 259 | 576 | 443 | 432 |
| 5 | `s1-04-modelos-camisetas.png` | 60 | 285 | 842 | 882 |
| 6 | `s1-05-mao-cartoes.png` | 291 | 552 | 379 | 508 |
| 7 | `s1-06-atendente.png` | 1491 | 552 | 588 | 588 |

Observações que evitam retrabalho:

- O **Y negativo** nos itens 1 e 2 está certo. O fundo e o modelo de polo são maiores que a
  seção e sangram para cima. Se o Studio não aceitar valor negativo no campo, arraste o
  elemento para cima até o topo sair da seção.
- A **atendente** (item 7) termina em X 2079, ou seja, passa 159 px da borda direita.
  É assim no PDF — ela aparece cortada pela metade.
- O **glow azul** entra duas vezes, em tamanhos diferentes. É a mesma imagem.
- Em cada imagem, defina o modo de preenchimento como **Fit** (ou "Original"), nunca "Fill" —
  Fill recorta e distorce os recortes com transparência.

## Passo 4 — A caixa azul do preço

Adicione uma forma retangular (Shape → Rectangle):

- X 1489 · Y 264 · Largura 292 · Altura 135
- Preenchimento: `#1741C9`
- Borda: nenhuma · Cantos: 0

Ela entra **antes** dos textos do preço, para ficar atrás deles.

## Passo 5 — Os textos

Adicione cada um como uma caixa de texto separada. Cor de todos: `#FFFFFF`.

| Texto | X | Y | Fonte | Tamanho | Entrelinha |
|---|---|---|---|---|---|
| `PROMOÇÃO` | 1470 | 125 | Playfair Display Regular | 45 px | 1.33 |
| `kit Start -Uniformes` | 709 | 139 | Playfair Display **Bold** | 115 px | 1.33 |
| `a partir de` | 1250 | 272 | Playfair Display Regular *itálico* | 46 px | 1.33 |
| `$` | 1504 | 289 | Playfair Display Regular | 60 px | 1.33 |
| `199` | 1543 | 212 | Playfair Display Regular | 144 px | 1.33 |
| `1 polos +` | 1082 | 354 | Anton Regular | 94 px | 1.47 |
| `4 camisetas +` | 976 | 485 | Anton Regular | 94 px | 1.47 |
| `500 cartões` | 1012 | 615 | Anton Regular | 94 px | 1.47 |

Pontos de atenção:

- **Desative o padding interno** das caixas de texto (alguns temas do Studio aplicam
  um espaçamento automático que desloca o texto em relação ao X/Y que você digitou).
- A **entrelinha** importa: foi ela que usei para calcular o Y. Se você deixar no padrão,
  o texto sobe ou desce alguns pixels.
- O `$` e o `199` são duas caixas separadas de propósito — os tamanhos são diferentes
  e o `$` fica alinhado mais alto.
- As três linhas Anton não são uma lista. São três caixas independentes, cada uma com
  X diferente — elas ficam escalonadas, não alinhadas.
- `1 polos +` está no plural, exatamente como no PDF. Só corrija se o Éder aprovar a mudança.

## Passo 6 — O botão

1. Adicione um botão. X 865 · Y 786 · Largura 724 · Altura 111.
2. Fundo `#FFFFFF`, cantos **totalmente arredondados** (raio 999 ou o máximo que o Studio aceitar —
   o formato é de pílula).
3. Texto: `QUERO MEU KIT AGORA` · Anton Regular · 66 px · cor `#3DB784`.
4. Link: **Endereço externo**, abrir em nova aba:

   ```
   https://wa.me/19047490204?text=Ol%C3%A1!%20Quero%20o%20Kit%20Start%20de%20uniformes.
   ```

5. Ícone do WhatsApp: adicione como elemento separado por cima do botão —
   X 1484 · Y 798 · 87 × 87 px, círculo verde `#65CF72` com o símbolo branco.
   O Studio tem esse ícone na biblioteca de ícones sociais.
6. Estado hover: um leve deslocamento para cima e sombra. Não exagere.

## Passo 7 — Tablet e mobile

Troque para o breakpoint mobile e refaça o empilhamento — as coordenadas acima valem só
para o desktop. A ordem no celular:

1. `PROMOÇÃO`
2. Título, quebrado em duas linhas: `kit Start` / `-Uniformes`
3. Linha com `a partir de` + a caixa azul do preço ao lado
4. As três linhas Anton, uma embaixo da outra
5. Botão em **largura total**
6. A imagem `s1-04-modelos-camisetas.png` embaixo, cortada na altura do peito

Esconda no mobile: a atendente, o modelo de polo, a mão com os cartões e os dois glows.
Mantenha o fundo roxo como background da seção, em modo cover.

O arquivo HTML que eu gerei já mostra exatamente esse comportamento — estreite a janela do
navegador e use como referência visual.

## Passo 8 — Antes de publicar

- Clique no botão em cada breakpoint e confirme que abre o WhatsApp certo.
- Teste com o teclado: navegue até o botão com Tab e veja se o foco fica visível.
- Nomeie os elementos no painel de Layers. Quando a página tiver nove seções,
  "Image 47" não ajuda ninguém.
- SEO: o título da página e a descrição ainda precisam ser definidos,
  e cada imagem precisa de texto alternativo.

---

## Texto alternativo das imagens (acessibilidade e SEO)

| Arquivo | Texto alternativo |
|---|---|
| `s1-03-modelo-polo.png` | Homem vestindo camisa polo azul-marinho com logo bordado |
| `s1-04-modelos-camisetas.png` | Quatro modelos vestindo camisetas pretas personalizadas da Super 5 Printing |
| `s1-05-mao-cartoes.png` | Mão segurando cartões de visita impressos |
| `s1-06-atendente.png` | Atendente da Super 5 Printing pronta para atender pelo WhatsApp |
| `s1-01-fundo-roxo.jpg`, `s1-02-glow-azul.png` | Decorativas — deixe o alt vazio |
