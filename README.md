# Novo-Futuro
Projeto web site utilizando html/css e javascirpt, para prática de programção.

<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Novo Futuro</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="circulo"></div>

    <img src="./img/logo.png" alt="Logo Novo Futuro" class="Logo" <p></p>

    <div class="conteudo">
        <div class="caixa-texto">
            <h2>É mais que Café, é o <span>Futuro</span></h2>
            <p>O futuro nos aguarda e depende somente de nós. Não deixe para amanhã o que pode ser feito hoje.</p>

            <button>Siga em Frente</button>
        </div>

        <div class="caixa-imagem">
            <img src="./img/img1.png" alt="Copo Novo Futuro" class="copo-grande" </div>
        </div>
    </div>

    <div class="menu">
        <img src="./img/img-pequena1.png" class="copo-pequeno verde">
        <img src="./img/img-pequena2.png" class="copo-pequeno rosa">
        <img src="./img/img-pequena3.png" class="copo-pequeno roxo">
    </div>

</body>
<script>
    let circulo = document.querySelector(".circulo")
    let imgCopo = document.querySelector(".copo-grande")
    let verde = document.querySelector(".verde")
    let rosa = document.querySelector(".rosa")
    let roxo = document.querySelector(".roxo")

    verde.addEventListener("click", () => {
        imgCopo.src = "./img/img1.png"
        circulo.style.background = "#017143"
    })

    rosa.addEventListener("click", () => {
       imgCopo.src = "./img/img2.png"
       circulo.style.background = "#eb7495"
    })

    roxo.addEventListener("click", () => {
       imgCopo.src = "./img/img3.png"
       circulo.style.background = "#d752b1"
    })   

</script>

</html>

CSS

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    padding-top: 20px;
    padding-right: 100px;
    padding-left: 100px;
}

.conteudo {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.caixa-texto {
    width: 600px;
}

.caixa-imagem {
    width: 600px;
    display: flex;
    justify-content: flex-end;
    margin-top: 250px;
}

.menu {
    display: flex;
    justify-content: center;
}

button {
    background-color: #017143;
    color: #ffffff;
    border: none;
    padding: 10px;
    border-radius: 20px;
}

h2 {
    font-size: 50px;
    font-weight: 500px;
}

span {
color: #017143;
font-size: 60px;
font-weight: 900px;
}

p {
    font-size: 18px;
    margin-top: 20px;
    margin-bottom: 30px;
}

.logo {
    width: 80px;
}

.copo-grande {
    width: 300px;
    z-index: 2;
}

.copo-pequeno {
    width: 60px;
    cursor: pointer;
    transition: 1s;
}

.copo-pequeno:hover {
    transform: translateY(-35px);
}

.circulo {
   background: #017143;
   width: 100%;
   height: 100%;
   position: absolute;
   top: 0;
   left: 0;
   clip-path: circle(600px at right 800px);
}
