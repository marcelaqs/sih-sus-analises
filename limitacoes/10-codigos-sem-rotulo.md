# 10. Códigos sem rótulo nas tabelas oficiais

**Campo:** `ESPEC`

## O que acontece

Alguns códigos aparecem nos dados, mas não estão nas tabelas de decodificação do DATASUS. O código 17 de `ESPEC` foi criado pela Portaria SAES/MS nº 245/2020 ("Estabelecimento Exclusivo UTI SUS"), só para AIH de COVID-19 em estabelecimentos com leitos exclusivos de UTI no SUS, mas não está no `LEITOS.CNV`.

## Por que importa para predição

Códigos sem rótulo viram "ignorado" ou somem em agregações, e um grupo específico de internações (aqui, COVID-19 em UTI exclusiva) fica fora das análises sem que se perceba.

## Como lidar

- Listar os códigos sem rótulo em cada campo antes de modelar.
- Procurar a norma que criou o código.

## Fonte

Portaria SAES/MS nº 245/2020 (ver [`../normas/`](../normas/)).
