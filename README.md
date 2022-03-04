# reckdo

<p align="justify">Agora nossa proposta é executar um container e validar que, através da flag -p, é possível acessá-lo diretamente a partir do host. Lembrando que já sabemos como executar containers, porém, devido ao isolamento, ainda não conseguimos validar o funcionamento deles. Vamos fazer essa execução e validação?</p>

<p align="justify">execute o comando <b>docker run -d dockersamples/static-site</b> para que o seu host baixe a imagem e execute o container em seguida.</p>

<p align="justify">A seguir, verifique se o seu container está em execução sem problemas através do comando <b>docker ps ou docker container ls</b>. Repare na coluna PORTS e veja que seu container está informando que possui uma aplicação que pode ser exposta tanto na porta 80 quanto na 443.</p>

<p align="justify">Obtendo esta informação, remova o container recém-criado com o comando <b>docker container rm <id-do-container> -–force</b>.</p>

<p align="justify">Seu objetivo agora será criar um novo container fazendo o devido mapeamento de portas. Para isso, execute o comando <b>docker run -d -p 8080:80 dockersamples/static-site</b>. Repare que através da flag -p, estamos informando que a porta 8080 de nosso host irá refletir na porta 80 do container.</p>

<p align="justify">Por fim, acesse em seu navegador localhost:8080 e veja a aplicação sendo carregada dentro de seu container.</p>
