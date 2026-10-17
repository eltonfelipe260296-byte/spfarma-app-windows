# SPFARMA — Aplicativos para Windows e Android

## Windows 0.16.0

[Baixar instalador Windows x64](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe)

Instale por cima da versão atual, sem desinstalar. Conclua ou feche as vendas abertas antes de atualizar. Perfil, login, impressoras, terminais e início com Windows são preservados. O aplicativo instalado também encontra esta versão pelo atualizador automático.

## Minimizar, restaurar e fechar

A engrenagem oferece **Minimizar** e **Fechar**, mesmo sem uma janela ativa. Minimizar recolhe todo o SPFARMA; ao voltar pelo ícone da barra de tarefas, aparece somente a barra inferior. As vendas continuam guardadas e podem ser recuperadas pela engrenagem. Fechar pede confirmação para descartar vendas com dados e aguarda emissões em andamento. Os comandos no título de cada janela afetam somente aquela janela.

A ativação pela barra de tarefas foi corrigida para evitar tela branca. Somente a barra principal cria uma entrada na barra de tarefas. Avisos de impressão pendente não reabrem janelas enquanto o aplicativo está minimizado; confira o Caixa ao voltar.

## Barra proporcional em monitores menores

A barra ocupa no máximo 25% da largura útil, limitada a 400 px. Em escala de 100%: 1024×768 → 256×31; 1280×720 → 320×38; 1366×768 → 341×41. Janelas mantêm 80% da largura da barra, com altura, título e conteúdo reduzidos proporcionalmente. Consulta/Caixa continuam acima da barra, encostados; a Venda acompanha o conteúdo. Monitores maiores mantêm o limite de 400×48. A escala da tela não muda o tamanho das comandas impressas.

## Atalhos do teclado

Abra **Engrenagem → Configurações → Atalhos do teclado**. Defina até duas teclas para **+Venda**, **Consulta** e **Caixa**, como `Alt + D`, `Ctrl + Q` ou uma tecla F1–F24. Deixe vazio e salve para desativar. Os campos começam vazios; exemplos não são atalhos padrão.

Os atalhos funcionam com outro programa em foco e com o SPFARMA minimizado, respeitando login/permissões. São salvos neste computador. Combinações duplicadas, de três teclas, incompletas e Alt+F4 são rejeitadas. Se uma combinação estiver em uso no Windows, escolha outra; os atalhos anteriores permanecem ativos quando a alteração falha.

## Endereço em Vendas

Sugestões e seleção mostram **Rua - Bairro**. A busca ocupa toda a linha; Número e Complemento ficam juntos abaixo. Pesquisa por rua, bairro, cidade ou CEP continua funcionando, mantendo os dados completos, taxa e número S/N. O mesmo ajuste está disponível na web e no Android 0.1.11.

Troco obrigatório em dinheiro continua: informe 0 quando não houver troco. Demais pagamentos, impressão e regras de entrega preservados.

## Verificações

56 testes automatizados e sintaxe aprovados; fonte e executável conferidos em seis resoluções, com ciclos nativos de minimizar/restaurar, atalhos globais, vendas independentes, falhas de emissão/impressão, Caixa, hierarquia, impressão entre dois aplicativos e início automático. Instalador, blockmap e latest.yml publicados juntos; atualizador confere SHA-512. SHA256SUMS.txt permite conferir os downloads. Reteste no terminal do usuário, papel/corte físico e aparelho Android continuam pendentes.

## Android 0.1.11 — Canal de teste

[Baixar APK Android](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/download/android-v0.1.11-test/SPFARMA-Entregas-0.1.11-teste.apk)

Android 8 ou superior. Pacote com.spfarma.entregas, versionCode 12, assinatura original preservada.

Em Vendas, sugestões e seleção de endereço mostram **Rua - Bairro**, sem cidade ou CEP na opção. A busca ocupa toda a linha; **Número e Complemento ficam lado a lado abaixo**. Pesquisa por rua, bairro, cidade e CEP continua funcionando. Dados completos do endereço, taxa, S/N, complemento, rascunho e comandas são preservados.

Instale por cima da versão atual, sem desinstalar. Use **Configurações → Aplicativo Android → Verificar atualizações**, ou baixe este APK. Confirme a instalação quando o Android solicitar. Atualizar o site não substitui as telas do APK instalado.

Pagamentos e troco obrigatório em dinheiro (0 significa sem troco), câmera por permissão nativa, notificações Firebase e atualizador anterior preservados.

Verificações de interface em 320/390/768/1366 px, seleção por teclado e preservação de Número/Complemento entre telas aprovadas, com runtime Capacitor real e serviços Android simulados. Assinatura, versão, recursos Firebase e fontes do APK conferidos, sem credenciais privadas. Teste em aparelho físico e confirmação real no iFood permanecem pendentes. Pré-lançamento Android separado do latest Windows 0.16.0.
