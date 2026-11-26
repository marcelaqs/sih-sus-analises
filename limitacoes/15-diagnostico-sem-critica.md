# 15. Diagnóstico sem crítica de compatibilidade com o procedimento

**Campos:** `DIAG_PRINC`, `DIAGSEC1` em diante, `PROC_REA`

## O que acontece

Desde jan/2015, o sistema deixou de criticar a compatibilidade entre o procedimento realizado e os diagnósticos registrados na AIH (Portaria SAS/MS nº 1.324/2014, art. 4º). A mesma portaria passou a definir o diagnóstico principal como o motivo principal da internação, estabelecido após estudo, que pode ser diferente do diagnóstico de admissão.

## Por que importa para predição

- A relação entre diagnóstico e procedimento pode mudar de padrão em 2015, por mudança de regra e não de perfil das internações.
- Um modelo que usa diagnóstico e procedimento juntos, treinado com dados de antes e depois de 2015, mistura dois regimes de registro.
- O diagnóstico principal reflete toda a internação, não só a admissão. Para predizer na admissão, ele pode carregar informação do desfecho (vazamento).

## Como lidar

- Comparar a distribuição dos pares diagnóstico–procedimento antes e depois de jan/2015.
- Em modelos de predição na admissão, discutir se o diagnóstico principal está disponível no momento da predição.

## Fonte

Portaria SAS/MS nº 1.324/2014, arts. 2º e 4º (ver [`../normas/`](../normas/)).
