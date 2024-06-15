# shrinkURL

Encurtador de URLs
Seu serviço irá receber inicialmente como parâmetro uma URL que deverá ser encurtada seguindo as seguintes regras:

Mínimo de 5 e máximo de 10 caracteres.

Apenas letras e números.

A url retornada deverá ser salva no banco de dados e possui prazo de validade (você poderá escolher quanto tempo) e ao receber uma url encurtada, deverá fazer o redirecionamento para a url salva no banco.

Exemplo ao encurtar
Seu sistema recebe uma chamada para encurtar a url backendbrasil.com.br e retorna o seguinte json:
```
{ 
  newUrl: "http://localhost:8081/abc123ab";
} 
```

Exemplo ao redirecionar
Ao receber uma chamada para http://localhost:8081/abc123ab você irá retorna um redirecionamento para a url salva no banco (backendbrasil.com.br), caso não seja encontrada, retornar HTTP 404

Evolução 2:

Além de receber uma URL, iremos utilizar IA para sugerir links cujo conteúdo seja parecido com o do link a ser encurtado.

Por exemplo, caso o link seja: https://ge.globo.com/
Retornar como sugestão links com sites de esporte, como por exemplo: https://www.espn.com.br/
