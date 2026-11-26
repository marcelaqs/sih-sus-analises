# 02. Competência não é data de internação

**Campos:** `ANO_CMPT`, `MES_CMPT`, `DT_INTER`, `DT_SAIDA`

## O que acontece

Os arquivos do DATASUS são organizados por competência, o mês de processamento da cobrança. Uma AIH pode ser apresentada meses depois da alta. Pela regra em vigor, o mês de produção é o mês da alta; o SIH aceita AIH com alta de até 4 meses antes do mês de processamento, e AIH bloqueadas ou rejeitadas podem ser reapresentadas em até 6 meses da alta (Portaria SAS/MS nº 472/2008, hoje arts. 400 e 401 da Portaria de Consolidação SAES/MS nº 1/2022). Os gestores alimentam mensalmente os bancos nacionais, e a remessa de uma competência só é aceita depois de validada a da competência anterior (Portaria GM/MS nº 3.462/2010, hoje arts. 294 e 295 da Portaria de Consolidação GM/MS nº 1/2017). Na AIH de continuação (`IDENT` = 5), `DT_INTER` repete a data da primeira AIH, então datas antigas em competências recentes são esperadas.

## Por que importa na análise

- Selecionar um período pela competência não seleciona as internações daquele período.
- Uma divisão temporal de treino e teste feita pela competência mistura internações de períodos diferentes.
- Os últimos meses disponíveis estão incompletos, porque parte das AIH ainda não foi apresentada.

## Como lidar

- Definir o período do estudo pela data de internação ou de saída.
- Baixar pelo menos 6 competências posteriores ao fim do período para capturar as AIH apresentadas com atraso.
- Fazer a divisão temporal pela data de internação.

## Fonte

Manual Técnico Operacional do SIH, set/2012, p. 8; Portaria SAS/MS nº 472/2008 (PRC SAES/MS nº 1/2022, arts. 400 a 402); Portaria GM/MS nº 3.462/2010 (ver [`../normas/`](../normas/)).
