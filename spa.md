# O que é SPA?

## Modelo tradicional (server-side)

- Cliente = browser
- Server = host da aplicação (internet/nuvem)

- O client faz o request inicial (por exemplo, ao digitar a URL do site, o usuário está pedindo que o site descarregue no browser)
- O server processa esse request, trabalha no que for necessário, forma um HTML completo (que já inclui referências JS, CSS etc) e devolve esse documento HTML completo
- O client, então, interpreta no browser e a página é exibida
- Caso o usuário faça um cadastro, ou um login, por exemplo, submetendo um formulário (form post); esse formulário é um POST com alguns dados que vai ser processado pelo server; nesse caso, ao fazer login, o server tem que mostrar uma outra tela, então ele vai processar essa outra tela, formar todo o HTML dessa tela e devolver, novamente, o HTML formado

- Sempre que o client faz uma requisição, esperamos o server trabalhar, formar todo o HTML e devolver o documento completo
- Toda vez que recebe um retorno, a página recarrega
- Mais pesado, mais lento

## Single Page Aplication (SPA)

- O client faz um request inicial para uma aplicação hospedada no server
- O server retorna um HTML mas, dessa vez, esse HTML é um arquivo que já está hospedado no servidor, não é processado na hora
- Esse documento HTML já contém as referências aos scripts 
- Ao fazer um POST - submeter um formulário de forma assíncrona ao sevidor -, o server vai trabalhar essa requisição e retornar um JSON
- O documento HTML não é devolvido pelo server porque ele já está no client; quando você faz a requisição pela primeira vez, você recebe basicamente a aplicação inteira e, depois disso, a comunicação é feita via JSON

- O arquivo JSON é muito mais leve, tornando a aplicação mais rápida
- Com o SPA, recebemos uma vez só do server um arquivo HTML e esse arquivo já contém os scripts JS necessários
- Esse script se comunica com o servidor de forma síncrona solicitando apenas as informações que ele precisa exibir na tela