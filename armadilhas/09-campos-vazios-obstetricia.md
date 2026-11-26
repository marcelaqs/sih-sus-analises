# 09. Campos sempre vazios em internações obstétricas

**Campos:** `VAL_SANGUE`, `VAL_UCI`, `INFEHOSP`, `GESTRISCO`, `NUM_FILHOS`

## O que acontece

Nas internações obstétricas, esses campos vêm praticamente sempre zerados ou vazios, embora os nomes sugiram informações úteis (transfusão, cuidado intermediário, infecção hospitalar, gestação de risco, número de filhos).

## Por que importa para predição

- Um campo constante não contribui para o modelo e pode passar despercebido numa seleção automática de variáveis.
- Pela descrição, parecem preditores clínicos importantes, mas não podem ser usados.

## Como lidar

- Verificar a distribuição de cada campo no recorte do estudo antes de incluí-lo.
- Relatar no artigo os campos descartados por falta de preenchimento.

## Fonte

Análise da coorte obstétrica do projeto (2015–2025).
