# 14. Diárias cobradas não são tempo de permanência

**Campos:** `QT_DIARIAS`, `DIAS_PERM`

## O que acontece

`QT_DIARIAS` conta as diárias cobradas, que incluem o último dia quando o motivo de saída é permanência, óbito ou transferência. Nesses casos, costuma ser `DIAS_PERM` + 1.

## Por que importa na análise epidemiológica

O tempo de permanência é desfecho e preditor frequente. Usar `QT_DIARIAS` superestima a permanência justamente nos óbitos e nas transferências, o que cria uma associação artificial com o desfecho.

## Como lidar

- Usar `DIAS_PERM` (ou a diferença entre `DT_SAIDA` e `DT_INTER`) para o tempo de permanência.

## Fonte

Manual Técnico Operacional do SIH, 2012, pp. 12–13.
