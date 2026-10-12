# SPFARMA Flutuante — Windows 0.2.0

Aplicativo instalado para Windows x64, conectado por HTTPS ao sistema em https://spfarma-entregas.onrender.com. Requer internet e um acesso existente. Interface, permissões e dados são carregados do servidor; atualizações publicadas no Render aparecem no aplicativo ao reabri-lo. O instalador contém somente a janela do aplicativo, sem banco, senhas ou cópia offline do sistema.

## Download e instalação

Download público: https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest

1. Baixe `SPFARMA-Flutuante-Instalador-0.2.0.exe` e execute o instalador em português.
2. A instalação cria **SPFARMA Flutuante** na área de trabalho e no Menu Iniciar.
3. Abra o atalho e entre com sua conta. Usuário, Caixa e administrador iniciam em Vendas.
4. Para fixar na barra de tarefas, abra o aplicativo, clique com o botão direito no ícone da barra e escolha **Fixar na barra de tarefas**. O instalador cria o atalho e a identidade necessários; a fixação é uma escolha feita no Windows.

O executável fica em uma pasta permanente do usuário, e o desinstalador aparece nos Aplicativos do Windows. Não é necessário instalar Node/Electron separadamente. O pacote 0.2.0 não possui assinatura digital; o arquivo `SHA256SUMS.txt` do download permite conferir a integridade. O repositório do sistema permanece privado; somente a distribuição deste aplicativo é pública.

## Operação

- **Vendas** abre a emissão; **Caixa** abre pedidos, consulta, acompanhamento, impressão e conclusão por código para os perfis autorizados.
- **Menu** abre as demais funções do perfil, incluindo lançamento manual e cadastro de endereço para o administrador.

- Arraste a barra vermelha para posicionar sobre seu sistema de vendas.
- Recolher reduz para uma barra. Nova entrega expande e mantém os campos sem recarregar.
- Fixar mantém a janela sobre outros programas; clique novamente para desativar.
- Auto recolhe após uma emissão bem-sucedida. Começa desativado.
- Sair encerra a conta; − minimiza; × fecha o aplicativo.

Expandido: 460 × até 800 px, redimensionável. Recolhido: 320 × 48 px. Sem preenchimento automático. Reutiliza o formulário publicado com ajustes visuais locais, sem mudanças no servidor. Conteúdo remoto sem Node, com isolamento/sandbox e navegação limitada ao site permitido.

## Desenvolvimento

`npm ci --prefix desktop`, `npm start --prefix desktop`, `npm run build --prefix desktop` (instalador NSIS x64). Dependências/build separados do servidor. `npm run build:portable --prefix desktop` gera o portátil opcional, sem instalar atalhos.

Verificação com bancos/perfis temporários:

- `node verificacao/verify-desktop.cjs`: isolamento, formulário, recolhimento, fixação, emissão e saída.
- `node verificacao/verify-desktop-operations.cjs`: Usuário/Caixa, impressão/conclusão, rascunho, menu e novo endereço.
- `node verificacao/verify-desktop-online.cjs`: saúde e tela de login do servidor público, sem autenticar nem gravar dados reais.
- `powershell -NoProfile -ExecutionPolicy Bypass -File verificacao/verify-desktop-installer.ps1`: instalação temporária, atalhos Desktop/Menu Iniciar e AppUserModelID, testes do executável instalado e desinstalação ao terminar. Interrompe se já houver instalação/atalhos, para preservá-los.

`SPFARMA_DESKTOP_EXECUTABLE` permite testar o binário empacotado. A identidade `com.spfarma.floating` é a mesma do aplicativo e dos atalhos NSIS; ícones em `assets/` derivados dos ícones existentes do sistema. O instalador não faz deploy do servidor nem estende permissões da conta. Impressão usa o diálogo e a impressora configurados no Windows.

Não incluir dependências baixadas, executáveis, perfil ou dados pessoais no Git. A sessão fica no perfil do aplicativo no Windows e segue o prazo do servidor. Recolher preserva a página; após fechar, o próximo acesso exige login se a sessão expirou.

Referências técnicas: [instalador NSIS](https://www.electron.build/nsis/), [integração da barra de tarefas](https://www.electronjs.org/docs/latest/tutorial/windows-taskbar).
