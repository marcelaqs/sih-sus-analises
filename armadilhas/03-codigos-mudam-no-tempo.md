# 03. Códigos que mudam de sentido no tempo

**Campos:** `COBRANCA`, `HOMONIMO`, `ESPEC`

## O que acontece

Algumas tabelas de códigos foram trocadas ao longo dos anos, e o mesmo código passou a significar outra coisa.

| Campo | Períodos |
| --- | --- |
| `COBRANCA` (motivo de saída) | Três tabelas: até 2007; 2008 a ago/2010; desde set/2010. O 51 era óbito sem necropsia até 2007 e passa a ser encerramento administrativo em 2008. Desde set/2010 entram os códigos 61 a 67, só para AIH de parto. |
| `HOMONIMO` | Muda de sentido em ago/2015 (Nota Técnica SIHD2 nº 001/2015). |
| `ESPEC` (especialidade do leito) | O 09 era psiquiatria em hospital-dia em 2007; hoje é leito-dia cirúrgico. |

## Por que importa para predição

- Um desfecho ou preditor definido com uma tabela única fica errado para parte dos anos.
- Modelos treinados em um período e aplicados em outro podem estar usando códigos com sentidos diferentes.

## Como lidar

- Decodificar cada campo com a tabela vigente na data da AIH.
- Documentar o período de cada definição de desfecho e preditor.

## Fonte

Nota Técnica SIHD2 nº 001/2015; Manual Técnico Operacional do SIH; Ipea (2019), p. 136.
