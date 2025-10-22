<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
  <title>HaptiChat — README</title>
</head>
<body>

<h1>HaptiChat — chat por vibrações (código Morse)</h1>
<p><strong>Autor:</strong> Heron de Souza</p>

<h2>O que é</h2>
<p>Aplicativo móvel feito com React Native (Expo Go) para treinar e trocar mensagens simples em código Morse usando toques curtos (·) e longos (—) com feedback por vibração.</p>

<h2>Como funciona (resumo)</h2>
<ul>
  <li>Você toca rápido para <strong>·</strong> e mantém pressionado para <strong>—</strong>.</li>
  <li>O app vibra em cada símbolo e ao fechar uma letra/palavra.</li>
  <li>O histórico das mensagens e ajustes são salvos localmente.</li>
  <li>A navegação usa abas (telas principais) e pilha (detalhes).</li>
</ul>

<h2>Funcionalidades</h2>
<ul>
  <li><strong>Treino Morse:</strong> área para praticar toques curtos/longos com vibração.</li>
  <li><strong>Conversas locais:</strong> lista de mensagens enviadas/recebidas (texto + horário).</li>
  <li><strong>Biblioteca:</strong> referência do alfabeto (A–Z, 0–9, sinais) com imagens.</li>
  <li><strong>Configurações:</strong> sensibilidade de toque e ligar/desligar vibração.</li>
</ul>

<h2>Tecnologias usadas</h2>
<ul>
  <li><strong>Expo + React Native</strong> (executa no app Expo Go).</li>
  <li><strong>React Navigation</strong> (Bottom Tabs + Stack).</li>
  <li><strong>AsyncStorage</strong> (armazenamento local key–value).</li>
  <li><strong>Vibration</strong> (atuador de vibração do dispositivo).</li>
</ul>

<h2>Instalação e execução (Expo Go)</h2>
<pre><code>npx create-expo-app@latest hapti-chat
cd hapti-chat
npm i
npx expo start
# Se precisar de túnel para o celular:
npx expo start --tunnel
</code></pre>

<h2>Estrutura de pastas</h2>
<pre><code>📦 hapti-chat
├─ 📄 App.tsx
├─ 📄 package.json
├─ 📄 app.json
├─ 📄 tsconfig.json
├─ 📄 babel.config.js
├─ 🗂️ assets/
│  ├─ 🖼️ icon.png
│  ├─ 🖼️ splash.png
│  └─ 🗂️ library/
│     ├─ 🖼️ morse_a.png
│     ├─ 🖼️ morse_b.png
│     └─ 🖼️ ...
├─ 🗂️ src/
│  ├─ 🗂️ navigation/
│  │  └─ 📄 index.tsx              <!-- Abas (Tabs) + Pilha (Stack) -->
│  ├─ 🗂️ screens/
│  │  ├─ 📄 HomeScreen.tsx
│  │  ├─ 📄 TrainScreen.tsx
│  │  ├─ 📄 ChatsScreen.tsx
│  │  ├─ 📄 ChatDetailScreen.tsx
│  │  ├─ 📄 LibraryScreen.tsx
│  │  └─ 📄 SettingsScreen.tsx
│  ├─ 🗂️ components/
│  │  ├─ 📄 HapticPad.tsx          <!-- Captura · e — -->
│  │  ├─ 📄 MessageBubble.tsx
│  │  └─ 📄 MorseChart.tsx
│  ├─ 🗂️ hooks/
│  │  ├─ 📄 useMorse.ts            <!-- encode/decode + tempos -->
│  │  ├─ 📄 useHaptics.ts          <!-- vibração (sucesso/erro) -->
│  │  └─ 📄 useShakeToClear.ts     <!-- opcional (acelerômetro) -->
│  ├─ 🗂️ lib/
│  │  ├─ 📄 morseMap.ts            <!-- mapeamento A–Z, 0–9, sinais -->
│  │  └─ 📄 morseDecoder.ts        <!-- máquina de estados -->
│  ├─ 🗂️ services/
│  │  └─ 📄 storage.ts             <!-- AsyncStorage (keys, get/set) -->
│  ├─ 🗂️ styles/
│  │  └─ 📄 theme.ts               <!-- cores/tipografia -->
│  └─ 🗂️ types/
│     └─ 📄 index.ts               <!-- tipos de Message, Settings -->
└─ 📄 README.md
</code></pre>

<p><em>Observação:</em> o foco é usar somente conteúdos trabalhados em aula (React Native com Expo, navegação, imagens, armazenamento local e atuador de vibração).</p>

</body>
</html>
