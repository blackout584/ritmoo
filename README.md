# Ritmo — player de música gratuito para Android

Inspirado nos recursos do Poweramp, feito do zero em Kotlin + Jetpack Compose + Media3 (ExoPlayer).

## O que já funciona (versão 1.0)
- Biblioteca: músicas, álbuns (com capas), artistas e pastas, com busca
- Player completo: tocar/pausar, anterior/próxima, barra de progresso, aleatório, repetir (todas / uma)
- Fila de reprodução: tocar a seguir, adicionar à fila e remover da fila
- Reprodução em segundo plano com notificação e controles na tela de bloqueio
- Pausa automática ao desconectar o fone
- Reprodução sem pausa entre faixas (gapless)
- Playlists: criar, renomear, excluir, adicionar e remover músicas, além da playlist "Favoritas"
- Equalizador: bandas ajustáveis, predefinições, reforço de graves e som 3D (salvos automaticamente)
- Velocidade de reprodução (0,5x a 2x)
- Timer para dormir
- Temas: claro, escuro, sistema, Material You e 6 cores de destaque
- Filtro para esconder áudios curtos (áudios do WhatsApp, toques)

## Próximas etapas sugeridas
- Crossfade (transição suave entre músicas)
- Letras de músicas
- Widget na tela inicial
- Android Auto
- Editor de tags (título, artista, capa)

## Como abrir e rodar
1. Instale o **Android Studio** (gratuito): https://developer.android.com/studio
2. Descompacte este .zip.
3. No Android Studio, use **File > Open** e selecione a pasta `Ritmo`.
4. Aguarde o Gradle sincronizar. Na primeira vez, ele baixa tudo o que precisa, o que pode levar alguns minutos.
   - Se aparecer uma sugestão para atualizar o Gradle ou o AGP, você pode aceitar.
5. No celular, ative as **Opções do desenvolvedor** e a **Depuração USB**:
   Configurações > Sobre o telefone > toque 7 vezes em "Número da versão".
6. Conecte o celular pelo cabo USB e clique no botão ▶ (Run) do Android Studio.

## Para publicar na Play Store
Use **Build > Generate Signed App Bundle / APK**, crie uma chave de assinatura (guarde-a bem!) e envie o arquivo `.aab` pelo Google Play Console (taxa única de US$ 25).

## Estrutura do projeto
```
app/src/main/java/com/ritmo/player/
├── MainActivity.kt          tela inicial e pedido de permissão
├── data/                    músicas, playlists e configurações
├── playback/                serviço de reprodução e equalizador
└── ui/                      telas (biblioteca, player, equalizador, ajustes)
```
