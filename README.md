<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Blog</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1 id="titulo-principal">Meu blog tech</h1>
    <p class="subtitulo">Vou compartilhar conhecimentos sobre tecnologia e programação</p>
    <button id="btn-tema" onclick="mudaTema()">Alternar Tema</button>
  </header>

  <main>
    <section class="boas-vindas">
      <p>Boas-vindas ao meu novo blog! Aqui vou compartilhar dicas de programação e curiosidades da área de tecnologia.</p>
    </section>

    <article class="post">
      <h2 class="titulo-post">Colossus: O primeiro computador eletrônico</h2>
      <p>
        O Colossus foi o primeiro computador eletrônico digital programável do mundo, 
        projetado por Tommy Flowers e entregue a Bletchley Park no início de 1944. 
        Seu único propósito era ajudar a decifrar mensagens criptografadas pela máquina 
        alemã Lorenz durante a Segunda Guerra Mundial.
      </p>
      <p>
        Utilizando 2.500 válvulas, o Colossus reduziu drasticamente o tempo de quebra 
        dos códigos, ajudando a decifrar 63 milhões de caracteres até o fim da guerra. 
        Sua existência permaneceu em sigilo absoluto até 1975.
      </p>
    </article>

    <article class="post">
      <h2 class="titulo-post">A reconstrução histórica</h2>
      <p>
        Em 1992, Tony Sale e sua equipe iniciaram a ambiciosa tarefa de reconstruir 
        um Colossus funcional usando apenas fragmentos de diagramas e fotografias antigas. 
        Hoje, a máquina está em exibição no The National Museum of Computing.
      </p>
    </article>

    <article class="post">
      <h2 class="titulo-post">E.R.N.I.E e os números aleatórios</h2>
      <p>
        Parte da mesma equipe de engenheiros do Colossus construiu em 1956 o E.R.N.I.E 
        (Electronic Random Number Indicator Equipment), um gerador de números aleatórios 
        criado para sortear os prêmios mensais dos títulos públicos do Reino Unido.
      </p>
    </article>

    <p class="artigo-fonte">
      Fonte: <a href="https://tnmoc.org" target="_blank">The National Museum of Computing</a>
    </p>
  </main>

  <script src="script.js"></script>
</body>
</html>
Use o código com cuidado.

2. style.css

css
:root {
  --cor-primaria: #183C63;
  --cor-secundaria: #3782d2;
  --cor-fundo: #ffffff;
  --cor-texto: #151428;
  --cor-contraste: #f3eef7;
  --cor-botao: #f9f9f9;
}

.tema-escuro {
  --cor-primaria: #c9e3ff;
  --cor-secundaria: #6cb2ff;
  --cor-fundo: #151428;
  --cor-texto: #ffffff;
  --cor-contraste: #22203d;
  --cor-botao: #2c2a4a;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}

body {
  background-color: var(--cor-fundo);
  color: var(--cor-texto);
  transition: background-color 0.3s, color 0.3s;
}

header {
  background-color: var(--cor-primaria);
  color: var(--cor-fundo);
  padding: 28px 16px;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

#titulo-principal {
  font-size: 32px;
}

.subtitulo {
  font-size: 16px;
  opacity: 0.9;
}

#btn-tema {
  margin-top: 6px;
  background-color: var(--cor-botao);
  color: var(--cor-texto);
  border: 1px solid var(--cor-secundaria);
  padding: 8px 16px;
  border-radius: 6px;
  cursor: pointer;
  font-weight: bold;
}

main {
  max-width: 800px;
  margin: 32px auto;
  padding: 0 16px;
}

.boas-vindas {
  background-color: var(--cor-contraste);
  border-left: 4px solid var(--cor-secundaria);
  padding: 16px 20px;
  border-radius: 6px;
  margin-bottom: 24px;
  line-height: 1.5;
}

.post {
  background-color: var(--cor-contraste);
  padding: 20px;
  border-radius: 8px;
  margin-bottom: 20px;
}

.titulo-post {
  color: var(--cor-secundaria);
  font-size: 24px;
  margin-bottom: 10px;
}

.post p {
  line-height: 1.6;
  margin-bottom: 10px;
}

.artigo-fonte {
  margin-top: 24px;
  font-size: 14px;
}

.artigo-fonte a {
  color: var(--cor-secundaria);
  text-decoration: none;
  font-weight: bold;
}

.artigo-fonte a:hover {
  text-decoration: underline;
}
Use o código com cuidado.

3. script.js

javascript
function mudaTema() {
  const corpoPagina = document.body;
  if (corpoPagina.classList.contains("tema-escuro")) {
    corpoPagina.classList.remove("tema-escuro");
  } else {
    corpoPagina.classList.add("tema-escuro");
  }
}
