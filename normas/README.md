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
| `publicacao` | Diário Oficial (seção e página) ou outra publicação |
| `link_oficial` | Endereço no DOU, Saúde Legis ou BVS-MS |
| `arquivo_local` | Cópia em [`pdf/`](pdf/) |
| `sha256` | Hash da cópia local, para saber exatamente qual versão foi lida |
| `armadilhas` | Números das armadilhas que usam a norma |

## Como acrescentar uma norma

1. Salve o PDF em `pdf/` com o nome do `id` (por exemplo, `portaria-saes-245-2020.pdf`).
2. Calcule o hash: `sha256sum pdf/arquivo.pdf` (Linux/macOS) ou `Get-FileHash pdf\arquivo.pdf` (PowerShell).
3. Acrescente a linha em `normas.csv`.

Atos oficiais não têm proteção de direito autoral (Lei nº 9.610/1998, art. 8º, IV), por isso as cópias podem ficar aqui.
