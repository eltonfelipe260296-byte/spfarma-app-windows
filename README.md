# SPFARMA Flutuante — Windows 0.10.0

[Baixar instalador Windows x64](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe)

## Novidade

Tela de carregamento animada SPFARMA na abertura do aplicativo e durante a preparação da interface. A animação respeita a opção de movimento reduzido do sistema. Atualizações mostram o andamento na mesma tela; erros continuam oferecendo tentar novamente. Os controles de fechar/minimizar permanecem acessíveis.

## Instalação e atualização

Execute o instalador por cima da versão atual, sem desinstalar. Perfil, impressoras, terminal e início automático são preservados. A partir da 0.8.0, o app verifica novas versões em cada abertura, instala silenciosamente e reabre antes de iniciar Vendas. Durante o uso, não reinicia uma venda ativa: espera próxima abertura, fechamento normal ou login livre. Sem internet, permite continuar e tenta novamente.

Apps 0.4.0 a 0.7.0 ainda seguem o ciclo anterior de baixar e instalar ao fechar normalmente; precisam concluir esse ciclo ou executar o instalador novo uma vez. O portátil e o desenvolvimento não usam o atualizador.

## Configurações e impressão

Iniciar com Windows e Impressoras ficam em Menu → Configurações → Aplicativo Windows. A interface do servidor também precisa estar atualizada. Para imprimir entre aplicativos, registre os terminais, crie/autorize grupo no acesso admin e selecione o receptor. Só o receptor configura a impressora local; não usa compartilhamento de impressoras do Windows. Receptor precisa estar aberto/conectado, podendo estar recolhido ou no login. São enviados um cupom e uma comanda por venda; atualizar emissores/receptores mantém o layout térmico.

Caixa mantém Hoje/Ontem e prévias compactas. Regras de seleção, pausa, limite, exigência de impressão, prazo e remuneração são administradas no servidor. Login permanece salvo; Sair, revogar acesso, alterar senha ou limpar dados pode exigir entrar novamente. O app usa HTTPS e exige internet; não contém banco comercial ou credenciais de acesso no instalador.

## Integridade e ativação

latest.yml, blockmap e SHA256SUMS.txt acompanham o pacote. O atualizador verifica SHA-512. A animação do site/interface é ativada pelo deploy do código no Render, preservando disco/banco/variáveis existentes. Esta publicação não executa deploy nem instala permanentemente no computador do usuário.
