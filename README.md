Alura_Logica2
=============
<meta charset = "UTF-8">
<html>

	<canvas id="tela" width="600" height="400"></canvas>
	<script>
		
		var tela = document.getElementById("tela");
		var c = tela.getContext("2d");
		var imagem = new Image();
		imagem.src = "anjinho.gif"
		
		c.fillStyle = "gray";
		c.fillRect(0,0,600,400);
		
		var desenhaImagem = function(x, y){
			c.drawImage(imagem, x, y);
					
		}
		
		var limpaTela = function(){
			
			c.clearRect(0,0,600,400);
		
		}
		var x = 0;
		var animacao = function(){
			limpaTela();
			desenhaImagem(x,100);
			x = x + 1;
		}
		
		setInterval(animacao, 30);
		
	</script>
</html>
