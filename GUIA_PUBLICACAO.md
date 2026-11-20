# Escala do Som — CCB Osasco Centro | versão 3.1

## Arquitetura

- **Sem banco de dados**: `escala.json` é a fonte oficial compartilhada.
- **Hospedagem estática**: arquivos `index.html`, `escala.json`, `manifest.webmanifest`, `sw.js` e ícones no mesmo site HTTPS.
- **Responsável**: organiza a escala em seu navegador, exporta uma nova carga e substitui `escala.json` no repositório/hospedagem.
- **Irmãos**: acessam a página e tocam em **Atualizar escala** para ler o JSON mais recente. O aplicativo mantém uma cópia local para consulta offline.
- **Trocas**: solicitação encaminhada pelo WhatsApp. A alteração oficial só aparece nos demais aparelhos depois que o responsável publica nova carga.

## Como publicar no GitHub Pages

1. Crie um repositório no GitHub (exemplo: `escala-som-osasco`). **Atenção: o arquivo e os nomes ficarão acessíveis publicamente**.
2. Envie os arquivos da pasta do aplicativo para a raiz do repositório, incluindo `.nojekyll`.
3. Em **Settings > Pages**, selecione **Deploy from a branch**, branch `main`, pasta `/ (root)` e salve.
4. O endereço do aplicativo será semelhante a `https://USUARIO.github.io/escala-som-osasco/`.
5. Nesse mesmo endereço, `escala.json` estará disponível em `https://USUARIO.github.io/escala-som-osasco/escala.json`.
6. Por padrão, a versão 3.1 usa automaticamente esse endereço quando o aplicativo é aberto em HTTPS. Você ainda pode alterar o endereço na aba de backup/atualização.
7. O responsável edita e clica em **Gerar escala oficial**, baixando `escala.json`; em seguida substitui o arquivo de mesmo nome no repositório e confirma a alteração. Depois da publicação, todos podem tocar em **Atualizar escala**.

## Primeira operação

- A escala inicial está vazia, sem nomes reais.
- Abra o aplicativo e cadastre os irmãos e atendimentos no perfil responsável.
- Gere o primeiro `escala.json` e publique-o.
- Compartilhe somente o link do aplicativo com os irmãos.
- No celular, use **Adicionar à tela inicial** para abrir como aplicativo, quando disponível no navegador.

## Restrições importantes

- **Não há autenticação real**: o seletor de perfis é uma interface local, não impede que alguém altere dados armazenados no próprio aparelho. Só quem tiver permissão de edição no repositório pode alterar o arquivo oficial. Proteja essa permissão.
- **Não há sincronização de pedidos de troca**: comunicar pelo WhatsApp é parte obrigatória do fluxo.
- **Sem atualização automática em segundo plano**: o botão busca a carga nova, quando há internet; sem conexão usa os dados locais já carregados.
- **Privacidade**: num GitHub Pages público, nomes e datas serão públicos. Use apenas nomes autorizados, ou avalie uma hospedagem com controle de acesso caso necessário.
- **Backup**: os dados que o responsável edita ficam no navegador dele até a publicação. Baixe backups regularmente, pois limpar os dados do site pode removê-los.
- **OneDrive**: pode guardar backups. Link de compartilhamento nem sempre é uma URL de JSON diretamente legível pelo navegador. Para este fluxo, hospedar app e JSON juntos no mesmo site é mais confiável.
