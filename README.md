<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biblioteca da Evolução - Livros que Transformam Vidas</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --azul-profundo: #0f4c81;
            --dourado: #ffd700;
            --preto: #111;
            --branco: #f9f9f9;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--preto);
            color: var(--branco);
            line-height: 1.8;
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(15, 76, 129, 0.15) 0%, transparent 25%),
                radial-gradient(circle at 90% 80%, rgba(255, 215, 0, 0.1) 0%, transparent 25%);
        }
        
        header {
            background: linear-gradient(135deg, var(--azul-profundo), #1a1a2e);
            color: white;
            padding: 8vh 0;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 4px solid var(--dourado);
        }
        
        .titulo-impacto {
            font-size: clamp(2.5rem, 5vw, 4rem);
            margin: 0;
            font-weight: 800;
            letter-spacing: -1px;
            background: linear-gradient(to right, var(--dourado), #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }
        
        .subtitulo {
            font-size: clamp(1rem, 2vw, 1.3rem);
            max-width: 800px;
            margin: 15px auto;
            position: relative;
            color: rgba(255, 255, 255, 0.9);
        }
        
        .subtitulo::after {
            content: '';
            display: block;
            width: 100px;
            height: 3px;
            background: var(--dourado);
            margin: 20px auto;
        }

        /* Barra de Busca Moderna */
        .search-container {
            margin: 40px auto;
            max-width: 800px;
            display: flex;
            gap: 10px;
            padding: 0 20px;
        }
        .search-bar {
            flex: 1;
            padding: 15px 25px;
            border: 2px solid var(--dourado);
            border-radius: 50px;
            font-size: 1rem;
            background: rgba(20, 20, 20, 0.8);
            color: white;
            transition: all 0.3s;
        }
        .search-bar:focus {
            outline: none;
            box-shadow: 0 0 0 3px rgba(255, 215, 0, 0.3);
        }
        .search-btn {
            background: linear-gradient(45deg, var(--azul-profundo), #16213e);
            color: var(--dourado);
            border: 2px solid var(--dourado);
            padding: 0 30px;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s;
        }
        .search-btn:hover {
            background: linear-gradient(45deg, #16213e, var(--azul-profundo));
            transform: scale(1.03);
        }

        /* Grid de Livros */
        .container-livros {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            padding: 5vh 10vw;
        }
        
        .livro-card {
            background: rgba(30, 30, 30, 0.8);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.25, 0.8, 0.25, 1);
            box-shadow: 0 8px 25px rgba(0,0,0,0.3);
            border: 1px solid rgba(255, 215, 0, 0.1);
            position: relative;
        }
        
        .livro-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(15, 76, 129, 0.4);
            border-color: var(--dourado);
        }
        
        .livro-capa {
            height: 250px;
            background-size: cover;
            background-position: center;
            position: relative;
        }
        
        .livro-detalhes {
            padding: 25px;
        }
        
        .livro-titulo {
            font-size: 1.4rem;
            margin: 0 0 10px;
            color: var(--dourado);
            font-weight: 700;
        }
        
        .livro-autor {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            margin-bottom: 15px;
            display: block;
        }
        
        .livro-desc {
            font-size: 0.95rem;
            opacity: 0.8;
            margin-bottom: 20px;
            min-height: 60px;
        }

        .preco-amazon {
            margin: 15px 0;
            color: var(--dourado);
            font-size: 1rem;
            font-weight: bold;
        }
        
        .btn-comprar {
            display: inline-block;
            padding: 12px 25px;
            background: linear-gradient(45deg, var(--azul-profundo), #1a1a2e);
            color: var(--dourado);
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s;
            border: 2px solid var(--dourado);
            font-size: 0.9rem;
            text-align: center;
            width: 100%;
            box-sizing: border-box;
        }
        
        .btn-comprar:hover {
            background: linear-gradient(45deg, #1a1a2e, var(--azul-profundo));
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(255, 215, 0, 0.2);
        }
        
        .destaque-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--dourado);
            color: var(--preto);
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }
        
        footer {
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(to right, var(--azul-profundo), #16213e);
            color: white;
            font-size: 0.9rem;
            margin-top: 50px;
            border-top: 3px solid var(--dourado);
        }
        
        /* Animações */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .flutuante {
            animation: float 4s ease-in-out infinite;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .container-livros {
                grid-template-columns: 1fr;
                padding: 5vh 5vw;
            }
            
            .search-container {
                flex-direction: column;
            }
            
            .search-bar, .search-btn {
                width: 100%;
            }
            
            .search-btn {
                padding: 12px;
            }
        }

        /* Melhorias para mobile */
        button, a {
            min-height: 48px;
            -webkit-tap-highlight-color: transparent;
        }
    </style>
</head>
<body>
    <header>
        <div class="titulo-impacto">Biblioteca da Evolução</div>
        <div class="subtitulo">
            Livros que viram sua vida de cabeça para baixo e aceleram sua transformação
        </div>
    </header>

    <!-- Barra de Busca -->
    <div class="search-container">
        <input type="text" id="searchInput" placeholder="🔍 Busque por título, autor ou tema..." class="search-bar">
        <button onclick="searchBooks()" class="search-btn">Buscar</button>
    </div>

    <!-- Grid de Livros -->
    <div class="container-livros">
        <!-- Livro 1 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/81fyoFoaxlL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">TOP 1</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">Os Segredos da Mente Milionária</h3>
                <span class="livro-autor">T. Harv Eker</span>
                <p class="livro-desc">Reprograme seu mindset financeiro e adote os hábitos das pessoas bem-sucedidas.</p>
                <div class="preco-amazon" id="preco1">
                    🛒 Preço: <strong>R$ 42,90</strong>
                </div>
                <a href="https://www.amazon.com.br/dp/B0A8YWRXJR" target="_blank" class="btn-comprar">Comprar na Amazon</a>
            </div>
        </div>
        
        <!-- Livro 2 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/71eFQn2F-QL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">CLÁSSICO</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">Pai Rico, Pai Pobre</h3>
                <span class="livro-autor">Robert Kiyosaki</span>
                <p class="livro-desc">A educação financeira que os ricos recebem e as escolas não ensinam.</p>
                <div class="preco-amazon" id="preco2">
                    🛒 Preço: <strong>R$ 47,90</strong>
                </div>
                <a href="https://www.amazon.com.br/dp/B0A8XYFV5K" target="_blank" class="btn-comprar">Comprar na Amazon</a>
            </div>
        </div>
        
        <!-- Livro 3 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/71mXcISd+5L._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">ESSENCIAL</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">O Homem Mais Rico da Babilônia</h3>
                <span class="livro-autor">George S. Clason</span>
                <p class="livro-desc">Princípios atemporais para acumular riqueza e solucionar problemas financeiros.</p>
                <div class="preco-amazon" id="preco3">
                    🛒 Preço: <strong>R$ 29,90</strong>
                </div>
                <a href="https://www.amazon.com.br/dp/B07CKYQ5WY" target="_blank" class="btn-comprar">Comprar na Amazon</a>
            </div>
        </div>
        
        <!-- Livro 4 -->
        <div class="livro-card">
            <div class="livro-capa" style="background-image: url('https://m.media-amazon.com/images/I/81CjPQVcHRL._AC_UF1000,1000_QL80_.jpg');">
                <div class="destaque-badge">BRASIL</div>
            </div>
            <div class="livro-detalhes">
                <h3 class="livro-titulo">Meu Primeiro Milhão</h3>
                <span class="livro-autor">Thiago Nigro</span>
                <p class="livro-desc">Como construir sua primeira fortuna com educação financeira prática.</p>
                <div class="preco-amazon" id="preco4">
                    🛒 Preço: <strong>R$ 39,90</strong>
                </div>
                <a href="https://www.amazon.com.br/dp/B0B1JHCDM7" target="_blank" class="btn-comprar">Comprar na Amazon</a>
            </div>
        </div>
    </div>

    <footer>
        <p>© 2023 Biblioteca da Evolução - Todos os direitos reservados</p>
        <p style="margin-top: 15px; opacity: 0.8;">
            "O conhecimento é a única coisa que ninguém pode tirar de você" - Elon Musk
        </p>
    </footer>

    <script>
        // Sistema de Busca
        function searchBooks() {
            const input = document.getElementById('searchInput').value.toLowerCase();
            const books = document.querySelectorAll('.livro-card');
            
            books.forEach(book => {
                const title = book.querySelector('.livro-titulo').textContent.toLowerCase();
                const author = book.querySelector('.livro-autor').textContent.toLowerCase();
                const isVisible = title.includes(input) || author.includes(input);
                
                book.style.display = isVisible ? 'block' : 'none';
            });
        }
        
        // Busca em tempo real
        document.getElementById('searchInput').addEventListener('input', searchBooks);

        // Efeito de hover nos cards
        document.querySelectorAll('.livro-card').forEach(card => {
            card.addEventListener('mouseenter', () => {
                card.style.transform = 'translateY(-10px)';
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'translateY(0)';
            });
        });
    </script>
</body>
</html>
