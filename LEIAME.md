# Adequação Sanitária Fortal — app de acompanhamento

Checklist do Relatório de Inspeção da Revisa (06/11/2026, prazo 09/12/2026).
Qualquer pessoa com o link ou o QR code abre, digita o nome e registra.
Cada marcação grava quem fez e a data/hora, com histórico.

## 1. Firebase (banco de dados) — ~10 min
1. Acesse console.firebase.google.com > **Adicionar projeto** (ex.: `fortal-revisa`). Pode desativar o Google Analytics.
2. Menu **Criação > Firestore Database > Criar banco de dados**. Local: `southamerica-east1 (São Paulo)`. Modo: **produção**.
3. Na aba **Regras**, apague tudo, cole o conteúdo do arquivo `firestore.rules` e clique em **Publicar**.
4. Engrenagem > **Configurações do projeto** > em "Seus apps" clique no ícone **</>** (Web) > dê um nome > **Registrar app**.
5. Copie os valores de `firebaseConfig` e cole no arquivo `firebase-config.js` no lugar de cada `COLE_AQUI`.

> A apiKey do Firebase pode ficar pública: quem protege os dados são as regras do passo 3.

## 2. GitHub Pages (hospedagem) — ~5 min
1. Em github.com > **New repository** > nome `fortal-revisa` > **Public** > Create.
2. **Add file > Upload files** > arraste todos os arquivos desta pasta > **Commit changes**.
3. **Settings > Pages** > Source: **Deploy from a branch** > Branch: `main` / `(root)` > Save.
4. Em 1–2 minutos o app fica em: `https://SEU-USUARIO.github.io/fortal-revisa/`

## 3. QR code
Gere o QR com o endereço do passo 2.4 e imprima.
No celular, a pessoa pode usar "Adicionar à tela de início" para abrir como aplicativo.

## Observações
- Ninguém consegue apagar registros; só mudar o status, sempre com o nome gravado no histórico.
- O nome é digitado pela pessoa (não há senha). Para controle mais rígido, dá para adicionar login depois.
