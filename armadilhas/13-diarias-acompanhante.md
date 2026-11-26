# 13. Diárias de acompanhante não mostram a presença do acompanhante

**Campo:** `DIAR_ACOM`

## O que acontece

`DIAR_ACOM` conta as diárias de acompanhante cobradas. A Portaria GM/MS nº 2.418/2005 regulamenta o acompanhante da mulher no trabalho de parto, parto e pós-parto imediato (Lei nº 11.108/2005) e autoriza a cobrança dessas diárias, mas a cobrança depende de formalização pelo gestor.

## Por que importa para predição

Um `DIAR_ACOM` igual a zero não mostra que a mulher ficou sem acompanhante. Usar o campo como indicador de direito garantido, ou como preditor de qualidade da assistência ao parto, mede a cobrança, e não a presença.

## Como lidar

- Não interpretar zero como ausência de acompanhante.
- Se usado, descrever o campo como "diárias de acompanhante cobradas".

## Fonte

Informe Técnico SIH 2016-03, p. 2; Portaria GM/MS nº 2.418/2005.
