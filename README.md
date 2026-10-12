# SPFARMA Flutuante â€” Windows 0.4.0

Aplicativo instalado para Windows x64, conectado por HTTPS ao sistema em https://spfarma-entregas.onrender.com. Requer internet e um acesso existente. Interface, permissÃµes e dados sÃ£o carregados do servidor; atualizaÃ§Ãµes publicadas no Render aparecem no aplicativo ao reabri-lo. O instalador contÃ©m somente a janela do aplicativo, sem banco, senhas ou cÃ³pia offline do sistema.

## Download e instalaÃ§Ã£o

Download pÃºblico: https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest

Download direto, sem pÃ¡gina intermediÃ¡ria: https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe

1. Baixe `SPFARMA-Flutuante-Instalador.exe` e execute o instalador em portuguÃªs. O pacote local de build inclui a versÃ£o no nome (`SPFARMA-Flutuante-Instalador-0.4.0.exe`).
2. A instalaÃ§Ã£o cria **SPFARMA Flutuante** na Ã¡rea de trabalho e no Menu Iniciar.
3. Abra o atalho e entre com sua conta. UsuÃ¡rio, Caixa e administrador iniciam em Vendas.
4. Para fixar na barra de tarefas, abra o aplicativo, clique com o botÃ£o direito no Ã­cone da barra e escolha **Fixar na barra de tarefas**. O instalador cria o atalho e a identidade necessÃ¡rios; a fixaÃ§Ã£o Ã© uma escolha feita no Windows.

O executÃ¡vel fica em uma pasta permanente do usuÃ¡rio, e o desinstalador aparece nos Aplicativos do Windows. NÃ£o Ã© necessÃ¡rio instalar Node/Electron separadamente. O pacote 0.4.0 nÃ£o possui assinatura digital; o arquivo `SHA256SUMS.txt` do download permite conferir a integridade. O repositÃ³rio do sistema permanece privado; somente a distribuiÃ§Ã£o deste aplicativo Ã© pÃºblica.

## OperaÃ§Ã£o

- **Vendas** abre a emissÃ£o em duas pÃ¡ginas. Na primeira, busque o cliente, escolha/confira o endereÃ§o e veja a taxa. **Seguir para o pagamento** abre a segunda, com valor da venda, pagamento, taxa/total e **Emitir venda**. **Voltar ao endereÃ§o** mantÃ©m os valores. EmissÃ£o bem-sucedida limpa e retorna Ã  primeira etapa; falhas mantÃªm os campos para repetir.
- **Consulta** pesquisa endereÃ§o e taxa cadastrada por rua, bairro, cidade ou CEP, sem editar cadastros. Mostra dez resultados de cada vez, com Mostrar mais. NÃ£o precisa iniciar uma venda, e a troca de aba mantÃ©m o rascunho.
- **Caixa** abre pedidos, acompanhamento, impressÃ£o e conclusÃ£o por cÃ³digo para os perfis autorizados.
- **Menu** abre as demais funÃ§Ãµes do perfil, incluindo lanÃ§amento manual e cadastro de endereÃ§o para o administrador.
- **Iniciar com Windows** ativa/desativa o inÃ­cio automÃ¡tico ao entrar no Windows, para o usuÃ¡rio deste computador. ComeÃ§a desligado; o botÃ£o marcado indica configuraÃ§Ã£o ativada e a escolha permanece ao fechar/reabrir. DisponÃ­vel no aplicativo instalado, inclusive antes do login no sistema; exige instalar a versÃ£o 0.2.1 ou posterior. NÃ£o faz login automÃ¡tico nem altera o prazo da sessÃ£o. Desinstalar remove a inicializaÃ§Ã£o; atualizar mantÃ©m a escolha. No desenvolvimento/portÃ¡til, a opÃ§Ã£o fica desabilitada para nÃ£o apontar para executÃ¡vel temporÃ¡rio.

- Expandido: arraste a barra vermelha para posicionar sobre seu sistema de vendas.
- Recolher reduz para uma barra. Nova entrega expande e mantÃ©m os campos sem recarregar.
- Fixar mantÃ©m a janela sobre outros programas; clique novamente para desativar.
- Auto recolhe apÃ³s uma emissÃ£o bem-sucedida. ComeÃ§a desativado.
- Sair encerra a conta; âˆ’ minimiza; Ã— fecha o aplicativo.

Expandido: 460 Ã— atÃ© 800 px, redimensionÃ¡vel. Recolhido: 320 Ã— 48 px. Sem preenchimento automÃ¡tico. Reutiliza o formulÃ¡rio publicado com ajustes visuais locais, sem mudanÃ§as no servidor. ConteÃºdo remoto sem Node, com isolamento/sandbox e navegaÃ§Ã£o limitada ao site permitido.

