# 02. Competência não é data de internação

**Campos:** `ANO_CMPT`, `MES_CMPT`, `DT_INTER`, `DT_SAIDA`

## O que acontece

Os arquivos do DATASUS são organizados por competência, o mês de processamento da cobrança. Uma AIH pode ser apresentada meses depois da alta. Na AIH de continuação (`IDENT` = 5), `DT_INTER` repete a data da primeira AIH, então datas antigas em competências recentes são esperadas.

## Por que importa para predição

- Selecionar um período pela competência não seleciona as internações daquele período.
- Uma divisão temporal de treino e teste feita pela competência mistura internações de períodos diferentes.
- Os últimos meses disponíveis estão incompletos, porque parte das AIH ainda não foi apresentada.

## Como lidar

- Definir o período do estudo pela data de internação ou de saída.
- Baixar competências posteriores ao fim do período para capturar as AIH apresentadas com atraso.
- Fazer a divisão temporal pela data de internação.

## Fonte

Manual Técnico Operacional do SIH, p. 8 (edição a registrar em [`../referencias/`](../referencias/)).
