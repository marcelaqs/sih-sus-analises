# 12. Raça/cor muda de regra no tempo

**Campo:** `RACA_COR`

## O que acontece

- **2008:** a Portaria SAS/MS nº 719/2007 inclui raça/cor no SIA e no SIH, autodeclarada pelo usuário ou responsável, com efeitos a partir de jan/2008. Antes disso, o campo não existe no SIH.
- **2010:** a etnia entra a partir da competência out/2010, exigida só para raça/cor indígena (Portaria SAS/MS nº 508/2010).
- **2014:** a partir de nov/2014, pela Portaria SAS/MS nº 1.134/2014, quando a AIH traz o Cartão Nacional de Saúde, os dados cadastrais vêm do CADSUS e não podem ser alterados na AIH. A raça/cor pode vir do cadastro, e não de uma pergunta feita na internação.
- **2023:** a partir da competência abr/2023, o SIH não aceita mais raça/cor 99 (sem informação). Internações anteriores apresentadas depois ainda podem trazer o 99.

## Por que importa na análise

- A queda da proporção sem informação ao longo do tempo é, em parte, efeito de regra, não de melhora do registro.
- Um modelo treinado antes de 2023 e aplicado depois encontra a categoria 99 vazia.
- Na avaliação de equidade do modelo, a origem da informação (autodeclaração ou cadastro) muda o que a variável mede.

## Como lidar

- Descrever a completude de raça/cor por período, separando antes e depois de abr/2023.
- Definir o tratamento da categoria 99 antes da divisão treino/teste.

## Fonte

Portarias SAS/MS nº 719/2007, nº 508/2010 e nº 1.134/2014; informe do DATASUS à 3ª reunião ordinária da CIT de 2023 (ver [`../normas/`](../normas/)).
