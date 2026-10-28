# Alinhamento — Selah Prayer House

Página única (HTML, CSS e JavaScript no mesmo ficheiro, sem dependências) para a
equipa de coordenação planear, imprimir e acompanhar ao vivo o alinhamento do evento.

**Endereço:** https://p9n77w5dm2-jpg.github.io/selah-alinhamento/

## Como usar

- **Planeamento:** blocos com tipo, duração, responsável, local, repertório (músicas)
  e notas. Entre cada
  par de blocos há uma transição com checklist (palco, som, luz, pessoas, espaço; não há
  projeção neste evento). As horas são calculadas a partir da hora de início do dia; reordena-se com
  as setas ou a arrastar (também ao toque).
- **Postos:** aba com os postos de apoio (estacionamento, apoio ao público…): onde, quando,
  quantas pessoas, o que fazer e quem fica em cada um (um nome vazio aparece como «a definir»).
  Sem horas, o posto conta para todo o evento. O **esquema do espaço** (vista aérea e planta)
  está nesta aba, numa secção fechada: as imagens só carregam quando se abre, e um toque amplia.
  O botão «Esquema do espaço» no cartão do evento leva lá diretamente. Para mandar à equipa:
  `…/selah-alinhamento/#postos` abre a aba; `…/#esquema` abre-a já com o esquema à vista.
- **Imprimir:** uma página A4 por dia, com a checklist de cada transição, e uma página com os
  postos (com uma linha para escrever os nomes em falta).
- **Ao vivo:** relógio, momento atual com contagem decrescente, próximo momento com a
  checklist da transição, desvio acumulado e fim projetado. «Avançar» regista a hora
  real; −5/−1/+1/+5 encurtam ou alongam o momento atual. No portátil, → ou Page Down
  avança e Ctrl+Z desfaz.

## Dados

Tudo fica guardado no navegador de cada dispositivo (localStorage); nada é enviado
para o GitHub. Para passar o alinhamento para outro dispositivo: **Dados › Exportar
JSON** num, **Dados › Importar JSON** no outro. **Repor dados de exemplo** volta ao
programa publicado.

## Atualizações

O alinhamento embutido em `index.html` é a versão publicada. Cada cópia guardada lembra-se
da versão de onde partiu (`seed`, impressão digital do conteúdo), por isso, depois de um push:

- quem não mexeu nos dados recebe a versão nova sozinho ao abrir ou recarregar a página
  («Alinhamento atualizado para a versão mais recente»);
- quem tem alterações próprias, ou está com o ao vivo a decorrer, vê um aviso e escolhe
  **Atualizar** (dá para anular) ou **Manter a deste dispositivo**;
- quem tem a página aberta vê «Há uma versão nova do alinhamento publicada» em poucos
  minutos (a página compara-se com a publicada ao voltar ao separador e de ~4 em ~4 min).

Os blocos, o dia e os itens das checklists do exemplo têm ids fixos (`b-abertura`, `dia-1`,
`c-…`): numa versão nova, o progresso ao vivo e a checklist marcada continuam a corresponder.
Ao mudar o exemplo, mantenha o id dos blocos que continuam. As cópias guardadas antes de
27/10/2026 (sem `seed`) são reconhecidas pelas impressões digitais em `LEGACY_SEEDS`.

## Publicação

O GitHub Pages serve a partir do `main`, pasta raiz
(**Settings → Pages → Deploy from a branch → `main` / `(root)`**).
Basta fazer push de `index.html`.
