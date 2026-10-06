# Relatório de Entrada — publicar no GitHub Pages

O site é um único arquivo (`index.html`). Para todos verem **ao vivo** as mesmas marcações, fotos e planilha, ele usa o Firebase Firestore (gratuito para esse uso).

## 1) Firebase (5 min)
1. Acesse https://console.firebase.google.com e abra o projeto (pode ser o `demandas-menores` ou um novo).
2. **Build > Firestore Database > Criar banco de dados** (se ainda não existir).
3. **Configurações do projeto (engrenagem) > Seus apps > ícone `</>` (Web)**: registre o app e copie o `firebaseConfig`.
4. Abra o `index.html` num editor, ache o bloco `FIREBASE_CONFIG` no começo do script e cole seus valores (`apiKey`, `authDomain`, `projectId`, `storageBucket`, `messagingSenderId`, `appId`).
5. **Firestore > Regras**: apague o conteúdo, cole o arquivo `firestore.rules` e clique em **Publicar**.

## 2) GitHub Pages
1. No GitHub, abra o repositório (ou crie um novo).
   - Se for o mesmo do Demandas Express, coloque este arquivo numa pasta própria (ex.: `relatorio-de-entrada/index.html`) para não sobrescrever o outro `index.html`.
2. **Add file > Upload files** e envie o `index.html` configurado. Faça o commit.
3. **Settings > Pages > Source: Deploy from a branch > main / (root) > Save**.
4. Em 1–2 minutos o link aparece, no formato `https://SEU-USUARIO.github.io/NOME-DO-REPO/` (ou `.../relatorio-de-entrada/`).

## Como usar
- Quem abrir o link vê tudo em tempo real: planilha, itens abastecidos e fotos.
- Para trocar o relatório do dia, arraste o novo `.xlsx` para a página. Ele vale para todos, e as marcações de abastecido recomeçam. As fotos ficam, pois são ligadas ao código do produto.
- Sem a configuração do Firebase, a página funciona em "Modo local" (só no navegador de quem abriu).

## Atenção
Como a equipe não faz login, qualquer pessoa com o link consegue marcar itens, enviar fotos e trocar a planilha. As regras acima só limitam o tamanho dos dados e as coleções usadas. Se quiser restringir depois, dá para adicionar login (Firebase Authentication).
