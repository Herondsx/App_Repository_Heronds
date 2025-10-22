<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8">
</head>
<body>

<h1>HaptiChat — chat por vibrações (código Morse)</h1>
<p><strong>Autor:</strong> Heron de Souza</p>

<h2>O que é</h2>
<p>Aplicativo simples em React Native (Expo Go) para duas coisas:</p>
<ul>
  <li><strong>Vibrar um texto em Morse:</strong> você escreve uma frase e o celular vibra o padrão em pontos (·) e traços (—).</li>
  <li><strong>Treinar toques:</strong> você pratica fazendo toques curtos (·) e longos (—) e o app monta as letras.</li>
</ul>

<h2>O que você consegue fazer com o HaptiChat</h2>
<ul>
  <li><strong>Sentir</strong> uma mensagem curta só pela vibração (sem precisar olhar a tela).</li>
  <li><strong>Praticar</strong> o ritmo do Morse com toques e ver o texto gerado.</li>
  <li>Consultar uma <strong>biblioteca</strong> com o alfabeto em Morse (imagens) quando tiver dúvida.</li>
  <li>Repetir o que já fez, usando um <strong>histórico local</strong> salvo no aparelho.</li>
</ul>

<h2>Como usar (passo a passo)</h2>

<h3>1) Modo “Vibrar um texto”</h3>
<ol>
  <li>Acesse a aba <strong>Home</strong>.</li>
  <li>Digite um texto curto (ex.: <em>oi, tudo bem?</em>).</li>
  <li>Toque em <strong>Vibrar</strong>. O celular vibra o padrão Morse da frase.</li>
  <li>Use novamente o botão para repetir quando quiser.</li>
</ol>
<p><em>Observação:</em> a vibração representa cada símbolo (· e —) e as pausas entre letras/palavras.</p>

<h3>2) Modo “Treino de toques”</h3>
<ol>
  <li>Acesse a aba <strong>Train</strong>.</li>
  <li><strong>Toque rápido</strong> para ponto (·) e <strong>segure</strong> para traço (—).</li>
  <li>O app vibra a cada toque e tenta montar a letra quando você faz a pausa.</li>
  <li>O texto decodificado aparece na tela. Apague e tente de novo quando quiser.</li>
</ol>

<h3>3) Biblioteca</h3>
<ul>
  <li>Aba <strong>Library</strong> → imagens com o alfabeto (A–Z, 0–9) e uma legenda simples de sinais.</li>
</ul>

<h3>4) Histórico</h3>
<ul>
  <li>Aba <strong>Chats</strong> → lista das últimas mensagens/treinos salvos no aparelho.</li>
</ul>

<h3>5) Ajustes</h3>
<ul>
  <li>Ajuste de <strong>vibração</strong> ligada/desligada e <strong>sensibilidade</strong> do toque (simples).</li>
</ul>

<h2>O que o app não faz</h2>
<ul>
  <li>Não tem conta, login ou envio online. Tudo é <strong>local</strong>.</li>
  <li>Não usa recursos avançados além do visto em aula.</li>
</ul>

<h2>Tecnologias usadas</h2>
<ul>
  <li><strong>Expo + React Native</strong> (roda no app Expo Go).</li>
  <li><strong>React Navigation</strong> (abas e, se precisar, uma pilha simples).</li>
  <li><strong>AsyncStorage</strong> (salvar histórico e ajustes localmente).</li>
  <li><strong>Vibration</strong> (vibração para o Morse e feedback de toque).</li>
</ul>

<h2>Instalação e execução (Expo Go)</h2>
<pre><code>npx create-expo-app@latest hapti-chat
cd hapti-chat
npm i
npx expo start
# Se precisar de túnel para o celular:
npx expo start --tunnel
</code></pre>

<h2>Estrutura de pastas (simples)</h2>
<pre><code>📦 Project
├─ 🗂️ assets/
│  ├─ icon.png
│  ├─ splash.png
│  └─ library/
│     ├─ morse_chart.png
│     ├─ haptic_pad_guide.png
│     └─ signal_legend.png
├─ 🗂️ src/
│  ├─ components/
│  │  └─ HapticPad.js
│  ├─ screens/
│  │  ├─ Home.js
│  │  ├─ Train.js
│  │  ├─ Chats.js
│  │  └─ Library.js
│  ├─ utils/
│  │  ├─ morse.js
│  │  └─ storage.js
│  └─ navigation.js
├─ App.js
├─ app.json
├─ babel.config.js
└─ package.json
</code></pre>

</body>
</html>
