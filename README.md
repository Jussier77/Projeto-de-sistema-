# Projeto-de-sistema-
Vídeo explicativo e código: https://drive.google.com/file/d/1oZWjXmvqrfkfbYfA7BTGqWxe0g7-2mM3/view?usp=sharing
# Parte do html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/index.CSS">
    <title>Assistente de segurança</title>
</head>
<body>
    
        <div class="container">
        <h1>Assistente de Segurança</h1>
        <p>Escolha seu nivel de segurança desejado</p>
        <div class="labels">
        
            <p><input id="baixa" type="radio" name="nivelSegurança" value="baixa" > Baixa</p>
                
            <p><input id="media" type="radio" name="nivelSegurança" value="média"> Média</p>
    
            <p><input id="alta" type="radio" name="nivelSegurança" value="alta"> Alta</p>
                
            
        </div>
       
        <button onclick="verificarResposta()" id="verificarSegurança">Vamos verificar?</button>
        <p id="resultado">Marque alguma opção!</p>
        <img src="img/importante.jpg" alt="fundo de site" class="imagem">
    </div>
    

    <script src="js/index.JS"></script>
</body>
</html>
#Parte do css
@import url('Spartanhttps://fonts.googleapis.com/css2?family=League+Spartan:wght@600&display=swap');

*{
    margin: 0;
    padding: 0;
    font-family: 'League ', sans-serif;
    font-display: initial;
    font-stretch: condensed;
    font-variant: unset;
}
.imagem{
    width: 0px;
    height: auto;
    margin: 0px;
       
}
body{
    background-image: url(../img/importante.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    

}
h1, p, label, button {
    text-align: center;
    
    margin: 10px;
}

.container h1{
    font-size: 45px;

}

.container p{
    font-size: 22px;

}

.labels{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
    width: 100%;
}

#verificarSegurança{
    width: 200px;
    height: 50px;
    font-size: 22px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
}

#verificarSegurança:hover{
    background-color: rgb(219, 219, 219);
}

.container{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    min-height: 100vh;
    color: rgb(255, 255, 255);
}
#Parte do js
var inputBaixa = document.querySelector("#baixa");
var inputMedia = document.querySelector("#media");
var inputAlta = document.querySelector("#alta");
var resultado = document.querySelector("#resultado");

function verificarResposta(){
       if(inputBaixa.checked){
              resultado.textContent = "Sugerimos que reforce suas fechaduras."
       } else if(inputMedia.checked){
              resultado.textContent = "Sugerimos que reforce suas fechaduras e coloque um cão de guarda."
       } else if(inputAlta.checked){
              resultado.textContent = "Sugerimos que reforce suas fechaduras, coloque um cão de guarda, instale cerca elétrica integrada a sensores de presença e reconhecimento facial, bem como alarmes. Por útimo, abuse de câmeras com monitoramento 24 horas."
       } else{
              resultado.textContent = "Nenhuma opção foi marcada"
       }
}
