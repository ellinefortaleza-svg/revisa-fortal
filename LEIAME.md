# Controle Sanitário Fortal

App da nutricionista RT e da equipe: temperaturas, amostras, higienização, recebimento,
checagem da equipe, treinamentos, ocorrências, itens do relatório da Revisa (06/11/2026),
prazos e controles (dedetização, filtro, caixa d'água, laudos, alvará) e relatório em PDF.

- Endereço: https://ellinefortaleza-svg.github.io/revisa-fortal/
- Dados: Firebase (projeto vigilanciafortal). As regras ficam em `firestore.rules`:
  cole no Console do Firebase > Firestore Database > Regras > Publicar sempre que este arquivo mudar.
- Cada registro grava quem registrou (nome digitado no topo) e data/hora. Nada pode ser apagado.