Campos de emissÃ£o com 32 px, informaÃ§Ãµes repetitivas ocultas e rua/nÃºmero lado a lado. A taxa aparece nas duas etapas. Avisos de erro e instruÃ§Ãµes relevantes do pagamento permanecem. O rascunho continua sendo mantido, sem texto complementar na tela. Esta reorganizaÃ§Ã£o Ã© local ao aplicativo Windows; instalar a versÃ£o 0.4.0 para recebÃª-la.

## Atualiza??o autom?tica

Instale esta vers?o uma vez por cima da existente, sem desinstalar. A partir da 0.4.0, o aplicativo instalado consulta releases p?blicos ao abrir (ap?s 15 segundos) e a cada quatro horas, baixa vers?es est?veis em segundo plano e instala ao fechar normalmente. A pr?xima abertura usa a nova vers?o; vendas n?o s?o interrompidas. Sem internet, o app continua e tenta novamente mais tarde. Atalhos, perfil e Iniciar com Windows permanecem. Desenvolvimento, testes e port?til n?o executam o atualizador. A barra indica Atualiza??o pronta quando o download termina.

Publica??o de pr?ximas vers?es: gerar o instalador NSIS e publicar, no mesmo release p?blico, o instalador, seu .blockmap e latest.yml gerados pelo builder; o nome indicado no YAML deve corresponder ao asset. O SHA-512 dos metadados ? verificado pelo atualizador. N?o colocar credenciais no pacote.

## Desenvolvimento

`npm ci --prefix desktop`, `npm start --prefix desktop`, `npm run build --prefix desktop` (instalador NSIS x64). DependÃªncias/build separados do servidor. `npm run build:portable --prefix desktop` gera o portÃ¡til opcional, sem instalar atalhos.

VerificaÃ§Ã£o com bancos/perfis temporÃ¡rios:

- `node verificacao/verify-desktop-updates.cjs`: download real do instalador por Electron, SHA-512, rejei??o de arquivo corrompido e pol?tica de atualiza??o sem rein?cio durante opera??o.
- `node verificacao/verify-desktop.cjs`: isolamento, formulÃ¡rio, recolhimento, fixaÃ§Ã£o, emissÃ£o e saÃ­da.
- `node verificacao/verify-desktop-operations.cjs`: UsuÃ¡rio/Caixa, impressÃ£o/conclusÃ£o, rascunho, menu e novo endereÃ§o.
- `node verificacao/verify-desktop-online.cjs`: saÃºde e tela de login do servidor pÃºblico, sem autenticar nem gravar dados reais.
- `node verificacao/verify-desktop-startup.cjs`: registro de inÃ­cio automÃ¡tico em namespace de teste, persistÃªncia ao reabrir, ativaÃ§Ã£o/desativaÃ§Ã£o e barra em quatro larguras. Usa binÃ¡rio empacotado, sem alterar a inicializaÃ§Ã£o pessoal do usuÃ¡rio.
- `node verificacao/verify-desktop-flow.cjs`: duas etapas, cliente existente, validaÃ§Ã£o, Consulta, taxa atualizada, preservaÃ§Ã£o de valores e falha/repetiÃ§Ã£o de emissÃ£o. As prÃ©vias visuais sÃ£o renderizadas a partir do DOM e valores do teste, com CSS do aplicativo.
- `powershell -NoProfile -ExecutionPolicy Bypass -File verificacao/verify-desktop-installer.ps1`: instalaÃ§Ã£o temporÃ¡ria, atalhos Desktop/Menu Iniciar e AppUserModelID, testes do executÃ¡vel instalado e desinstalaÃ§Ã£o ao terminar. Interrompe se jÃ¡ houver instalaÃ§Ã£o/atalhos, para preservÃ¡-los.

`SPFARMA_DESKTOP_EXECUTABLE` permite testar o binÃ¡rio empacotado. A identidade `com.spfarma.floating` Ã© a mesma do aplicativo e dos atalhos NSIS; Ã­cones em `assets/` derivados dos Ã­cones existentes do sistema. O instalador nÃ£o faz deploy do servidor nem estende permissÃµes da conta. ImpressÃ£o usa o diÃ¡logo e a impressora configurados no Windows.

NÃ£o incluir dependÃªncias baixadas, executÃ¡veis, perfil ou dados pessoais no Git. A sessÃ£o fica no perfil do aplicativo no Windows e segue o prazo do servidor. Recolher preserva a pÃ¡gina; apÃ³s fechar, o prÃ³ximo acesso exige login se a sessÃ£o expirou.

ReferÃªncias tÃ©cnicas: [instalador NSIS](https://www.electron.build/nsis/), [integraÃ§Ã£o da barra de tarefas](https://www.electronjs.org/docs/latest/tutorial/windows-taskbar).
