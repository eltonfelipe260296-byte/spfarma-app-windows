# SPFARMA Flutuante — Windows 0.3.0

Aplicativo instalado para Windows x64, conectado por HTTPS ao sistema em https://spfarma-entregas.onrender.com. Requer internet e um acesso existente. Interface, permissões e dados são carregados do servidor; atualizações publicadas no Render aparecem no aplicativo ao reabri-lo. O instalador contém somente a janela do aplicativo, sem banco, senhas ou cópia offline do sistema.

## Download e instalação

Download público: https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest

Download direto, sem página intermediária: https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe

1. Baixe `SPFARMA-Flutuante-Instalador.exe` e execute o instalador em português. O pacote local de build inclui a versão no nome (`SPFARMA-Flutuante-Instalador-0.3.0.exe`).
2. A instalação cria **SPFARMA Flutuante** na área de trabalho e no Menu Iniciar.
3. Abra o atalho e entre com sua conta. Usuário, Caixa e administrador iniciam em Vendas.
4. Para fixar na barra de tarefas, abra o aplicativo, clique com o botão direito no ícone da barra e escolha **Fixar na barra de tarefas**. O instalador cria o atalho e a identidade necessários; a fixação é uma escolha feita no Windows.

O executável fica em uma pasta permanente do usuário, e o desinstalador aparece nos Aplicativos do Windows. Não é necessário instalar Node/Electron separadamente. O pacote 0.3.0 não possui assinatura digital; o arquivo `SHA256SUMS.txt` do download permite conferir a integridade. O repositório do sistema permanece privado; somente a distribuição deste aplicativo é pública.

## Operação

- **Vendas** abre a emissão em duas páginas. Na primeira, busque o cliente, escolha/confira o endereço e veja a taxa. **Seguir para o pagamento** abre a segunda, com valor da venda, pagamento, taxa/total e **Emitir venda**. **Voltar ao endereço** mantém os valores. Emissão bem-sucedida limpa e retorna à primeira etapa; falhas mantêm os campos para repetir.
- **Consulta** pesquisa endereço e taxa cadastrada por rua, bairro, cidade ou CEP, sem editar cadastros. Mostra dez resultados de cada vez, com Mostrar mais. Não precisa iniciar uma venda, e a troca de aba mantém o rascunho.
- **Caixa** abre pedidos, acompanhamento, impressão e conclusão por código para os perfis autorizados.
- **Menu** abre as demais funções do perfil, incluindo lançamento manual e cadastro de endereço para o administrador.
- **Iniciar com Windows** ativa/desativa o início automático ao entrar no Windows, para o usuário deste computador. Começa desligado; o botão marcado indica configuração ativada e a escolha permanece ao fechar/reabrir. Disponível no aplicativo instalado, inclusive antes do login no sistema; exige instalar a versão 0.2.1 ou posterior. Não faz login automático nem altera o prazo da sessão. Desinstalar remove a inicialização; atualizar mantém a escolha. No desenvolvimento/portátil, a opção fica desabilitada para não apontar para executável temporário.

- Arraste a barra vermelha para posicionar sobre seu sistema de vendas.
- Recolher reduz para uma barra. Nova entrega expande e mantém os campos sem recarregar.
- Fixar mantém a janela sobre outros programas; clique novamente para desativar.
- Auto recolhe após uma emissão bem-sucedida. Começa desativado.
- Sair encerra a conta; − minimiza; × fecha o aplicativo.

Expandido: 460 × até 800 px, redimensionável. Recolhido: 320 × 48 px. Sem preenchimento automático. Reutiliza o formulário publicado com ajustes visuais locais, sem mudanças no servidor. Conteúdo remoto sem Node, com isolamento/sandbox e navegação limitada ao site permitido.

Campos de emissão com 32 px, informações repetitivas ocultas e rua/número lado a lado. A taxa aparece nas duas etapas. Avisos de erro e instruções relevantes do pagamento permanecem. O rascunho continua sendo mantido, sem texto complementar na tela. Esta reorganização é local ao aplicativo Windows; instalar a versão 0.3.0 para recebê-la.

## Desenvolvimento

`npm ci --prefix desktop`, `npm start --prefix desktop`, `npm run build --prefix desktop` (instalador NSIS x64). Dependências/build separados do servidor. `npm run build:portable --prefix desktop` gera o portátil opcional, sem instalar atalhos.

Verificação com bancos/perfis temporários:

- `node verificacao/verify-desktop.cjs`: isolamento, formulário, recolhimento, fixação, emissão e saída.
- `node verificacao/verify-desktop-operations.cjs`: Usuário/Caixa, impressão/conclusão, rascunho, menu e novo endereço.
- `node verificacao/verify-desktop-online.cjs`: saúde e tela de login do servidor público, sem autenticar nem gravar dados reais.
- `node verificacao/verify-desktop-startup.cjs`: registro de início automático em namespace de teste, persistência ao reabrir, ativação/desativação e barra em quatro larguras. Usa binário empacotado, sem alterar a inicialização pessoal do usuário.
- `node verificacao/verify-desktop-flow.cjs`: duas etapas, cliente existente, validação, Consulta, taxa atualizada, preservação de valores e falha/repetição de emissão. As prévias visuais são renderizadas a partir do DOM e valores do teste, com CSS do aplicativo.
- `powershell -NoProfile -ExecutionPolicy Bypass -File verificacao/verify-desktop-installer.ps1`: instalação temporária, atalhos Desktop/Menu Iniciar e AppUserModelID, testes do executável instalado e desinstalação ao terminar. Interrompe se já houver instalação/atalhos, para preservá-los.

`SPFARMA_DESKTOP_EXECUTABLE` permite testar o binário empacotado. A identidade `com.spfarma.floating` é a mesma do aplicativo e dos atalhos NSIS; ícones em `assets/` derivados dos ícones existentes do sistema. O instalador não faz deploy do servidor nem estende permissões da conta. Impressão usa o diálogo e a impressora configurados no Windows.

Não incluir dependências baixadas, executáveis, perfil ou dados pessoais no Git. A sessão fica no perfil do aplicativo no Windows e segue o prazo do servidor. Recolher preserva a página; após fechar, o próximo acesso exige login se a sessão expirou.

Referências técnicas: [instalador NSIS](https://www.electron.build/nsis/), [integração da barra de tarefas](https://www.electronjs.org/docs/latest/tutorial/windows-taskbar).
