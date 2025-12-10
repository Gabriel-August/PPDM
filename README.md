📱 Projeto Multi-Funcional Expo

Este projeto é uma coleção de funcionalidades avançadas utilizando React Native e Expo. Ele demonstra o uso de sensores, gestos, multimídia, mapas, armazenamento local e monitoramento de rede em um único aplicativo.

🚀 Instalação Rápida

Para rodar este projeto, você precisa instalar todas as dependências abaixo.
Execute o comando único no seu terminal:

npx expo install react-dom react-native-web @expo/metro-runtime react-native-gesture-handler react-native-reanimated expo-sensors expo-av @expo/vector-icons react-native-maps expo-location expo-camera expo-media-library @react-native-async-storage/async-storage @react-native-community/netinfo expo-haptics


📦 Lista de Dependências Utilizadas

Abaixo, a explicação do que cada pacote faz no nosso projeto:

1. Núcleo e Web

Essenciais para o projeto rodar, inclusive no navegador.

expo: Framework base.

react-native-web: Permite rodar o app no navegador (Chrome/Edge).

react-dom: Renderizador necessário para a versão web.

@expo/metro-runtime: Motor que faz o javascript rodar na web.

2. Gestos e Animações (Telas de Interação)

Usados nas telas de Arrastar, Pinça (Zoom), Rotação e Toque Longo.

react-native-gesture-handler: Detecta toques complexos (arrastar, girar, pinça).

react-native-reanimated: Cria animações fluidas (60fps) e de alta performance.

3. Sensores e Hardware

expo-sensors: Usado na tela Nível de Bolha para acessar o Acelerômetro.

expo-haptics: Usado na tela Toque Longo para fazer o celular vibrar (feedback tátil).

4. Multimídia

expo-av: Usado no Player de Música (tocar/pausar áudio).

expo-camera: Usado na tela de Câmera para tirar fotos.

expo-media-library: Permite salvar as fotos tiradas na galeria do celular.

5. Mapas e Localização

react-native-maps: Exibe o mapa visual (Google/Apple Maps).

expo-location:

Pega a posição GPS (Latitude/Longitude).

Necessário para ler o nome do Wi-Fi (SSID) no Android.

Usado nas telas de Mapa, GPS e Wi-Fi.

6. Armazenamento de Dados

@react-native-async-storage/async-storage:

Salva dados no celular que não somem ao fechar o app.

Usado na Lista de Tarefas para salvar os itens.

7. Rede e Conectividade

@react-native-community/netinfo:

Monitora se tem internet, tipo de conexão (Wi-Fi/4G) e IP.

Usado na tela de Monitor Wi-Fi.

8. Visual

@expo/vector-icons: Biblioteca de ícones (MaterialIcons, FontAwesome, Ionicons) usada em todos os botões e menus.

🛠 Comandos Úteis

Iniciar o Projeto

npx expo start


Limpar Cache (Se der erro estranho)

npx expo start --clear


Rodar especificamente no Android

npx expo start --android
