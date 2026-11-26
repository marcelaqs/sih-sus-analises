# 06. Causa externa no diagnóstico secundário

**Campos:** `DIAG_PRINC`, `DIAG_SECUN`, `DIAGSEC1`

## O que acontece

Em internações por lesões e envenenamentos (capítulo XIX da CID-10), o diagnóstico principal registra a lesão, e a causa externa (capítulo XX) vai no primeiro diagnóstico secundário.

## Por que importa para predição

Desfechos ou preditores ligados a violência, acidentes e outras causas externas não aparecem no diagnóstico principal. Buscar só no `DIAG_PRINC` subestima esses casos, o que pesa em estudos sobre violência contra a mulher.

## Como lidar

- Buscar causas externas nos diagnósticos secundários.
- Os campos `DIAGSEC1` a `DIAGSEC9` entraram com a Portaria SAS/MS nº 1.324/2014; antes dela, buscar no `DIAG_SECUN`.

## Fonte

Manual Técnico Operacional do SIH; Portaria SAS/MS nº 1.324/2014 (ver [`../normas/`](../normas/)).
