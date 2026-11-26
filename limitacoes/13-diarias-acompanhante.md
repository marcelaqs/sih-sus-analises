# 13. Diárias de acompanhante não mostram a presença do acompanhante

**Campo:** `DIAR_ACOM`

## O que acontece

`DIAR_ACOM` conta as diárias de acompanhante cobradas. A Portaria GM/MS nº 2.418/2005 regulamenta o acompanhante da mulher no trabalho de parto, parto e pós-parto imediato (Lei nº 11.108/2005) e autoriza a cobrança dessas diárias, mas a cobrança depende de formalização pelo gestor. Desde 2017, a regra está no art. 92 da Portaria de Consolidação GM/MS nº 3/2017, que hoje, com a Lei nº 14.737/2023 e a Portaria GM/MS nº 5.350/2024, estende o direito a acompanhante a admissão, internação, alta, consultas e exames.

A cobrança de diárias de acompanhante na AIH também vale para pacientes com mais de 60 anos internados (Portaria GM/MS nº 280/1999, hoje Anexo 2 do Anexo XI da Portaria de Consolidação GM/MS nº 2/2017). Um `DIAR_ACOM` maior que zero não indica parto.

## Por que importa na análise

Um `DIAR_ACOM` igual a zero não mostra que a mulher ficou sem acompanhante. Usar o campo como indicador de direito garantido, ou como preditor de qualidade da assistência ao parto, mede a cobrança, e não a presença.

## Como lidar

- Não interpretar zero como ausência de acompanhante.
- Se usado, descrever o campo como "diárias de acompanhante cobradas".

## Fonte

Portaria de Consolidação GM/MS nº 2/2017, Anexo 2 do Anexo XI; Informe Técnico SIH 2016-03, p. 2; Portaria GM/MS nº 2.418/2005; Portaria de Consolidação GM/MS nº 3/2017, art. 92.
