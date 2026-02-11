# aniversario.20
<style>
    /* RESET GERAL */
    .meu-widget-aniversario {
        all: initial;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    /* FUNDO ANIMADO */
    .fundo-fixo {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
        animation: corMexe 15s ease infinite;
        z-index: 999999;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 20px;
        box-sizing: border-box;
    }

    /* CARTÃO DE VIDRO */
    .cartao-vidro {
        background: rgba(255, 255, 255, 0.95);
        border-radius: 25px;
        padding: 30px;
        text-align: center;
        width: 100%;
        max-width: 400px;
        box-shadow: 0 20px 50px rgba(0,0,0,0.2);
        color: #333;
        animation: sobe 0.6s ease-out;
        position: relative;
    }

    /* BOTÃO PRINCIPAL (ROSA) */
    .meu-botao {
        background: #ff758c;
        color: white;
        border: none;
        padding: 14px 35px;
        font-size: 1.1rem;
        border-radius: 50px;
        cursor: pointer;
        margin-top: 25px;
        font-weight: bold;
        transition: 0.3s;
        box-shadow: 0 5px 15px rgba(255, 117, 140, 0.4);
        display: inline-block;
        text-decoration: none;
    }
    .meu-botao:hover { transform: scale(1.05); background: #ff5e78; }

    /* BOTÃO DE MÚSICA (PRETO) */
    .botao-musica {
        background: #222;
        color: #fff;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
        padding: 12px;
        border-radius: 12px;
        text-decoration: none;
        margin-top: 20px;
        font-size: 0.9rem;
        font-weight: 600;
        transition: 0.2s;
        border: 1px solid #444;
    }
    .botao-musica:hover { background: #000; transform: translateY(-2px); }
    .icone-play { font-size: 1.2rem; }

    /* TEXTOS */
    h1 { margin: 0 0 10px 0; color: #ff758c; font-size: 2.2rem; font-family: 'Georgia', serif; }
    p { font-size: 1.05rem; line-height: 1.6; margin-bottom: 12px; color: #555; }
    
    .destaque-final { color: #ff758c; font-weight: bold; font-size: 1.4rem; display: block; margin-top: 15px; border-top: 1px solid #eee; padding-top: 15px; }
    .tela-oculta { display: none; }
    .aviso-pequeno { font-size: 0.75rem; color: #999; margin-top: 5px; }

    @keyframes corMexe { 
        0% { background: linear-gradient(120deg, #84fab0, #8fd3f4); }
        50% { background: linear-gradient(120deg, #e0c3fc, #8ec5fc); }
        100% { background: linear-gradient(120deg, #84fab0, #8fd3f4); }
    }
    @keyframes sobe { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
</style>

<div class="meu-widget-aniversario">
    <div class="fundo-fixo">
        
        <div id="tela1" class="cartao-vidro">
            <h1>Para você... ✨</h1>
            <p>Hoje é um dia especial e eu guardei algumas palavras.</p>
            <p class="aviso-pequeno">Sugestão: coloque fone de ouvido 🎧</p>
            <button id="btn-abrir" class="meu-botao">Abrir Surpresa 💌</button>
        </div>

        <div id="tela2" class="cartao-vidro tela-oculta">
            
            <a href="https://www.youtube.com/watch?v=V141wUSkTfk" target="_blank" class="botao-musica">
                <span class="icone-play">▶️</span> Toque a nossa música aqui
            </a>
            <p class="aviso-pequeno">(Vai abrir no YouTube, deixe tocando e volte pra ler!)</p>

            <div style="margin-top: 20px;">
                <h1>Feliz aniversário 🎂</h1>
                <p>Que esse novo ano venha leve, intenso e cheio de coisas boas. Você merece tudo aquilo que faz o coração sorrir de verdade.</p>
                <p>Tem uma frase do <strong>CBJR'</strong> que me lembra você: <em>“O impossível é só questão de opinião.”</em> Desde que você chegou, muita coisa começou a fazer sentido.</p>
                <span class="destaque-final">Eu te amo menina ❤️</span>
            </div>

        </div>

    </div>
</div>

<script>
    document.addEventListener("DOMContentLoaded", function() {
        var btn = document.getElementById("btn-abrir");
        if(!btn) btn = document.querySelector(".meu-botao");

        if(btn) {
            btn.addEventListener("click", function() {
                document.getElementById("tela1").style.display = "none";
                document.getElementById("tela2").style.display = "block";
            });
        }
    });
</script>
