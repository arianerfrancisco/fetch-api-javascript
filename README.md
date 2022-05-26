# A API Fetch

Fornece uma interface JavaScript para acessar e manipular partes do pipeline HTTP, tais como os pedidos e respostas. 
Ela também fornece o método global fetch() (en-US) que fornece uma maneira fácil e lógica para buscar recursos de forma assíncrona através da rede.

Este tipo de funcionalidade era obtida anteriormente utilizando XMLHttpRequest. 
Fetch fornece uma alternativa melhor que pode ser facilmente utilizada por outras tecnologias como Service Workers (en-US). 
Fetch também provê um lugar lógico único para definir outros conceitos relacionados ao protocolo HTTP como CORS e extensões ao HTTP.

Note que a especificação fetch() difere de jQuery.ajax(), principalmente, de três formas:

A Promise retornada do fetch() não rejeitará o status do erro HTTP, mesmo que a resposta seja um HTTP 404 ou 500.
Em vez disso, ela irá resolver normalmente (com o status ok definido como falso), e só irá rejeitar se houver falha na rede ou se algo impedir a requisição de ser completada.
fetch() não receberá cookies cross-site; você não pode estabelecer uma conexão cross-site usando fetch. 

Cabeçalhos Set-Cookie de outros sites são ignorados silenciosamente.
fetch() não enviará cookies, a não ser que seja definida a opção credentials do parâmetro init. 