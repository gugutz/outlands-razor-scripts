**activate-char-aspect**

Este script ativa o aspecto do personagem com algumas condições:

- Se o char tem magery, ele vai tentar ativar o aspecto do book
- Se o char nao tem magery, ele tenta ativar o aspecto da arma
- Se o char tem herding, e ele encontra um crook sem aspecto na bag, ele desequipa as mãos, equipa o crook e ativa o aspecto de arma no crook, tira o crook da mão e re-coloca o livro/arma
- Se o char esta de maos vazias, ele tenta achar e equipar um livro (caso o char seja mage)
- Ativa o aspecto da armadura

O script nao seleciona aspecto pra ativar, apenas trabalha com os aspectos que já estão selecionados na janela de Aspectos
