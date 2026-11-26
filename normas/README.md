# Normas

Portarias e notas técnicas que definem ou alteram campos e códigos do SIH citados nas [limitações](../limitacoes/).

A tabela [`normas.csv`](normas.csv) tem uma linha por norma:

| Coluna | Conteúdo |
| --- | --- |
| `id` | Identificador curto, usado nas limitações |
| `tipo`, `numero`, `data`, `orgao` | Identificação da norma |
| `assunto` | O que a norma muda no SIH |
| `situacao` | Vigente, alterada ou revogada |
| `alterada_por` | `id` da norma que alterou ou revogou esta |
| `link_oficial` | Endereço no Saúde Legis (BVS-MS) ou outra fonte oficial |
| `arquivo_local` | Cópia em [`pdf/`](pdf/), quando houver |
| `sha256` | Hash do documento (do link ou da cópia local), lido entre 24 e 26/11/2026; mostra exatamente qual versão foi usada |
| `limitacoes` | Números das limitações que usam a norma |

Os links e os hashes vêm do registro de fontes da revisão do SIH no [omnisus](https://github.com/marcelaqs/omnisus) (`src/omnisus/data/dicionarios/sources/registry.json`), onde cada documento foi baixado e conferido. Linhas sem link ainda não têm cópia registrada.

## Portarias de consolidação

Boa parte das portarias antigas está hoje reunida em portarias de consolidação, que citam a origem de cada artigo. A coluna `situacao` indica onde cada norma foi consolidada, quando foi. Conferido em 26/11/2026:

| Consolidação | O que traz para o SIH |
| --- | --- |
| [PRC SAES/MS nº 1/2022](https://bvsms.saude.gov.br/bvs/saudelegis/saes/2022/prc0001_31_03_2022_comp.html) | Regulamento da AIH (arts. 291 e seguintes): 718/2006 (art. 298), 1.324/2014 (arts. 308 a 312). SIA e SIH (arts. 393 e seguintes): 472/2008 (arts. 400 a 402) |
| [PRC GM/MS nº 3/2017](https://bvsms.saude.gov.br/bvs/saudelegis/gm/2017/prc0003_03_10_2017_comp.html) | Acompanhante no parto: 2.418/2005 (art. 92) |
| [PRC GM/MS nº 2/2017](https://bvsms.saude.gov.br/bvs/saudelegis/gm/2017/prc0002_03_10_2017.html) | Nenhuma das normas desta tabela |

Não aparecem nessas três: as normas de raça/cor e etnia (719/2007, 508/2010), a 1.134/2014 (CADSUS), as de UTI (298/2019, 1.202/2023, 3.511/2025), a 245/2020, a 389/2004, a 321/2007, a 1.541/2007 e a 3.462/2010. As portarias do Gabinete do Ministro podem estar em outras consolidações de 2017 (por exemplo, a nº 1 ou a nº 6), ainda não conferidas.

## Como acrescentar uma norma

1. Acrescente a linha em `normas.csv`.
2. Se guardar uma cópia, salve em `pdf/` com o nome do `id` e calcule o hash: `sha256sum pdf/arquivo` (Linux/macOS) ou `Get-FileHash pdf\arquivo` (PowerShell).

Atos oficiais não têm proteção de direito autoral (Lei nº 9.610/1998, art. 8º, IV), por isso as cópias podem ficar aqui.
