# Roteiro de Viagem — São Paulo + Rio de Janeiro 2026

App de roteiro no formato de site, feito para funcionar como um aplicativo (pode ser
"instalado" na tela inicial do celular), com o roteiro completo de 15 a 27/09.

## O que tem no app

- **Roteiro dia a dia**, com os dias em abas roláveis e cada atividade em ordem de horário.
- **Filtro por casal** (Ambos / Will & Vick / João & Wivi) no topo — atividades que só valem
  para um casal ficam marcadas com uma etiqueta colorida; o resto aparece para os dois.
- **Criar, editar e excluir** qualquer atividade (horário, ícone, título, local, notas e
  para quem é), direto pelo celular, tocando no botão laranja "+" ou no lápis ✏️.
- Toque no **📍 local** de uma atividade para abrir direto no Google Maps.
- Marque atividades como **feitas** tocando no círculo ao lado do horário.
- **Extras**: checklist de bagagem, controle de gastos (com quem gastou) e um bloco de
  notas com hospedagens, voos e informações do carro.
- **Contador de dias** para a viagem no topo da tela.
- **Backup**: em Ajustes → Exportar/Importar — como os dados ficam salvos só no navegador
  de cada celular, exporte um `.json` depois de editar e mande para o outro casal importar,
  se quiserem manter tudo sincronizado.
- Funciona **offline** depois do primeiro acesso (dá para consultar o roteiro sem internet).

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser privado ou público).
2. Envie os arquivos desta pasta (`index.html`, `manifest.json`, `sw.js`, `icon.svg`)
   para a raiz do repositório.
3. No repositório, vá em **Settings → Pages**.
4. Em "Source", selecione a branch `main` e a pasta `/ (root)`, depois clique em **Save**.
5. Em alguns minutos o GitHub mostra o link do site, algo como:
   `https://seu-usuario.github.io/nome-do-repositorio/`
6. Abra esse link no celular de cada casal e, no menu do navegador, escolha
   **"Adicionar à tela inicial"** — o roteiro passa a abrir como um app, com ícone próprio.

## Editar o roteiro por fora do app (opcional)

Todo o roteiro inicial está dentro de `index.html`, dentro da função `buildDefaultData()`.
Se preferir alterar o roteiro "de fábrica" direto no código (em vez de editar pelo app),
é só mexer nessa função antes de publicar. Depois que o app já estiver em uso, qualquer
edição feita pelo código só afeta quem tocar em "Restaurar roteiro original" em Ajustes —
o dia a dia normal é editado direto pela interface.
