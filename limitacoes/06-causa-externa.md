# 06. Causa externa no diagnóstico secundário

**Campos:** `DIAG_PRINC`, `DIAG_SECUN`, `DIAGSEC1`

## O que acontece

Em internações por lesões e envenenamentos (capítulo XIX da CID-10), o diagnóstico principal registra a lesão, e a causa externa (capítulo XX, códigos V01 a Y98) vai no primeiro campo de CID secundário. Nos politraumatizados, as demais lesões vão nos outros campos de CID secundário.

O caráter de atendimento também tem códigos para acidentes e lesões (03 a 06), definidos pela Portaria SAS/MS nº 719/2007, art. 4º. Na conferência de arquivos de São Paulo (revisão do omnisus), esses códigos só aparecem com diagnóstico principal S ou T, mas a maioria das AIH com S ou T traz caráter 01 (eletivo) ou 02 (urgência).

## Por que importa na análise

Desfechos ou preditores ligados a violência, acidentes e outras causas externas não aparecem no diagnóstico principal. Buscar só no `DIAG_PRINC` subestima esses casos, o que pesa em estudos sobre violência contra a mulher.

## Como lidar

- Buscar causas externas nos diagnósticos secundários.
- Não usar o caráter de atendimento 03 a 06 como marcador de causa externa: ele deixa de fora a maior parte dos casos.
- Os campos de CID secundário (`DIAGSEC1` em diante) entraram com a Portaria SAS/MS nº 1.324/2014, com efeitos a partir de jan/2015; antes, buscar no `DIAG_SECUN`.

## Fonte

Manual Técnico Operacional do SIH; Portaria SAS/MS nº 1.324/2014, art. 3º, § 2º (ver [`../normas/`](../normas/)).
