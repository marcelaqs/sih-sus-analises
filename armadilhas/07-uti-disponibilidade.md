# 07. Campos de UTI medem disponibilidade

**Campos:** `UTI_MES_TO`, `MARCA_UTI`

## O que acontece

Os campos de UTI registram diárias de UTI cobradas. Só há cobrança quando o hospital tem leito de UTI habilitado no SUS e disponível. Por isso, esses campos refletem a estrutura do hospital tanto quanto a gravidade da paciente.

## Por que importa para predição

- Usar a UTI como marcador de gravidade (por exemplo, para morbidade materna grave) classifica de forma diferente mulheres igualmente graves em hospitais com e sem UTI.
- Como preditor, a UTI carrega informação sobre o hospital e a região, e pode piorar o desempenho do modelo justamente onde há menos leitos.

## Como lidar

- Não usar a UTI isoladamente como critério de gravidade.
- Avaliar o desempenho do modelo por tipo de estabelecimento e por região.

## Fonte

Análise da coorte obstétrica do projeto (2015–2025); Manual Técnico Operacional do SIH.
