# 1. Crie um container em modo interativo, sem rodá-lo, nomeando-o como 01container e utilizando a imagem alpine na versão 3.12
## Resolução: 
[Requisito 1](./command01.dc)
<br><br>

# 2. Inicie o container 01container
## Resolução:
[Requisito 2](./command02.dc)
<br><br>

# 3. Liste os containers filtrando pelo nome 01container
## Resolução:
[Requisito 3](./command03.dc)
<br><br>

# 4. Execute o comando cat /etc/os-release no container 01container sem se acoplar a ele
## Resolução:
[Requisito 4](./command04.dc)
<br><br>

# 5. Remova o container 01container
## Resolução:
[Requisito 5](./command05.dc)
<br><br>

# 6. Faça o download da imagem nginx com a versão 1.21.3-alpine sem criar ou rodar um container
## Resolução:
[Requisito 6](./command06.dc)
<br><br>

# 7. Rode um novo container com a imagem nginx com a versão 1.21.3-alpine em segundo plano nomeando-o como 02images e mapeando sua porta padrão de acesso para porta 3000 do sistema hospedeiro
## Resolução:
[Requisito 7](./command07.dc)
<br><br>

# 8. Pare o container 02images que está em andamento
## Resolução:
[Requisito 8](./command08.dc)
<br><br>

# Dockerfile

# 9. Gere uma build a partir do Dockerfile do back-end do todo-app nomeando a imagem para `todobackend`
Escreva no arquivo [command09.dc](./command09.dc) um comando que fará o build de uma imagem a partir do arquivo Dockerfile, esta imagem deve ter o nome `todobackend`.

No arquivo Dockerfile escreva os comandos que farão com que a imagem:

<ul>
<li> Rode a partir da imagem do node na versão 14;
exponha a porta 3001; </li>
<li> Defina o diretório de trabalho para /app/back-end; </li>
<li> Adicione o arquivo node_modules.tar.gz à imagem;</li>
<li> Copie todos os arquivos da pasta back-end para a imagem;</li>
<li> Inicie a aplicação com o comando npm start respeitando as seguintes restrições:</li>
<ol>
<li> Ao subir um container baseado na imagem buildada a partir desse Dockerfile, o comando npm deve ser rodado sempre;</li>
<li> Ao subir um container baseado na imagem buildada a partir desse Dockerfile, deve ser possível sobrescrever o comando start.</li>
</ul>

## Resolução: 
[Comando Docker](./command09.dc);<br>
[Configuração do Dockerfile](../todo-app/back-end/Dockerfile).
<br><br>

# 10. Gere uma build a partir do Dockerfile do front-end do todo-app nomeando a imagem para `todofrontend`
Escreva no arquivo [command10.dc](./command10.dc) um comando que fará o build de uma imagem a partir do arquivo Dcokerfile, esta imagem deve ter o nome `todofrontend`.

No arquivo Dockerfile escreva os comandos que farão com que a imagem:

<ul>
<li> Rode a partir da imagem do node na versão 14;
<li> Exponha a porta 3000;
<li> Defina o diretório de trabalho para /app/front-end
<li> Adicione o arquivo node_modules.tar.gz à imagem;
<li> Copie todos os arquivos da pasta front-end para a imagem;
<li> Inicie a aplicação com o comando npm start respeitando as seguintes restrições:
<ol>
<li> Ao subir um container baseado na imagem buildada a partir desse Dockerfile, o comando npm deve ser rodado sempre;
<li> Ao subir um container baseado na imagem buildada a partir desse Dockerfile, deve ser possível sobrescrever o comando start.
</ol>
</ul>

## Resolução: 
[Comando Docker](./command10.dc);<br>
[Configuração do Dockerfile](../todo-app/front-end/Dockerfile).
<br><br>

# 11. Gere uma build a partir do Dockerfile dos testes do todo-app nomeando a imagem para `todotests`
Escreva no arquivo [command11.dc](./command11.dc) um comando que fará o build de uma imagem a partir do arquivo Dockerfile, esta imagem deve ter o nome `todotests`.

No arquivo Dockerfile escreva os comandos que farão com que a imagem:

<ul>
<li> Rode a partir da imagem do betrybe/puppetter:1.0;
<li> Defina o diretório de trabalho para /app/tests;
<li> Adicione o arquivo node_modules.tar.gz à imagem;
<li> Copie todos os arquivos da pasta tests para a imagem.
<li> Iinicie a aplicação com o comando npm test respeitando as seguintes restrições:
<ol>
<li> Ao subir um container baseado na imagem buildada a partir desse Dockerfile, o comando npm deve ser rodado sempre;
<li> Ao subir um container baseado na imagem buildada a partir desse Dockerfile, deve ser possível sobrescrever o comando test.
</ol>
</ul>

## Resolução: 
[Comando Docker](./command11.dc);<br>
[Configuração do Dockerfile](../todo-app/tests/Dockerfile).
<br><br>