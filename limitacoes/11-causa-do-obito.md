# 11. Causa do óbito não está no SIH

**Campos:** `CID_MORTE`, `CID_ASSO`, `MORTE`

## O que acontece

A Portaria SAS/MS nº 718/2006 tornou obrigatória a CID da causa da morte na AIH quando o motivo de saída é óbito, a partir da competência set/2006. A Portaria SAS/MS nº 1.324/2014 (hoje no art. 308 da Portaria de Consolidação SAES/MS nº 1/2022) excluiu do layout da AIH os campos "Diagnóstico da Causa Morte" e "Diagnóstico Causas Complementares", com efeitos a partir de jan/2015. Desde 2015, `CID_MORTE` e `CID_ASSO` vêm `0000` em todas as AIH, inclusive nas de óbito.

## Por que importa para predição

- Um desfecho por causa específica de óbito (por exemplo, óbito materno por hemorragia) não pode ser construído pelo `CID_MORTE` a partir de 2015.
- O campo só é obrigatório nos óbitos de set/2006 a dez/2014; antes disso, o preenchimento não era exigido.
- Em séries que atravessam 2015, o campo parece "perder" preenchimento, quando na verdade foi extinto.

## Como lidar

- Para a causa do óbito, usar o SIM (com linkage, quando possível).
- No SIH, restam `DIAG_PRINC` e `DIAGSEC1` a `DIAGSEC9`, que descrevem a internação, não a causa do óbito.

## Fonte

Portaria SAS/MS nº 718/2006; Portaria SAS/MS nº 1.324/2014; Portaria de Consolidação SAES/MS nº 1/2022, art. 308; conferência em arquivos RD de São Paulo e Roraima (revisão do omnisus).
