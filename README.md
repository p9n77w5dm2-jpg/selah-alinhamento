# Alinhamento — Selah Prayer House

Página única (HTML, CSS e JavaScript no mesmo ficheiro, sem dependências) com o programa,
os postos de apoio e as fotos do espaço do evento, para a equipa consultar e imprimir.

**Endereço:** https://p9n77w5dm2-jpg.github.io/selah-alinhamento/

## Como usar

O site é **só de leitura**: todos veem a mesma versão e ninguém a altera no navegador
(as alterações são feitas pela coordenação, ver «Alterar o programa»).

- **Programa:** os blocos com hora, duração, responsável, local, repertório (músicas) e
  notas; entre cada par de blocos, a transição com a checklist (palco, som, luz, pessoas,
  espaço). As horas são calculadas a partir da hora de início do dia.
- **Fotos do espaço:** o atalho com a miniatura, no cartão do evento, abre a aba Postos já com
  as fotos (vista aérea e planta) à vista; um toque numa imagem amplia. As imagens vão
  embutidas no ficheiro, mas só são descodificadas quando se abrem.
- **Postos:** os postos de apoio (estacionamento, apoio ao público…): onde, quando, quantas
  pessoas, o que fazer e quem fica em cada um (um nome vazio aparece como «a definir»). Sem
  horas, o posto conta para todo o evento.
- **Imprimir:** uma página A4 por dia, com a checklist de cada transição, e uma página com os
  postos (com uma linha para escrever os nomes em falta).

Ligações diretas para mandar à equipa: `…/selah-alinhamento/#postos` abre a aba Postos;
`…/#fotos` abre-a já com as fotos à vista (o antigo `…/#esquema` continua a funcionar).

## Alterar o programa

O programa, os postos e as notas estão em `exampleState()`, no `index.html`: altera-se aí,
testa-se localmente e publica-se com um push (ver «Publicação»). A lista de transições segue a
ordem dos blocos: a primeira fica entre o 1.º e o 2.º bloco, e assim por diante.

## Dados

Cada navegador só guarda as preferências (aba, dia e tema) em localStorage; nada é enviado
para o GitHub. As cópias guardadas pelas versões anteriores, que tinham o programa (às vezes
editado) e o ao vivo, são ignoradas e substituídas pelas preferências na primeira visita.

## Atualizações

Depois de um push, quem abre ou recarrega a página vê logo a versão nova. Quem já a tem
aberta vê «Há uma versão nova do programa publicada» em poucos minutos (a página compara-se
com a publicada ao voltar ao separador e de ~4 em ~4 min) e toca em **Atualizar**.

A chave `selah-alinhamento-v1` mantém-se de propósito: as páginas abertas com versões
anteriores só reconhecem a versão nova se a encontrarem no script publicado.

## Publicação

O GitHub Pages serve a partir do `main`, pasta raiz
(**Settings → Pages → Deploy from a branch → `main` / `(root)`**).
Basta fazer push de `index.html`.
