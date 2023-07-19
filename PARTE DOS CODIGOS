# parte dos codigos 

<!DOCTYPE html>
<html>
      <head>
        <title> rafael na programacao </title>
        </head>
<body>
            <Iabel for="nota1"> nota 1:</Iabel>
            <input type="text" id="nota1"/>

            <label for="nota2"> nota 2:</label>
            <input type="text" id="nota2"/>

            <label for="nota3"> nota 3:</label>
            <input type="text" id="nota3"/>

            <label for="nota4"> nota 4:</label>
            <input type="text" id="nota4"/>
            <button type="button" onclick="calcularMedia()">calcular média</button>

            <p id="resultado">0</p>
</body>
	
        <script>
        
           function  calcularMedia() {
             var nota1 = parseFloat(document.getElementById('nota1').value)
             var nota2 = parseFloat(document.getElementById('nota2').value)
             var nota3 = parseFloat(document.getElementById('nota3').value)
             var nota4 = parseFloat(document.getElementById('nota4').value)

             var media = (nota1+nota2+nota3+nota4) / 4

             var resultado = document.getElementById('resultado')

          	 resultado.innerHTML = media	
		
	
	}
	
	</script>
	 
</html>


# FIM


# projeto que calcula media ponderada codigo abaixo influindo o codigo.js e o "media.html".


codigo.js

function doGet() {
  return HtmlService.createHtmlOutputFromFile('Media')
}
  function calcularMedia(nota1, peso1, nota2, peso2){
  var media = ( (nota1*peso1) + (nota2*peso2) ) / (peso1+peso2);
return media;
}

media.html

<!DOCTYPE html>
<html>
  <head>
    <base target="_top">
</head>
<body>
  <h1>Página que calcula média ponderada</h1>

  <label for="nota1">Nota 1:</label>
  <input type="number" id="nota1">

  <label for="peso1">Peso 1:</label>
  <input type="number" id="peso1">

  <label for="nota2">Nota 2:</label>
  <input type="number" id="nota2">

  <label for="peso2">Peso 2:</label>
  <input type="number" id="peso2">

  <button onclick="calcularMedia()">Calcular média</button> </br>
<div>
  <p>Resultado:</p>
  <p id="resultadoMedia"></p>
</div>
<script>
  function calcularMedia(){
    var nota1 = parseFloat(document.getElementById('nota1').value);
    var peso1 = parseFloat(document.getElementById('peso1').value);
    var nota2 = parseFloat(document.getElementById('nota2').value);
    var peso2 = parseFloat(document.getElementById('peso2').value);

    google.script.run.withSuccessHandler(exibirMedia).calcularMedia(nota1, peso1, nota2,
peso2);
  }
  function exibirMedia(media){
    var resultadoMedia = document.getElementById('resultadoMedia');
    resultadoMedia.innerHTML = media;
  }
</script>
</body>
</html>

# FIM



# Projeto com login com email e senha codigo abaixo influindo o codigo.js e o "index.html".


codigo.js

function doGet() {
  return HtmlService.createHtmlOutputFromFile('index');
}

function verificarCredenciais(email, senha) {
  var emailCorreto = 'aluno@ceep.com';
  var senhaCorreta = 'alunoceep2023';
  
  if (email === emailCorreto && senha === senhaCorreta) {
    return 'Login bem-sucedido';
  } else {
    return 'Login falhou';
  }
}

index.html

<!DOCTYPE html>
<html>
  <head>
    <base target="_top">
  </head>
  <body>
    <h1>Login</h1>
    <form onsubmit="event.preventDefault(); verificarLogin();">
      <label for="email">E-mail:</label>
      <input type="email" id="email" required><br>
      <label for="senha">Senha:</label>
      <input type="password" id="senha" required><br>
      <input type="submit" value="Login">
    </form>
    <p id="resultado"></p>
    
    <script>
      function verificarLogin() {
        var email = document.getElementById('email').value;
        var senha = document.getElementById('senha').value;
        
        google.script.run.withSuccessHandler(exibirResultado).verificarCredenciais(email, senha);
      }
      
      function exibirResultado(resultado) {
        document.getElementById('resultado').textContent = resultado;
      }
    </script>
  </body>
</html>

# FIM


# projeto que inviar dados ao servidor codigo abaixo influindo o codigo.js e o "formulario.html".

codigo.js


function doGet() {
  return HtmlService.createTemplateFromFile('formulario').evaluate();
}

function doPost(e){

  Logger.log(e.parameter.msg)
  Logger.log(e.parameter.endereco)
}

function getUrl(){
  var url = ScriptApp.getService().getUrl();
  return url
}


formulario.html


<!DOCTYPE html>
<html>
  <head>
    <base target="_top">
  </head>
  <body>
    
    <? var url = getUrl() ?>

    <form action="<?= url ?>" method="POST">
      <label for="msg">Mensagem</label>
      <input type="text" id="text" name="msg">

      <label for="endereco">Endereço</label>
      <input type="text" id="endereco" name="endereco">
      <button type="submit">Enviar</button>
    </form>
  </body>
</html>


#FIM

