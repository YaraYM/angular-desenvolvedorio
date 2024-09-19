# O que � SPA?

## Modelo tradicional (server-side)

- Cliente = browser
- Server = host da aplica��o (internet/nuvem)

- O client faz o request inicial (por exemplo, ao digitar a URL do site, o usu�rio est� pedindo que o site descarregue no browser)
- O server processa esse request, trabalha no que for necess�rio, forma um HTML completo (que j� inclui refer�ncias JS, CSS etc) e devolve esse documento HTML completo
- O client, ent�o, interpreta no browser e a p�gina � exibida
- Caso o usu�rio fa�a um cadastro, ou um login, por exemplo, submetendo um formul�rio (form post); esse formul�rio � um POST com alguns dados que vai ser processado pelo server; nesse caso, ao fazer login, o server tem que mostrar uma outra tela, ent�o ele vai processar essa outra tela, formar todo o HTML dessa tela e devolver, novamente, o HTML formado

- Sempre que o client faz uma requisi��o, esperamos o server trabalhar, formar todo o HTML e devolver o documento completo
- Toda vez que recebe um retorno, a p�gina recarrega
- Mais pesado, mais lento

## Single Page Aplication (SPA)

- O client faz um request inicial para uma aplica��o hospedada no server
- O server retorna um HTML mas, dessa vez, esse HTML � um arquivo que j� est� hospedado no servidor, n�o � processado na hora
- Esse documento HTML j� cont�m as refer�ncias aos scripts 
- Ao fazer um POST - submeter um formul�rio de forma ass�ncrona ao sevidor -, o server vai trabalhar essa requisi��o e retornar um JSON
- O documento HTML n�o � devolvido pelo server porque ele j� est� no client; quando voc� faz a requisi��o pela primeira vez, voc� recebe basicamente a aplica��o inteira e, depois disso, a comunica��o � feita via JSON

- O arquivo JSON � muito mais leve, tornando a aplica��o mais r�pida
- Com o SPA, recebemos uma vez s� do server um arquivo HTML e esse arquivo j� cont�m os scripts JS necess�rios
- Esse script se comunica com o servidor de forma s�ncrona solicitando apenas as informa��es que ele precisa exibir na tela