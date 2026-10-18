# SPFARMA — Aplicativos para Windows e Android

## Windows 0.17.0

[Baixar instalador Windows x64](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/latest/download/SPFARMA-Flutuante-Instalador.exe)

## Acesso salvo, Alt+D e tamanho em 1024×768 — 18/10/2026

- Em **Engrenagem → Configurações → Acesso automático**, salve usuário e senha. O app usa esse acesso na próxima abertura. A senha é protegida pelo Windows neste computador e não é exibida novamente; para trocar, digite e salve a nova senha. **Remover acesso salvo** desativa esse comportamento. Falha de autenticação permite entrar manualmente e corrigir as configurações.
- **Alt+D** abre +Venda por padrão. Atalhos personalizados são preservados; é possível alterar ou deixar vazio e salvar para desativar. Configurações antigas sem atalho de vendas recebem Alt+D uma vez.
- Em 1024×768, barra e janelas usam o mesmo tamanho em pixels da versão 1366×768: barra 341×41 e janelas 273 px de largura, em escala de 100%. Altura, título e conteúdo acompanham a escala e respeitam a área útil; Consulta/Caixa ficam acima da barra. 1024×600 mantém as dimensões anteriores.
- Inclui os ajustes compartilhados de clientes/relatório: filtro Todos, telefone de 8 a 11 dígitos e máscara pela direita. Novas entregas do motoboy entram acima das informadas como realizadas.

Instale por cima da versão atual após concluir/fechar as vendas. Perfil, impressoras, início automático e sessão são preservados. Acesso salvo é específico do usuário Windows deste computador. Testes usam perfis temporários; não preconfiguram credenciais pessoais nem deixam instalação permanente.

## Android 0.1.12 — Canal de teste

[Baixar APK Android](https://github.com/eltonfelipe260296-byte/spfarma-app-windows/releases/download/android-v0.1.12-test/SPFARMA-Entregas-0.1.12-teste.apk)

Android 8 ou superior. Pacote com.spfarma.entregas, versionCode 13, assinatura original preservada.

Inclui filtro Todos no relatorio de entregadores; importacao e cadastro com telefones de 8 a 11 digitos; busca com ou sem DDD e nono digito, com selecao se houver ambiguidades; mascara preenchida pela direita. Endereco importado usa rua/bairro/cidade da base e carrega a taxa atual ao selecionar em Vendas. Novas entregas ficam antes das marcadas como realizadas pelo motoboy, mantendo a ordem manual.

Instale por cima, sem desinstalar, e confirme quando o Android solicitar. Configuracoes > Aplicativo Android > Verificar atualizacoes tambem oferece a versao. A ordenacao e validacao de numeros locais exigem backend atualizado junto. Atualizar o site nao substitui os arquivos incluidos no APK.

Assinatura, Firebase e fontes conferidos; ponte Capacitor e regressao verificadas com servicos nativos simulados. Teste no aparelho fisico permanece pendente. Nao inclui credenciais privadas nem altera banco de producao. Pre-lancamento Android separado do latest Windows 0.17.0.
