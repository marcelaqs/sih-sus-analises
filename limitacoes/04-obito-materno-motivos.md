# 04. Óbito materno fora dos motivos 41 a 43

**Campos:** `COBRANCA`, `MORTE`

## O que acontece

Desde set/2010, a AIH de parto tem motivos de saída próprios (61 a 67), incluídos pela Portaria SAS/MS nº 384/2010. O óbito da mulher aparece também nos códigos 65 (óbito da gestante e do concepto), 66 e 67 (óbito da mãe com alta ou permanência do recém-nascido), e não só nos códigos de óbito 41 a 43.

## Por que importa para predição

Quem define o óbito materno hospitalar só pelos motivos 41 a 43 perde casos, e o desfecho fica subestimado justamente na AIH de parto.

## Como lidar

- Incluir os motivos 65 a 67 na definição de óbito materno a partir de set/2010.
- Não usar todo código de 61 a 67 com "óbito" no rótulo: 63 e 64 registram o óbito do recém-nascido ou fetal. Em arquivos de São Paulo de 2014 a 2025, 65 a 67 vêm sempre com `MORTE` = 1 e 61 a 64 com `MORTE` = 0: `MORTE` marca a morte da mulher, não a do concepto.

## Fonte

Manual Técnico Operacional do SIH, set/2012, pp. 12–13; conferência nos dados na revisão do [omnisus](https://github.com/raphaelfh/omnisus) (PR #240).
