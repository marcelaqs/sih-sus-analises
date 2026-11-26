# 05. "Ignorado" que não é ignorado

**Campos:** `ETNIA`, `RACA_COR`, `SEXO`

## O que acontece

Várias tabelas CNV do DATASUS começam com uma linha que cobre todos os códigos ("Ignorado 00–99") e depois listam os válidos. Ferramentas que expandem essa linha rotulam como ignorado qualquer código não listado.

- **Etnia:** o campo existe desde a competência out/2010 e só é exigido para raça/cor indígena (Portaria SAS/MS nº 508/2010). O código 0000 vem em quase todas as AIH, inclusive de pacientes não indígenas. Rotulado como "não informado", ele faz qualquer medida de completude da etnia sair errada.
- **Sexo:** o leiaute oficial do RD define 1 = masculino e 3 = feminino. O 2 não tem documentação, mas o TabWin o rotula como feminino.

## Por que importa na análise epidemiológica

- Completude calculada sobre rótulos expandidos não descreve a qualidade real do campo.
- Categorias "ignorado" artificiais entram no modelo como se fossem informação.
- Raça/cor e etnia são centrais para avaliar a equidade do modelo; um rótulo errado distorce essa avaliação.

## Como lidar

- Decodificar só os códigos citados nas fontes oficiais; manter os demais como sem rótulo.
- Descrever a etnia restrita às pacientes indígenas (raça/cor = indígena).
- Tratar o sexo pelos códigos documentados.

## Fonte

Portaria SAS/MS nº 508/2010; pacote `TAB_SIH` (arquivos CNV); leiaute do RD (`Layout_REDUZIDA.pdf`); revisão do dicionário no [omnisus](https://github.com/raphaelfh/omnisus).
