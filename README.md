# Alinhamento — Selah Prayer House

Página única (HTML, CSS e JavaScript no mesmo ficheiro, sem dependências) para a
equipa de coordenação planear, imprimir e acompanhar ao vivo o alinhamento do evento.

**Endereço:** https://p9n77w5dm2-jpg.github.io/selah-alinhamento/

## Como usar

- **Planeamento:** blocos com tipo, duração, responsável, local e notas. Entre cada
  par de blocos há uma transição com checklist (palco, som, luz, projeção, pessoas,
  espaço). As horas são calculadas a partir da hora de início do dia; reordena-se com
  as setas ou a arrastar (também ao toque).
- **Imprimir:** uma página A4 por dia, com a checklist de cada transição.
- **Ao vivo:** relógio, momento atual com contagem decrescente, próximo momento com a
  checklist da transição, desvio acumulado e fim projetado. «Avançar» regista a hora
  real; −5/−1/+1/+5 encurtam ou alongam o momento atual. No portátil, → ou Page Down
  avança e Ctrl+Z desfaz.

## Dados

Tudo fica guardado no navegador de cada dispositivo (localStorage); nada é enviado
para o GitHub. Para passar o alinhamento para outro dispositivo: **Dados › Exportar
JSON** num, **Dados › Importar JSON** no outro. **Repor dados de exemplo** volta ao
programa original.

## Publicação

O GitHub Pages serve a partir do `main`, pasta raiz
(**Settings → Pages → Deploy from a branch → `main` / `(root)`**).
Basta fazer push de `index.html`.
