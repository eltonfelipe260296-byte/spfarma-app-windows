# SPFARMA Flutuante — Windows 0.13.0

[Baixar instalador Windows x64](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe)

## Instalação e atualização

Instale por cima da versão atual, sem desinstalar. Perfil, login, impressoras, terminais e início com Windows são preservados. Feche ou conclua as vendas abertas antes de atualizar.

O aplicativo instalado verifica atualizações ao abrir. Quando houver atualização durante o uso, aguarda um momento seguro ou o fechamento normal para instalar. O download direto do instalador permanece o mesmo.

## Barra inferior

A barra fica visível no canto inferior direito com **+Venda**, **Consulta** e **Caixa**. A engrenagem permanece sempre visível e oferece opções mesmo sem atendimentos abertos. O símbolo original da tela de carregamento aparece à esquerda de +Venda, sem animação. Auto e Fixar foram removidos: todas as janelas ficam sempre à frente.

## Vendas independentes

Cada clique em **+Venda** abre uma venda nova, arrastável, com 320 px de largura e altura ajustada ao conteúdo da etapa. A dica inicial do telefone foi removida. Mensagens de busca e erros continuam disponíveis. Em telas pequenas ou com campos adicionais, há rolagem vertical quando o conteúdo excede o monitor. Cada janela mantém seus próprios dados, inclusive quando minimizada. Uma janela não altera a outra.

Emissão bem-sucedida fecha somente a janela daquela venda, após o envio dos documentos para a fila. Falha na emissão mantém a janela e os dados. Se somente a impressão falhar depois de salvar a venda, o Caixa apresenta o aviso de impressão pendente; não emita a venda novamente.

## Consulta e Caixa

Compartilham a mesma janela fixa no lado direito, encostada acima da barra inferior, sem espaço entre as bordas. Abrir uma oculta a outra; clicar novamente no mesmo botão oculta a tela. Alternar preserva os dados da sessão. A janela fixa tem 80% da largura da barra (320 px) e 65% da altura útil do monitor, com rolagem vertical. Nomes de clientes têm uma linha própria; endereço e entregador quebram linha. A janela fixa não pode ser arrastada. Fechá-la não encerra a barra nem as vendas.

As vendas ficam acima de Consulta/Caixa, e a barra permanece visível acima das janelas. Selecionar uma venda a traz para a frente das demais vendas.

## Minimizar e fechar

Na engrenagem, **Minimizar janela ativa** oculta sem descartar os dados. As vendas ocultas aparecem listadas pelo nome: selecione a que deseja recuperar.

**Fechar janela ativa** encerra somente a selecionada. Uma venda não emitida com dados pede confirmação para descartar. A emissão em andamento deve terminar antes do fechamento. Os mesmos comandos estão no título de cada janela.

A engrenagem também mantém acesso às funções do sistema, impressoras, saída da conta e encerramento do aplicativo. Início com Windows continua nas configurações do aplicativo Windows.

## Verificação

O instalador, blockmap e latest.yml são distribuídos juntos. O atualizador verifica SHA-512; SHA256SUMS.txt permite conferir os arquivos baixados. Cinco resoluções simuladas de 1024×600 até 2560×1440 verificadas sem rolagem horizontal. Testes com banco/perfis temporários cobriram várias vendas, emissão com sucesso/falha, alternância, descarte, minimizar/recuperar, ordem nativa das janelas, impressão entre dois aplicativos e início automático. Impressão física/corte e validação final pelo usuário continuam pendentes.

Mudança exclusiva do Windows. A versão Android permanece 0.1.8; não é necessário atualizar o APK para esta alteração.

## Android — app 0.1.8

[Download app para Android (Android 8+)](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/download/android-v0.1.8-test/SPFARMA-Entregas-0.1.8-teste.apk)

Caixa “Realizada” em Minhas entregas, com confirmação e aviso informativo ao Caixa (✓ verde). A marcação move o cartão para o fim, preserva o arrasto posterior e não faz baixa nem gera repasse. Caixa conclui pelo código em uma única etapa visível. Cartões compactados, cores de status realçadas e gradiente conforme o status: amarelo (impresso), azul (coletado), verde (concluído), sempre para branco. Instalação/teste físico desta versão ainda pendentes.

Busca de clientes por telefone sem DDD, com escolha por nome e DDD quando houver mais de um resultado. Em Minhas entregas, arraste pela alça ⠿ para reordenar os cartões; o cartão flutua durante o gesto e a ordem fica salva por motoboy. Retirada direta por QR Code ou código impresso de seis dígitos, sem reserva prévia.

Instale por cima, sem desinstalar, ou use Menu → Configurações → Aplicativo Android → Verificar atualizações. Mesma assinatura original; Firebase e atualizações internas preservados. O backend precisa estar atualizado. Testes automatizados, interface no navegador e assinatura APK verificados; instalação e gesto no celular físico ainda precisam de confirmação. Consulte o [guia da versão](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/tag/android-v0.1.8-test). Windows permanece na versão estável 0.10.0.
