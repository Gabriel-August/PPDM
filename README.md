📱 Super App Expo - Projeto Integrado

Status: Em Desenvolvimento 🚧

Tecnologia: React Native + Expo

Este projeto é uma demonstração completa das capacidades do Expo, reunindo funcionalidades de hardware, gestos complexos, mapas e persistência de dados em um único aplicativo. Foi desenvolvido com foco em código limpo, componentização e UX moderna.

📂 Estrutura do Projeto

Para garantir que o app funcione, organize seus arquivos desta maneira:

MeuProjeto/
├── assets/                 # Imagens e Músicas (mp3/jpg)
│   ├── Scorpion_-_Wind_of_change_(mp3.pm).mp3
│   ├── blocoDeGelo.jpg
│   └── ...
├── screens/                # Todas as telas criadas
│   ├── Acelerometro.js     # Nível de Bolha
│   ├── ArrastarDrag.js     # Gestos de Arrastar
│   ├── CameraScreen.js     # Câmera e Galeria
│   ├── GpsScreen.js        # Dados de GPS
│   ├── ListaScreen.js      # Tarefas (AsyncStorage)
│   ├── MapaScreen.js       # Google Maps
│   ├── PerfilScreen.js     # Perfil com Menu
│   ├── PinchGestureHandler.js # Zoom em Imagem
│   ├── RotationGestureHandler.js # Rotação de Objeto
│   ├── Som.js              # Player de Música
│   └── WifiScreen.js       # Monitor de Rede
├── App.js                  # Navegação Principal (Drawer/Stack)
├── app.json                # Configurações do Expo
└── package.json            # Dependências


✨ Funcionalidades (Telas)

O aplicativo é dividido em módulos. Aqui está o que cada arquivo faz:

🛠 Ferramentas

Nível de Bolha (Acelerometro.js): Usa o acelerômetro do celular para funcionar como uma ferramenta de nível de pedreiro. A bolinha fica verde quando a superfície está reta.

Monitor Wi-Fi (WifiScreen.js): Mostra status da conexão, SSID, IP e mantém um histórico de quedas de rede.

Monitor GPS (GpsScreen.js): Painel estilo dashboard mostrando Latitude, Longitude, Altitude e Velocidade em tempo real.

🎵 Multimídia

Music Player (Som.js): Player estilo Spotify com capa de álbum, play/pause, loop e barra de progresso. Toca música localmente.

Câmera Pro (CameraScreen.js): Interface de câmera customizada com opção de salvar fotos na galeria do dispositivo.

📝 Produtividade

Lista de Tarefas (ListaScreen.js): Todo-List que salva os dados no celular (AsyncStorage). Nada é perdido ao fechar o app.

👆 Laboratório de Gestos

Zoom (PinchGestureHandler.js): Efeito de pinça para ampliar imagens com efeito elástico estilo Instagram.

Rotação (RotationGestureHandler.js): Gire elementos na tela usando dois dedos.

Arrastar (ArrastarDrag.js): Mova objetos pela tela com física e limites de borda.

Toque Longo (LongPress.js): Botão que exige pressão contínua com feedback tátil (vibração).

🚀 Instalação e Configuração

Siga estes passos se estiver baixando o projeto pela primeira vez ou trocou de computador.

1. Instalar Dependências

Este comando instala tud0 o que é necessário (Mapas, Sensores, Gestos, etc):

npx expo install react-dom react-native-web @expo/metro-runtime react-native-gesture-handler react-native-reanimated expo-sensors expo-av @expo/vector-icons react-native-maps expo-location expo-camera expo-media-library @react-native-async-storage/async-storage @react-native-community/netinfo expo-haptics


2. Iniciar o Projeto

npx expo start


Pressione a para Android (Emulador ou USB).

Pressione w para Web (Limitado, alguns sensores não funcionam).

Escaneie o QR Code com o app Expo Go no seu celular físico.

❓ Solução de Problemas Comuns

🔴 Erro: Unable to resolve module expo-haptics (ou outro módulo)

Isso significa que você esqueceu de instalar uma biblioteca nova.
Solução: Pare o servidor (Ctrl + C) e rode o comando de instalação acima novamente.

🔴 Erro: Invalid value for 'component' prop

Geralmente acontece no App.js ao importar uma tela.
Solução: Verifique se você está usando chaves {} incorretamente.

Errado: import { Som } from './screens/Som'

Certo: import Som from './screens/Som' (Se usar export default).

⚠️ Aviso: Expo AV has been deprecated

O Expo está avisando que o pacote de áudio vai mudar no futuro.
Solução: Pode ignorar por enquanto, o código atual funciona perfeitamente no SDK atual.

📱 O GPS/Wi-Fi não funciona no Emulador

O emulador do Android não tem GPS real nem Wi-Fi real.
Solução:

Para GPS: No emulador, clique nos ... > Location > Set Location.

Para Wi-Fi: Teste sempre no Dispositivo Físico para dados reais.

📦 Detalhe das Dependências

Pacote

Função Principal

Tela Exemplo

expo-av

Áudio e Música

Som.js

expo-camera

Fotos e Vídeo

CameraScreen.js

expo-location

GPS e Geolocalização

GpsScreen.js

expo-sensors

Acelerômetro/Giroscópio

Acelerometro.js

react-native-maps

Mapas (Google/Apple)

MapaScreen.js

async-storage

Salvar dados locais

ListaScreen.js

netinfo

Monitorar Internet

WifiScreen.js

gesture-handler

Toques complexos

Pinch/Drag/Rotate

reanimated

Animações fluídas

Todas de Gesto

Desenvolvido com 💙 por [Seu Nome/Estudante SENAI]
