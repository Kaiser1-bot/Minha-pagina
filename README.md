# Minha-pagina
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Revolução Mental - Livros que Transformam</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --roxo-energetico: #7b2cbf;
            --preto-profundo: #0a0a0a;
            --destaque: #ff6d00;
            --texto: #e2e2e2;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--preto-profundo);
            color: var(--texto);
            line-height: 1.8;
            background-image: radial-gradient(circle at 10% 20%, rgba(123, 44, 191, 0.1) 0%, transparent 20%);
        }
        
        header {
            background: linear-gradient(to right, var(--preto-profundo), var(--roxo-energetico));
            color: white;
            padding: 5vh 0;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 3px solid var(--destaque);
        }
        
        .titulo-impacto {
            font-size: 3.5rem;
            margin: 0;
            font-weight: 800;
            letter-spacing: -1px;
            text-transform: uppercase;
            background: linear-gradient(to right, #fff, #ccc);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
            animation: pulse 2s infinite alternate;
        }
        
        .subtitulo {
            font-size: 1.3rem;
            opacity: 0.9;
            max-width: 800px;
            margin: 15px auto;
            position: relative;
        }
        
        .subtitulo::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: var(--destaque);
            margin: 20px auto;
        }
        
        .container-livros {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            padding: 5vh 10vw;
        }
        
        .livro-card {
            background: rgba(30, 30, 30, 0.7);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            border: 1px solid rgba(123, 44, 191, 0.3);
            position: relative;
        }
        
        .livro-card:hover {
            transform: translateY(-10px) scale(1.03);
            box-shadow: 0 15px 30px rgba(123, 44, 191, 0.4);
            border-color: var(--destaque);
        }
        
        .livro-capa {
            height: 200px;
            background-size: cover;
            background-position: center;
            position: relative;
        }
        
        .livro-detalhes {
            padding: 20px;
        }
        
        .livro-titulo {
            font-size: 1.4rem;
            margin: 0 0 10px;
            color: white;
            font-weight: 600;
        }
        
        .livro-autor {
            color: var(--destaque);
            font-size: 0.9rem;
            margin-bottom: 15px;
            display: block;
        }
        
        .livro-desc {
            font-size: 0.95rem;
            opacity: 0.8;
            margin-bottom: 20px;
        }
        
        .btn-comprar {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(45deg, var(--roxo-energetico), var(--destaque));
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: all 0.3s;
            border: none;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        .btn-comprar:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 109, 0, 0.4);
        }
        
        .destaque-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--destaque);
            color: black;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
            animation: pulse 1.5s infinite;
        }
        
        footer {
            text-align: center;
            padding: 30px;
            background: linear-gradient(to right, var(--roxo-energetico), var(--preto-profundo));
            color: white;
            font-size: 0.9rem;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.05); opacity: 0.9; }
            100% { transform: scale(1); opacity: 1; }
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .flutuante {
            animation: float 4s ease-in-out infinite;
        }
        
        /* Efeito de máquina de escrever */
        .maquina-escrever {
            overflow: hidden;
            border-right: 3px solid var(--destaque);
            white-space: nowrap;
            margin: 0 auto;
            letter-spacing: 1px;
            animation: 
                typing 3.5s steps(40, end),
                blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: var(--destaque); }
        }
    </style>
</head>
<body>
    <header>
        <div class="titulo-impacto">Bem-vindo ao Meu Site</div>
        <div class="subtitulo maquina-escrever">
            Aqui estão seus livros para virar sua vida de cabeça para baixo e evoluir
        </div>
    </header>

    <div class="container-livros">
        <!-- LIVRO 1 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/81fyoFoaxlL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">Mais Vendido</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">Os Segredos da Mente Milionária</h3>
                <span class="livro-autor">T. Harv Eker</span>
                <p class="livro-desc">Reprograme seu "termômetro financeiro" e adote os hábitos das pessoas bem-sucedidas.</p>
                <a href="#comprar" class="btn-comprar">Transforme sua mente</a>
            </div>
        </div>
        
        <!-- LIVRO 2 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/71eFQn2F-QL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">Clássico</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">Pai Rico, Pai Pobre</h3>
                <span class="livro-autor">Robert Kiyosaki</span>
                <p class="livro-desc">O que os ricos ensinam a seus filhos sobre dinheiro que os pobres não fazem.</p>
                <a href="#comprar" class="btn-comprar">Mude sua educação financeira</a>
            </div>
        </div>
        
        <!-- LIVRO 3 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/71mXcISd+5L._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">Recomendação</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">O Homem Mais Rico da Babilônia</h3>
                <span class="livro-autor">George S. Clason</span>
                <p class="livro-desc">Princípios atemporais para acumular riqueza e solucionar problemas financeiros.</p>
                <a href="#comprar" class="btn-comprar">Leia os segredos</a>
            </div>
        </div>
        
        <!-- LIVRO 4 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/81CjPQVcHRL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">Novidade</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">Meu Primeiro Milhão</h3>
                <span class="livro-autor">Thiago Nigro</span>
                <p class="livro-desc">Como sair do zero e construir sua primeira fortuna com educação financeira.</p>
                <a href="#comprar" class="btn-comprar">Comece sua jornada</a>
            </div>
        </div>
        
        <!-- LIVRO 5 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/81j0DP4XGkL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">Mindset</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">O Poder do Hábito</h3>
                <span class="livro-autor">Charles Duhigg</span>
                <p class="livro-desc">Por que fazemos o que fazemos e como transformar padrões para ter sucesso.</p>
                <a href="#comprar" class="btn-comprar">Recrie seus hábitos</a>
            </div>
        </div>
        
        <!-- LIVRO 6 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/71aFt4+OTOL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">Motivacional</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">O Milagre da Manhã</h3>
                <span class="livro-autor">Hal Elrod</span>
                <p class="livro-desc">O segredo para transformar sua vida antes das 8h da manhã.</p>
                <a href="#comprar" class="btn-comprar">Acorde para o sucesso</a>
            </div>
        </div>
    </div>

    <footer>
        <p>© 2023 Revolução Mental - Todos os direitos reservados</p>
        <p style="margin-top: 10px; font-size: 0.8rem; opacity: 0.7;">
            "Sua vida só muda quando você muda" - Jim Rohn
        </p>
    </footer>

    <script>
        // Efeitos interativos
        document.querySelectorAll('.livro-card').forEach((card, index) => {
            card.style.opacity = '0';
            card.style.transform = 'translateY(30px)';
            card.style.animation = `fadeInUp 0.5s ease-out ${index * 0.1 + 0.5}s forwards`;
            
            card.addEventListener('click', function() {
                this.classList.toggle('flutuante');
            });
        });

        // Adiciona a animação fadeInUp dinamicamente
        const style = document.createElement('style');
        style.textContent = `
            @keyframes fadeInUp {
                from { opacity: 0; transform: translateY(30px); }
                to { opacity: 1; transform: translateY(0); }
            }
        `;
        document.head.appendChild(style);
        
        // Efeito de digitação no subtítulo
        function typeWriter(element) {
            const text = element.textContent;
            element.textContent = '';
            
            let i = 0;
            const typing = setInterval(() => {
                if (i < text.length) {
                    element.textContent += text.charAt(i);
                    i++;
                } else {
                    clearInterval(typing);
                    element.style.borderRight = 'none';
                }
            }, 50);
        }
        
        typeWriter(document.querySelector('.maquina-escrever'));
    </script>
</body>
</html>
