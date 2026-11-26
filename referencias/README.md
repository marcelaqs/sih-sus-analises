# Referências

## Oficiais

Portal do SIH no DATASUS: [sihd.datasus.gov.br](http://sihd.datasus.gov.br/documentos/documentos.php), com documentos do SIHD2 e do SISAIH01, notas técnicas e portarias antigas (até 2010). Substitui as páginas antigas do DATASUS como ponto de partida.

Links e SHA-256 do registro de fontes do [omnisus](https://github.com/marcelaqs/omnisus).

| Documento | Edição | Link | SHA-256 (início) |
| --- | --- | --- | --- |
| Manual Técnico Operacional do SIH/SUS | set/2012 | [BVS-MS](https://bvsms.saude.gov.br/bvs/publicacoes/manual_tecnico_sistema_informacao_hospitalar_sus.pdf) | `7429b011ee2a` |
| Informe Técnico SIH/SUS (`IT_SIHSUS_1603.pdf`) | mar/2016 | [FTP DATASUS](ftp://ftp.datasus.gov.br/dissemin/publicos/SIHSUS/200801_/Doc/IT_SIHSUS_1603.pdf) | `1e89d5f2cc41` |
| Dicionário de Dados – AIH | 02/05/2016 | [FTP DATASUS](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/dicionario_de_dados_AIH.pdf) | `f70974716de8` |
| Layout do arquivo reduzida (`Layout_REDUZIDA.pdf`) | | [FTP DATASUS](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/Layout_REDUZIDA.pdf) | `f6084d22de30` |
| Layout do SISAIH01 | competência set/2015 | [FTP DATASUS](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/Layout_do_SISAIH01_para_CMPT_201509.zip) | `af543b2b2c9b` |
| Pacote `TAB_SIH.zip` (DEF e CNV do TabWin) | 15/11/2026 | [FTP DATASUS](ftp://ftp.datasus.gov.br/dissemin/publicos/SIHSUS/200801_/Auxiliar/TAB_SIH.zip) | `21e42384645a` |

### Manual Técnico Operacional do SIH, todas as edições

No portal SIHD (FTP do DATASUS; navegadores atuais não abrem links FTP, ver abaixo).

| Edição | Arquivo |
| --- | --- |
| jan/2017 | [MANUAL_SIH_janeiro_2017.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_janeiro_2017.pdf) |
| jan/2015 | [MANUAL_SIH_janeiro_2015.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_janeiro_2015.pdf) |
| out/2013 | [MANUAL_SIH_outubro_2013.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_outubro_2013.pdf) |
| set/2013 | [MANUAL_SIH_setembro_2013_29_08_13.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_setembro_2013_29_08_13.pdf) |
| set/2012 | [MANUAL_SIH_SETEMBRO_2012_VERSAO_DIA_30_09_12.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_SETEMBRO_2012_VERSAO_DIA_30_09_12.pdf) |
| abr/2011 | [Manual_SIH_Abril_2011.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/Manual_SIH_Abril_2011.pdf) |
| set/2010 | [MANUAL_SIH_SETEMBRO_2010.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_SETEMBRO_2010.pdf) |
| mai/2010 | [MANUAL_SIH_MAIO_2010.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/MANUAL_SIH_MAIO_2010.pdf) |
| jun/2009 | [Manual_SIH_Junho_2009.pdf](ftp://ftp2.datasus.gov.br/public/sistemas/dsweb/SIHD/Manuais/Manual_SIH_Junho_2009.pdf) |

Para baixar no Windows, use o PowerShell: `curl.exe -O <link>`.

Também usados na revisão, ainda sem link registrado:

- DATASUS. *Informe Técnico SIH/SUS* 2012-03.
- Ministério da Saúde, DENASUS. *Auditoria no SUS: noções básicas sobre sistemas de informação*. 2004.

## Secundárias

- Cerqueira DRC et al. *Uma análise da base de dados do Sistema de Informação Hospitalar entre 2001 e 2018*. Rio de Janeiro: Ipea, 2019. [PDF](https://repositorio.ipea.gov.br/bitstream/11058/9409/1/Uma_analise_da_base_de_dados_do_sistema_de_informacao_hospitalar.pdf)
- Fiocruz/ICICT, PCDaS. [Documentação técnica do SIH](https://pcdas.icict.fiocruz.br/wp-content/uploads/2023/08/documentacao_SIH_2.html).
- Saldanha R. *Sistemas de Informação em Saúde no Brasil* (panorama dos sistemas).

## Dicionário

- [omnisus](https://github.com/raphaelfh/omnisus) (fork da revisão: [marcelaqs/omnisus](https://github.com/marcelaqs/omnisus)): dicionário do RD em `src/omnisus/data/dicionarios/sih_aih_reduzida.yaml` e registro de fontes em `sources/registry.json`.
