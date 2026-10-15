# SPFARMA Flutuante — Windows 0.8.0

[Baixar instalador para Windows x64](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe)

Execute o instalador por cima da versão existente, sem desinstalar. Atalhos, configuração da impressora, identidade do terminal e perfil são preservados. O aplicativo usa o sistema online por HTTPS e exige internet.

## Login e conexão

No Windows, o login permanece salvo ao fechar e reabrir. No celular, deixe Manter conectado marcado. A sessão persistente não vence por inatividade no servidor; o cookie dura 400 dias e se renova diariamente durante o uso. Sair, revogar acesso, mudar senha ou limpar os dados locais exige novo login. Sessões já expiradas antes desta atualização precisam entrar novamente uma vez.

Ao voltar ao primeiro plano ou recuperar internet, o sistema verifica a sessão e recupera os dados sem limpar os campos. O sistema operacional pode suspender o navegador em segundo plano. A política de login exige que o administrador publique também o código atualizado no servidor existente, preservando banco, disco e variáveis.

## Atualização automática

A versão 0.8.0 verifica atualizações em cada abertura antes de carregar Vendas. Havendo nova versão, baixa, confere a integridade, instala silenciosamente e reabre. Falhas liberam o uso e serão tentadas novamente. Durante o uso, não reinicia uma venda ativa: aplica na próxima abertura, no fechamento normal ou na tela de login livre. Consulta também a cada cinco minutos. Diagnóstico em updates.log no perfil do aplicativo.

Versões 0.4.0 a 0.7.0 ainda baixam e aguardam fechamento normal para instalar. Para receber a nova política, feche normalmente e reabra depois do download, ou execute este instalador uma vez por cima. Desenvolvimento e versão portátil não executam o atualizador.

## Impressão entre aplicativos

Cada instalação possui identidade própria. Em Impressora, registre os aplicativos; o administrador cria o grupo e autoriza emissores/receptor. No receptor, ative Receber impressões e selecione sua impressora local; nos emissores, escolha esse aplicativo receptor do mesmo grupo. A comunicação ocorre pelo servidor online, sem compartilhamento de impressoras do Windows.

Ao emitir, são enfileirados um cupom principal e uma comanda do cliente. O receptor precisa estar aberto e conectado, podendo estar recolhido ou na tela de login. Se estiver offline, os trabalhos aguardam a reconexão. Esta versão mantém o layout de cupom e até dois pagamentos da 0.7.0.

O instalador não contém banco comercial ou credenciais. SHA256SUMS.txt permite conferir os arquivos; latest.yml e blockmap são usados pelo atualizador.
