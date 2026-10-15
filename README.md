# SPFARMA Flutuante — Windows 0.9.0

[Baixar instalador para Windows x64](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe)

Execute o instalador por cima da versão existente, sem desinstalar. Atalhos, configuração da impressora, identidade do terminal e perfil são preservados. O aplicativo usa o sistema online por HTTPS e exige internet.

## Novidades da versão 0.9.0

Iniciar com Windows e Impressoras ficam em Menu → Configurações → Aplicativo Windows. O servidor/interface também precisa ser atualizado para mostrar esse menu no novo app. Configurações de impressão, identidade do terminal e início automático são preservadas.

Caixa abre em Hoje, oferece Ontem e filtros por seleção sem botões-filtro. Prévias compactas mantêm cliente, código e total na primeira linha; nomes longos ficam com reticências. Comanda traz data junto de Entrega prevista, endereço sem cidade, total alinhado, valor a cobrar antes de cada parcela e QR/código com espaçamento mínimo. Pix, iFood e pagamentos prévios não entram no valor a cobrar. Atualize emissores e receptores para usar o novo cupom.

Admin → Regras de entrega permite selecionar por prazo, por emissão ou livremente, pausar novas reservas e exigir comanda impressa antes de reservar. Não cancela reservas/retiradas existentes. Prazo, limite e remuneração continuam configuráveis. Administrador também pode enviar som MP3/WAV até 2 MB e 20 segundos para avisos dentro do app. O som do vídeo solicitado ainda depende de arquivo fornecido pelo usuário; o sino padrão é mantido enquanto não configurado. Com o app fechado, Web Push continua usando o som definido pelo celular; não garante áudio personalizado.

## Login e conexão

No Windows, o login permanece salvo ao fechar e reabrir. No celular, deixe Manter conectado marcado. A sessão persistente não vence por inatividade no servidor; o cookie dura 400 dias e se renova diariamente durante o uso. Sair, revogar acesso, mudar senha ou limpar os dados locais exige novo login. Sessões já expiradas antes desta atualização precisam entrar novamente uma vez.

Ao voltar ao primeiro plano ou recuperar internet, o sistema verifica a sessão e recupera os dados sem limpar os campos. O sistema operacional pode suspender o navegador em segundo plano. A política de login exige que o administrador publique também o código atualizado no servidor existente, preservando banco, disco e variáveis.

## Atualização automática

A versão 0.9.0 verifica atualizações em cada abertura antes de carregar Vendas. Havendo nova versão, baixa, confere a integridade, instala silenciosamente e reabre. Falhas liberam o uso e serão tentadas novamente. Durante o uso, não reinicia uma venda ativa: aplica na próxima abertura, no fechamento normal ou na tela de login livre. Consulta também a cada cinco minutos. Diagnóstico em updates.log no perfil do aplicativo.

Versões 0.4.0 a 0.7.0 ainda baixam e aguardam fechamento normal para instalar. Para receber a nova política, feche normalmente e reabra depois do download, ou execute este instalador uma vez por cima. Desenvolvimento e versão portátil não executam o atualizador.

## Impressão entre aplicativos

Cada instalação possui identidade própria. Em Menu → Configurações → Aplicativo Windows → Impressoras, registre os aplicativos; o administrador cria o grupo e autoriza emissores/receptor. No receptor, ative Receber impressões e selecione sua impressora local; nos emissores, escolha esse aplicativo receptor do mesmo grupo. A comunicação ocorre pelo servidor online, sem compartilhamento de impressoras do Windows.

Ao emitir, são enfileirados um cupom principal e uma comanda do cliente. O receptor precisa estar aberto e conectado, podendo estar recolhido ou na tela de login. Se estiver offline, os trabalhos aguardam a reconexão. Esta versão mantém o layout de cupom e até dois pagamentos da 0.7.0.

O instalador não contém banco comercial ou credenciais. SHA256SUMS.txt permite conferir os arquivos; latest.yml e blockmap são usados pelo atualizador.

## Android — APK teste 0.1.1

[Baixar APK teste (Android 8+)](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/download/android-v0.1.1-test/SPFARMA-Entregas-0.1.1-teste.apk)

Versão em validação. Notificações com app fechado ainda aguardam Firebase; não houve teste físico antes da publicação. Veja o guia no [pré-lançamento Android](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/tag/android-v0.1.1-test). O aplicativo e o atualizador Windows permanecem na versão estável 0.9.0.
