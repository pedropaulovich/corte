# Calculadora de Corte de Mangas

Calculadora para otimizar o corte e a enfestada de mangas filtrantes industriais (corpo, boca, fundo e reforço), a partir dos dados do cliente e das medidas do rolo de feltro.

## Como usar

Abra `corte.html` no navegador (funciona offline, sem instalar nada — inclusive no Chrome do celular).

### Dados do cliente (sempre em mm)

- **F.E.** — furo espelho
- **L** — comprimento da manga
- **Boca** — bainha ou aço mola
- **Reforço** — nenhum, somente na boca, somente no fundo, ou nos dois
- **E** — altura do reforço (se houver)
- **Quantidade de mangas** do pedido

Marque as caixas **Corpo / Boca / Fundo** para escolher quais peças entram no pedido — dá pra combinar as três, só duas, ou uma só (por exemplo, um pedido de reposição só de fundo).

### Parâmetros de corte

- **Ajuste lateral** — quanto se apara da lateral do rolo para deixar retilíneo
- **Altura do rolo, útil** — largura fixa do rolo (o limite físico que não muda)
- **Comprimento total do rolo** — quanto tem disponível para puxar
- **Máx. camadas por enfestada** — limite de empilhamento da máquina de corte (opcional)

## O que a calculadora faz

1. Calcula as dimensões de cada peça a partir das fórmulas do cliente (A, B, C, D, E, F).
2. Testa as duas orientações de corte de cada peça (girada 90° ou não) e escolhe a que gasta menos feltro — já que a altura do rolo é fixa, mas o comprimento se estende desenrolando mais rolo.
3. Monta a enfestada combinando peças: a peça mais larga abre uma seção de comprimento, e peças mais estreitas pegam "carona" na sobra de largura ao lado dela, sem gastar comprimento extra.
4. Compara **cortar tudo separado** vs **sua seleção combinada** — em área de feltro (m²) e número de enfestadas — mostrando quando vale a pena misturar peças ou não.
5. Deixa testar manualmente qualquer número de camadas, comparando com o ótimo sugerido.
6. Se uma peça vai ser aproveitada de retalho (sobra de outro corte), marque **Retalho** no seletor dela — ela sai da conta do rolo e some da comparação.

## Arquivos

- `corte.html` — a calculadora (arquivo único, sem dependências externas)
- `README.md` — este arquivo
