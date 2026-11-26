# sih-predicao-sus

Considerações sobre o SIH/SUS para modelos preditivos: campos, códigos e normas.

O Sistema de Informações Hospitalares (SIH/SUS) é uma base de faturamento. Vários campos registram o que foi cobrado, não o que aconteceu com a paciente, e alguns códigos mudaram de sentido ao longo dos anos. Para quem desenvolve modelos preditivos, isso gera erros silenciosos: variáveis que parecem informativas, mas medem outra coisa, e vazamento de informação entre treino e teste.

Este repositório reúne essas armadilhas, com a fonte oficial de cada uma, como base para o artigo sobre o uso do SIH em predição no SUS.

**Status:** em construção (nov/2026).

## Conteúdo

| Pasta | O que tem |
| --- | --- |
| [`armadilhas/`](armadilhas/) | Uma nota por armadilha: campo, período, por que importa para predição, como lidar e fonte |
| [`normas/`](normas/) | Portarias e notas técnicas citadas, com link oficial e SHA-256 da cópia local |
| [`referencias/`](referencias/) | Manuais, leiautes, dicionários e fontes secundárias |

## Armadilhas

| Nº | Armadilha | Campos |
| --- | --- | --- |
| 01 | [AIH não é pessoa](armadilhas/01-aih-nao-e-pessoa.md) | `N_AIH`, `IDENT` |
| 02 | [Competência não é data de internação](armadilhas/02-competencia-nao-e-internacao.md) | `ANO_CMPT`, `MES_CMPT`, `DT_INTER`, `DT_SAIDA` |
| 03 | [Códigos que mudam de sentido no tempo](armadilhas/03-codigos-mudam-no-tempo.md) | `COBRANCA`, `HOMONIMO`, `ESPEC` |
| 04 | [Óbito materno fora dos motivos 41 a 43](armadilhas/04-obito-materno-motivos.md) | `COBRANCA`, `MORTE` |
| 05 | ["Ignorado" que não é ignorado](armadilhas/05-ignorado-falso.md) | `ETNIA`, `RACA_COR`, `SEXO` |
| 06 | [Causa externa no diagnóstico secundário](armadilhas/06-causa-externa.md) | `DIAG_PRINC`, `DIAG_SECUN`, `DIAGSEC1` |
| 07 | [Campos de UTI medem disponibilidade](armadilhas/07-uti-disponibilidade.md) | `UTI_MES_TO`, `MARCA_UTI` |
| 08 | [Procedimento realizado é o faturado](armadilhas/08-procedimento-faturado.md) | `PROC_REA` |
| 09 | [Campos sempre vazios em internações obstétricas](armadilhas/09-campos-vazios-obstetricia.md) | `VAL_SANGUE`, `VAL_UCI`, `INFEHOSP`, `GESTRISCO`, `NUM_FILHOS` |
| 10 | [Códigos sem rótulo nas tabelas oficiais](armadilhas/10-codigos-sem-rotulo.md) | `ESPEC` |
| 11 | [Causa do óbito não está no SIH](armadilhas/11-causa-do-obito.md) | `CID_MORTE`, `CID_ASSO` |
| 12 | [Raça/cor muda de regra no tempo](armadilhas/12-raca-cor-no-tempo.md) | `RACA_COR` |
| 13 | [Diárias de acompanhante não mostram a presença do acompanhante](armadilhas/13-diarias-acompanhante.md) | `DIAR_ACOM` |
| 14 | [Diárias cobradas não são tempo de permanência](armadilhas/14-diarias-nao-sao-permanencia.md) | `QT_DIARIAS`, `DIAS_PERM` |

## Relação com o omnisus

Parte destas armadilhas foi identificada na revisão do dicionário do SIH no [omnisus](https://github.com/raphaelfh/omnisus), feita com a Letícia. As correções do dicionário seguem por pull request no omnisus; aqui ficam as consequências para a análise preditiva.

## Autoria

Marcela Quaresma Soares, LABDAPS, Faculdade de Saúde Pública da USP.

## Licença

Textos e tabelas: [CC BY 4.0](LICENSE). Documentos oficiais em `normas/` são públicos.
