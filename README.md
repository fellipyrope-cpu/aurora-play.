# Aurora Play — alternativa pessoal de streaming (protótipo Android)

Projeto Android nativo em Kotlin + Jetpack Compose, pensado para celular e TV Box Android.

## O que já está implementado
- Navegação: Início, TV ao vivo, Filmes, Séries, Buscar e Favoritos.
- Interface escura com cards, destaque, categorias e telas de detalhes.
- Catálogo e canais fictícios para demonstração.
- Favoritos mantidos em memória durante a execução.
- Compatibilidade-base Android 7.0+ (minSdk 24), interface responsiva em Compose.

## O que ainda não está implementado
- Não há transmissões, filmes ou séries reais incluídos.
- Os botões de reprodução são demonstrativos; o Media3 está declarado como dependência, mas ainda não foi conectado a URLs de mídia.
- Favoritos e histórico ainda não são persistidos após fechar o app.
- Não foi executada compilação ou teste automatizado neste ambiente.

## Como compilar o APK
1. Instale o Android Studio atualizado e o JDK 17.
2. Abra a pasta `UniTV_Alternativa_Android` no Android Studio.
3. Aguarde a sincronização do Gradle e instale o Android SDK Platform 35 se solicitado.
4. Execute em um dispositivo ou emulador para testar.
5. Para gerar APK: **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. O Android Studio mostrará o caminho do APK gerado.

## TV Box
O layout tem navegação lateral e elementos focáveis como ponto de partida, mas a experiência completa com controle remoto precisa ser testada e refinada em uma TV Box real.

## Conteúdo
Use somente fontes de mídia próprias, de domínio público ou para as quais você tenha autorização. O catálogo atual é fictício e não tenta acessar servidores privados de terceiros.


## Gerar APK automaticamente pelo GitHub Actions
1. Crie um repositório no GitHub e envie os arquivos desta pasta para a branch `main`.
2. Abra a aba **Actions** e execute **Build Android APK** (ou aguarde o build após o push).
3. Quando o workflow terminar, abra a execução concluída e baixe o artefato `aurora-play-debug-apk`.
4. Extraia o ZIP do artefato: dentro estará `app-debug.apk`, que pode ser instalado no Android.

O APK gerado por esse fluxo é de depuração (`debug`), adequado para testes pessoais. O fluxo ainda precisa ser executado no GitHub para produzir o binário.
