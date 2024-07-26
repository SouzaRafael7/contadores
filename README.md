# validacoes
site de validação de cpf e outro de email onde cada um tem seus códigos para serem verificados.

* [Cpf](#cpf)
* [Código Cpf](#codigo-utilizado)
* [Email](#email)
* [Codigo Email](#codigo-email)
* [Tecnologias utilizadas](#tecnologias-utilizadas)
* [Autores](#autores)

## Cpf

No site o usuário digita um cpf, o código analisa o cpf e logo abaixo deixa sua resposta se o cpf é valido ou invalido. 

![Site](vdi/cpf-contador.gif)

## Código cpf

O site analisa se o código tem algum erro, como por exemplo:

**if(cpf.length !== 11 || /^(\d)\1{10}$/.test(cpf))**: 
Ele analisa se todos os números são iguais.

**function validarCPF(cpf)**:
Define a função validarCPF que recebe o número de CPF como parâmetro.

**cpf = cpf.replace(/[^\d]+/g, '')**:
Remove todos os caracteres que não são dígitos do número de CPF.

**if(validarCPF(cpf))**:
Chama a função validarCPF passando o valor do CPF. Se a função retornar true, o CPF é válido e a mensagem é alterada para "O CPF é válido" com a cor verde.

**else** :
Se a função validarCPF retornar false, o CPF é inválido e a mensagem é alterada para "O CPF é inválido" com a cor vermelha.

**const msg = document.getElementById('message')**: Obtém a referência ao elemento HTML com o ID 'message', que será usado para exibir a mensagem de validação.

**const cpf = document.getElementById('cpf').value**: Obtém o valor do campo de entrada com o ID 'cpf' e armazena em uma constante chamada 'cpf'.

**event.preventDefault()**: Essa linha impede o comportamento padrão do formulário, que seria recarregar a página. Isso é útil para realizar a validação antes de enviar os dados para um servidor, por exemplo.

**document.getElementById('cpfForm').addEventListener('submit', ...)** :Essa linha adiciona um ouvinte de eventos ao formulário com o ID 'cpfForm'. Isso significa que quando o formulário for enviado (clicando no botão "Enviar"), a função dentro do addEventListener será executada.

**for(let i=1;i <= 9;i++)**: Este é um loop que itera de 1 a 9. A variável i será usada como índice para acessar os dígitos do CPF.

**parseInt(...)**: Converte o dígito extraído para um número inteiro.

**substring()** é uma ferramenta poderosa para trabalhar com strings em JavaScript. Ele permite que você extraia partes específicas de uma string de forma fácil e eficiente, o que é fundamental em muitas aplicações de desenvolvimento web.

## Email ##
Neste site o usuário digita um email válido, o código verifica se o email está correto ou incorreto e logo se estiver correto, o email aparece abaixo.

![Site](vdi/email-validador.gif)

## Codigo Email

**document.forms[0].email.value**: Acessa o valor do campo de email no primeiro formulário do documento.
== "": Verifica se o campo de email está vazio.
**indexOf('@') == -1**: Verifica se o caractere '@' não existe no endereço de email (indexOf retorna -1 se não encontrar).
**indexOf('.') == -1**: Verifica se o caractere '.' não existe no endereço de email.
if: Se qualquer uma dessas condições for verdadeira, o email é inválido.

**alert("Por favor, informe um e-mail válido")**: Exibe uma mensagem de alerta informando que o email é inválido.
**return false;**: Retorna false para indicar que a validação falhou.

**else**: Se todas as condições do if forem falsas, o email é considerado válido.

**alert("Email informado")**: Exibe uma mensagem de alerta informando que o email foi informado.

**document.getElementById('email').innerHTML = document.forms[0].email.value**: Atribui o valor do campo de email ao elemento HTML com o ID 'email'. Isso provavelmente é para exibir o email em algum lugar da página.

## Tecnologias Utilizadas
* [<code><img height="32" src="https://raw.githubusercontent.com/github/explore/80688e429a7d4ef2fca1e82350fe8e3517d3494d/topics/html/html.png" alt="HTML5"/></code>](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
* [<code><img height="32" src="https://blog.netscandigital.com/wp-content/uploads/2023/07/O-que-e-o-Google-Bard.png" alt="Bard"/></code>](https://bard.google.com/chat?hl=pt)
* [<code><img height="32" src="https://img.shields.io/badge/VSCode-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" alt="VisualStudio"/></code>](https://code.visualstudio.com/)
* [<code><img height="32" src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></code>](https://github.com/)
* [<code><img height="32" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/1200px-CSS3_logo_and_wordmark.svg.png" alt="Css3"/></code>](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
* [<code><img height="32" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/1200px-Unofficial_JavaScript_logo_2.svg.png" alt="javascript"/></code>](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)

## Autores
* ``Aluno 2ºC:``Rafael Souza Mastellini