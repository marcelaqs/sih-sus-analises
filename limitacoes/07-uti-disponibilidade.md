# 07. Campos de UTI medem disponibilidade

**Campos:** `UTI_MES_TO`, `MARCA_UTI`

## O que acontece

Os campos de UTI registram diárias de UTI cobradas. Só há cobrança quando o hospital tem leito de UTI habilitado no SUS e disponível. Por isso, esses campos refletem a estrutura do hospital tanto quanto a gravidade da paciente.

## Por que importa na análise

- Usar a UTI como marcador de gravidade (por exemplo, para morbidade materna grave) classifica de forma diferente mulheres igualmente graves em hospitais com e sem UTI.
- Como preditor, a UTI carrega informação sobre o hospital e a região, e pode piorar o desempenho do modelo justamente onde há menos leitos.

## Como lidar

- Não usar a UTI isoladamente como critério de gravidade.
- Avaliar o desempenho do modelo por tipo de estabelecimento e por região.
- Atenção aos tipos: a UTI tipo I (códigos 74 e 77) foi reclassificada como Unidade de Cuidados Intermediários em 2019, mas o código 74 continua aparecendo no RD. A Portaria SAS/MS nº 298/2019 também excluiu da tabela as diárias de UTI I e criou diárias próprias de UCI, que não aparecem nos campos de UTI do RD. A UCI adulto e pediátrica não tem campo no RD: `UTI_INT_TO` e `MARCA_UCI` só cobrem UCI neonatal.

## Fonte

Análise da coorte obstétrica do projeto (2015–2025); Informe Técnico SIH 2016-03; Portarias SAS/MS nº 298/2019, SAES/MS nº 1.202/2023 e nº 3.511/2025.
