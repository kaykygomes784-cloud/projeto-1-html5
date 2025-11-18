# projeto-1-html5 
projeto/
index.html
projetos.html
cadastro.html
imagens/
logo.png
 voluntariado.jpg
doacao.jpg
styles/
style.css
scripts/
script.js

Página Inicial (index.html):

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Organização</title>
    <link rel="stylesheet" href="styles/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Início</a></li>
                <li><a href="projetos.html">Projetos Sociais</a></li>
                <li><a href="cadastro.html">Cadastro</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h1>Organização</h1>
        <p>Bem-vindo à nossa organização!</p>
        <address>
            Contato: <a href="mailto:contato@organizacao.com">contato@organizacao.com</a>
        </address>
        <img src="imagens/logo.png" alt="Logo da Organização">
    </main>
    <footer>
        <p>&copy; 2023 Organização</p>
    </footer>
</body>
</html>

Página de Projetos Sociais (projetos.html):

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projetos Sociais</title>
    <link rel="stylesheet" href="styles/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Início</a></li>
                <li><a href="projetos.html">Projetos Sociais</a></li>
                <li><a href="cadastro.html">Cadastro</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h1>Projetos Sociais</h1>
        <p>Conheça nossos projetos sociais!</p>
        <section>
            <h2>Voluntariado</h2>
            <p>Participe do nosso voluntariado!</p>
            <img src="imagens/voluntariado.jpg" alt="Voluntariado">
        </section>
        <section>
            <h2>Doação</h2>
            <p>Faça uma doação para nossa causa!</p>
            <img src="imagens/doacao.jpg" alt="Doação">
        </section>
    </main>
    <footer>
        <p>&copy; 2023 Organização</p>
    </footer>
</body>
</html>

Página de Cadastro (cadastro.html):

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro</title>
    <link rel="stylesheet" href="styles/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Início</a></li>
                <li><a href="projetos.html">Projetos Sociais</a></li>
                <li><a href="cadastro.html">Cadastro</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <h1>Cadastro</h1>
        <form>
            <fieldset>
                <legend>Informações Pessoais</legend>
                <label for="nome">Nome Completo:</label>
                <input type="text" id="nome" name="nome" required>
                <label for="email">E-mail:</label>
                <input type="email" id="email" name="email" required>
                <label for="cpf">CPF:</label>
                <input type="text" id="cpf" name="cpf" pattern="\d{3}\.\d{3}\.\d{3}-\d{2}" required>
                <label for="telefone">Telefone:</label>
                <input type="tel" id="telefone" name="telefone" pattern="\(\d{2}\) \d{4,5}-\d{4}" required>
                <label for="nascimento">Data de Nascimento:</label>
                <input type="date" id="nascimento" name="nascimento" required>
            </fieldset>
            <fieldset>
                <legend>Endereço</legend>
                <label for="endereco">Endereço:</label>
                <input type="text" id="endereco" name="endereco" required>
                <label for="cep">CEP:</label>
                <input type="text" id="cep" name="cep" pattern="\d{5}-\d{3}" required>
                <label for="cidade">Cidade:</label>
                <input type="text" id="cidade" name="cidade" required>
                <label for="estado">Estado:</label>
                <select id="estado" name="estado" required>
                    <option value="">Selecione</option>
                    <option value="AC">Acre</option>
                    <option value="AL">Alagoas</option>
                    <!-- Adicione mais opções aqui -->
                </select>
            </fieldset>
            <button type="submit">Cadastrar</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2023 Organização</p>
    </footer>
    <script src="scripts/script.js"></script>
</body>
</html>

JavaScript para Máscaras de Input:

// scripts/script.js
const cpfInput = document.getElementById('cpf');
const telefoneInput = document.getElementById('telefone');
const cepInput = document.getElementById('cep');

cpfInput.addEventListener('input', () => {
    cpfInput.value = cpfInput.value.replace(/(\d{3})(\d{3})(\d{3})(\d{2})/, '$1.$2.$3-$4');
});

telefoneInput.addEventListener('input', () => {
    telefoneInput.value = telefoneInput.value.replace(/(\d{2})(\d{4,5})(\d{4})/, '($1) $2-$3');
});

cepInput.addEventListener('input', () => {
    cepInput.value = cepInput.value.replace(/(\d{5})(\d{3})/, '$1-$2');
});
