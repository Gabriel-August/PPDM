📱 Super App Expo - Projeto Integrado

Este projeto é uma demonstração robusta das capacidades do Expo SDK, reunindo funcionalidades de hardware (sensores, câmera, GPS), gestos complexos, mapas e persistência de dados em um único aplicativo modular.

📑 Tabela de Conteúdos

Estrutura de Pastas

Catálogo de Telas e Funcionalidades

Dependências e Tecnologias

Instalação e Execução

Solução de Problemas (FAQ)

📂 Estrutura de Pastas

A organização do projeto segue o padrão de separação por responsabilidade.

MeuProjeto/
├── assets/                 # Recursos estáticos
│   ├── Scorpion_-_Wind_of_change_(mp3.pm).mp3
│   ├── blocoDeGelo.jpg
│   └── ...
├── screens/                # Módulos do Aplicativo
│   ├── Acelerometro.js     # Ferramenta de Nível
│   ├── ArrastarDrag.js     # Lab. de Gestos (Drag)
│   ├── CameraScreen.js     # Câmera e Galeria
│   ├── GpsScreen.js        # Dashboard GPS
│   ├── ListaScreen.js      # Tarefas (Persistência)
│   ├── MapaScreen.js       # Mapas Visuais
│   ├── PerfilScreen.js     # UI de Perfil
│   ├── PinchGestureHandler.js # Lab. de Gestos (Zoom)
│   ├── RotationGestureHandler.js # Lab. de Gestos (Rotação)
│   ├── Som.js              # Music Player
│   └── WifiScreen.js       # Monitor de Rede
├── App.js                  # Navegação (Entry Point)
└── app.json                # Configurações do Expo


📱 Catálogo de Telas e Funcionalidades

Abaixo, a relação de cada arquivo com sua funcionalidade e o que ele demonstra tecnicamente.

Tela / Arquivo

Categoria

Descrição Funcional

Acelerometro.js

🛠 Ferramentas

Nível de bolha digital. A interface muda de cor (Verde/Vermelho) dependendo da inclinação do dispositivo.

WifiScreen.js

🛠 Ferramentas

Monitor de rede em tempo real. Exibe SSID, IP e log de quedas de conexão.

GpsScreen.js

🛠 Ferramentas

Dashboard de dados de localização: Latitude, Longitude, Altitude e Velocidade (km/h).

Som.js

🎵 Multimídia

Player de música completo com controles de Loop, Play/Pause e barra de progresso.

CameraScreen.js

🎵 Multimídia

Câmera personalizada com botão de disparo, troca de câmera (frontal/traseira) e salvamento na galeria.

ListaScreen.js

📝 Produtividade

Lista de tarefas persistente. Os dados não somem ao fechar o app (AsyncStorage).

MapaScreen.js

🗺 Mapas

Visualização de mapa (Google/Apple Maps) com marcador na posição atual do usuário.

Pinch...js

👆 Gestos

Demonstração de Zoom (Pinça) em imagens com efeito elástico ("Snap back").

Rotation...js

👆 Gestos

Rotação de elementos na tela utilizando dois dedos.

Arrastar...js

👆 Gestos

Movimentação de objetos (Drag & Drop) com física e limites de tela.

LongPress.js

👆 Gestos

Botão de pressão longa com feedback tátil (vibração/haptics).

📦 Dependências e Tecnologias

Principais bibliotecas utilizadas para construir as funcionalidades acima.

Pacote

Uso Principal

expo-av

Reprodução de áudio e música.

expo-camera

Acesso à câmera do dispositivo.

expo-media-library

Permissões para salvar fotos na galeria.

expo-location

Acesso ao GPS e permissões de localização (necessário para Wi-Fi no Android).

expo-sensors

Acesso ao Acelerômetro e Giroscópio.

expo-haptics

Feedback tátil (vibração) físico.

react-native-maps

Renderização de mapas nativos.

async-storage

Banco de dados local simples (Chave-Valor).

netinfo

Monitoramento de estado de rede (Online/Offline).

gesture-handler

Sistema avançado de toques e gestos.

reanimated

Sistema de animações de alta performance (60fps).

🚀 Instalação e Execução

1. Pré-requisitos

Certifique-se de ter o Node.js instalado e o ambiente Expo configurado.

2. Instalar todas as dependências

Execute este comando único para garantir que todas as bibliotecas necessárias estejam presentes:

npx expo install react-dom react-native-web @expo/metro-runtime react-native-gesture-handler react-native-reanimated expo-sensors expo-av @expo/vector-icons react-native-maps expo-location expo-camera expo-media-library @react-native-async-storage/async-storage @react-native-community/netinfo expo-haptics


3. Rodar o Projeto

npx expo start


Android: Pressione a (Requer Emulador ou USB).

Web: Pressione w (Funcionalidades de sensores/GPS são limitadas).

iOS: Pressione i (Requer macOS/Simulator ou iPhone físico).

❓ Solução de Problemas (FAQ)

🔴 Erro: Unable to resolve module expo-haptics

Causa: Biblioteca não instalada.
Solução: Pare o servidor e rode: npx expo install expo-haptics.

🔴 Erro: Invalid value for 'component' prop

Causa: Erro na importação da tela no App.js.
Solução: Verifique se usou chaves {} incorretamente.

❌ Errado: import { Som } from './screens/Som'

✅ Certo: import Som from './screens/Som' (Para export default).

📱 GPS ou Wi-Fi não funcionam no Emulador

Causa: Limitação do Emulador.
Solução:

GPS: No emulador, vá em ... > Location e defina uma coordenada.

Wi-Fi: O emulador simula uma rede genérica "AndroidWifi". Para ver o nome real do seu Wi-Fi, use um dispositivo físico.

⚠️ Erro de Permissão (Câmera/Galeria)

Solução: Se o app fechar ou não salvar a foto, vá nas configurações do celular > Aplicativos > Expo Go > Permissões e garanta que tudo está permitido.

Desenvolvido para fins educacionais e demonstrativos.
