# Normas

Portarias e notas técnicas que definem ou alteram campos e códigos do SIH citados nas [armadilhas](../armadilhas/).

A tabela [`normas.csv`](normas.csv) tem uma linha por norma:

| Coluna | Conteúdo |
| --- | --- |
| `id` | Identificador curto, usado nas armadilhas |
| `tipo`, `numero`, `data`, `orgao` | Identificação da norma |
| `assunto` | O que a norma muda no SIH |
| `situacao` | Vigente, alterada ou revogada |
| `alterada_por` | `id` da norma que alterou ou revogou esta |
| `link_oficial` | Endereço no Saúde Legis (BVS-MS) ou outra fonte oficial |
| `sha256` | Hash do documento no link, lido em 24/11/2026; mostra exatamente qual versão foi usada |
| `armadilhas` | Números das armadilhas que usam a norma |

Os links e os hashes vêm do registro de fontes da revisão do SIH no [omnisus](https://github.com/marcelaqs/omnisus) (`src/omnisus/data/dicionarios/sources/registry.json`), onde cada documento foi baixado e conferido. Linhas sem link ainda não têm cópia registrada.

## Como acrescentar uma norma

1. Acrescente a linha em `normas.csv`.
2. Se guardar uma cópia, salve em `pdf/` com o nome do `id` e calcule o hash: `sha256sum pdf/arquivo` (Linux/macOS) ou `Get-FileHash pdf\arquivo` (PowerShell).

Atos oficiais não têm proteção de direito autoral (Lei nº 9.610/1998, art. 8º, IV), por isso as cópias podem ficar aqui.
