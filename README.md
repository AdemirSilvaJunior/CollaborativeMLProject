# CollaborativeMLProject
Collaborative Machine Learning HTML Project - Beginner

<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="stylesheet" href="styles.css">
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projeto Colaborativo de Machine Learning</title>
</head>
<body>
    <header>
        <h1>Projeto Colaborativo de Machine Learning</h1>
        <p>Um espaço para compartilhar informações e recursos sobre Machine Learning.</p>
    </header>

    <section id="conteudo">
        <h2>Conteúdo</h2>
        <p>Adicione aqui informações sobre Machine Learning que você gostaria de compartilhar. Pode ser uma breve introdução, conceitos básicos, ou links úteis.</p>
    </section>

    <section id="projetos-colaborativos">
        <h2>Projetos Colaborativos</h2>
    
        <!-- Formulário para Contribuir com um Projeto -->
        <form id="form-projeto">
            <label for="nome-projeto">Nome do Projeto:</label>
            <input type="text" id="nome-projeto" name="nome-projeto" required>
    
            <label for="descricao-projeto">Descrição do Projeto:</label>
            <textarea id="descricao-projeto" name="descricao-projeto" required></textarea>
    
            <label for="codigo-projeto">Código do Projeto (opcional):</label>
            <textarea id="codigo-projeto" name="codigo-projeto"></textarea>
    
            <button type="submit">Enviar Projeto</button>
        </form>
    
        <!-- Lista de Projetos Colaborativos -->
        <div id="lista-projetos">
            <!-- Os projetos adicionados pelos membros serão exibidos aqui -->
        </div>
    </section>

    <section id="contribuir">
        <h2>Como Contribuir</h2>
        <p>Se você quiser contribuir com informações, exemplos de código ou recursos, sinta-se à vontade para editar este arquivo HTML diretamente ou enviar um pull request no GitHub.</p>
    </section>

    <footer>
        <p><b>&copy; 2023 Ademir Silva Junior</b></p>
    </footer>
</body>

<script>
    document.addEventListener('DOMContentLoaded', function () {
        const formProjeto = document.getElementById('form-projeto');
        const listaProjetos = document.getElementById('lista-projetos');

        formProjeto.addEventListener('submit', function (event) {
            event.preventDefault();

            const nomeProjeto = document.getElementById('nome-projeto').value;
            const descricaoProjeto = document.getElementById('descricao-projeto').value;
            const codigoProjeto = document.getElementById('codigo-projeto').value;

            // Adicione o novo projeto à lista
            const novoProjeto = document.createElement('div');
            novoProjeto.innerHTML = `
                <h3>${nomeProjeto}</h3>
                <p>${descricaoProjeto}</p>
                ${codigoProjeto ? `<pre><code>${codigoProjeto}</code></pre>` : ''}
            `;
            listaProjetos.appendChild(novoProjeto);

            // Limpe o formulário
            formProjeto.reset();
        });
    });
</script>

</html>
