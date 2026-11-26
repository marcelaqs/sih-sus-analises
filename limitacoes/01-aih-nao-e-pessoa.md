# 01. AIH não é pessoa

**Campos:** `N_AIH`, `IDENT`

## O que acontece

Cada linha do arquivo RD é uma AIH, que é um documento de cobrança. Uma mesma internação pode gerar mais de uma AIH (por exemplo, AIH de continuação, `IDENT` = 5, em internações longas), e a mesma pessoa pode ter várias internações. O RD não traz identificador da pessoa. O número do Cartão Nacional de Saúde (CNS) passou a ser exigido aos poucos a partir de 2004 (Portaria SAS/MS nº 389/2004), mas não é divulgado nos arquivos públicos.

Desde a competência ago/2015, o SIHD2 bloqueia AIH do mesmo CNS com internações sobrepostas ou com intervalo de até 3 dias, e o bloqueio de homônimos passa a valer só para AIH sem CNS (Nota Técnica SIHD2 nº 001/2015). A regra de duplicidade muda, então, no meio da série.

## Por que importa na análise epidemiológica

- O número de linhas não é o número de internações nem de pessoas.
- AIH da mesma internação ou da mesma pessoa podem cair uma no treino e outra no teste, o que infla o desempenho do modelo (vazamento).
- Desfechos como óbito e preditores como tempo de permanência ficam repetidos ou fracionados entre AIH.

## Como lidar

- Definir a unidade de análise (AIH, internação ou pessoa) antes de modelar.
- Tratar AIH de continuação: agregar à internação ou excluir, de forma explícita.
- Quando a pessoa importa, usar linkage com outra fonte e dividir treino e teste por pessoa ou por tempo.

## Fonte

Manual Técnico Operacional do SIH (ver [`../referencias/`](../referencias/)); Portaria SAS/MS nº 389/2004; Nota Técnica SIHD2 nº 001/2015.
