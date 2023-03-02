[Voltar](/README.md)

# Cronograma do Workshop

## Criando um repositório no GitHub

No GitHub, a partir do menu superior direito, clicar no sinal de “+”, depois em **“New Repository”**

![Untitled](img/Untitled.png)

Na tela de repositório, dar ao repositório o mesmo nome do seu perfil no GitHub e marcar  **“Add a README file”**:

![Untitled](img/Untitled%201.png)

No repositório, clicar no botão “<> Code”, depois na aba “Local”, depois “HTTPS” e copiar o endereço:

![Untitled](img/Untitled%202.png)

## Clonando o repositório localmente

Abrir o terminal do Windows (Windows + R, “cmd”), digitar “git” para se certificar que o git está instalado na máquina. Deve aparecer algo como a imagem abaixo:

![Untitled](img/Untitled%203.png)

No terminal, navegar até a pasta `c:\` com o comando `cd c:\`:

![Untitled](img/Untitled%204.png)

Neste local, criar uma pasta chamada `repos` com o comando `mkdir repos` e entrar nesta pasta com `cd repos`

![Untitled](img/Untitled%205.png)

Nesta pasta, escrever `git clone` concatenando o endereço do repositório do GitHub copiado anteriormente. Algo semelhante a imagem abaixo será mostrado:

![Untitled](img/Untitled%206.png)

Navegue até o repositório recém baixado com o comando `cd <nome_do_repositório>`a,no caso so exemplo `cd abc123`:

![Untitled](img/Untitled%207.png)

## Utilizando o VS Code para editar o arquivo Readme.md

Se o VS Code estiver instalado na máquina, digite `code .` e pressione Enter. O VS Code deve abrir a pasta(repositório) atual. Caso uma mensagem seja exibida sobre confiar nos autores da pasta, confirme:

![Untitled](img/Untitled%208.png)

Abrir o arquivo `README.md` a partir da barra lateral:

![Untitled](img/Untitled%209.png)

Entrar no seguinte endereço do GitHub Gists: [https://gist.github.com/thcerutti/540fd54b51307062366665e2c51a8038](https://gist.github.com/thcerutti/540fd54b51307062366665e2c51a8038)

![Untitled](img/Untitled%2010.png)

Clicar no botão “Raw” copiar todo o texto:

![Untitled](img/Untitled%2011.png)

Colar no arquivo `README.md` que está aberto no VS Code e salvar:

![Untitled](img/Untitled%2012.png)

Vamos fazer o commit primeiramente pelo terminal para aprender via linha de comando, sempre ficando de olho na aba de controle de versão (segundo ícone, lado esquerdo).

![Untitled](img/Untitled%2013.png)

## Adicionando arquivos no `git`

Primeiramente precisamos falar pro git quais arquivos serão incluídos no nosso primeiro commit. No nosso caso vamos adicionar todos (no caso “todos” resume-se a 1 arquivo, o README.md). Para isso vamos executar o comando `git add --all`

![Untitled](img/Untitled%2014.png)

## Mandando alterações para `git`

Depois disso o arquivo que aparecia como “Changes” agora aparece como “Staged Changes”. A área de staging é a nossa área intermediária que identifica o que queremos adicionar ao commit. Com nosso arquivo identificado, vamos criar nosso primeiro commit com o comando

`git commit -m "adiciona modelo de perfil"`

![Untitled](img/Untitled%2015.png)

Perceba que nosso arquivo foi commitado localmente, o que significa que o GIT está monitorando as alterações que fizemos até o momento. Agora precisamos enviar para o GitHub e para isso precisamos informar o GIT que queremos fazer um push, ou seja, queremos “empurrar” o código para o GitHub, identificando a nossa branch local como sendo a branch main do GitHub. Para isso rodamos o comando

`git push -u origin main`

Mas quando fazemos isso o git fala que precisa autenticar no GitHub para enviarmos o código. Aqui selecionamos a opção de autenticar pelo browser, então podemos informar “’1” ou simplesmente dar um Enter para que ele assuma este método de autenticação:

![Untitled](img/Untitled%2016.png)

Uma janela do navegador será aberta e se você já estiver logado no GitHub, a autenticação será automática e uma janela como a abaixo será mostrada:

![Untitled](img/Untitled%2017.png)

De volta para o VS Code, o terminal mostra que o commit deu certo:

![Untitled](img/Untitled%2018.png)

Agora já podemos verificar o nosso repositório no GitHub, que já deve ter o código atualizado:

![Untitled](img/Untitled%2019.png)

## Trabalhando com branches

Agora vamos abrir uma branch nova para fazer algumas alterações no arquivo e treinar o fluxo de Pull Requests. No VS Code podemos ver que estamos na branch principal do projeto, chamada de “main”. Vamos criar uma branch a partir dela com o seguinte comando

`git checkout -b atualiza-perfil`

![Untitled](img/Untitled%2020.png)

Perceba que no canto inferir esquerdo já aparece o nome da nossa nova branch

![Untitled](img/Untitled%2021.png)

Vamos alterar o arquivo `README.md` com as nossas informações pessoais. Depois de alterarmos o arquivo, podemos ver o que foi alterado com o comando `git diff` no terminal, que deve gerar algo parecido com isso:

![Untitled](img/Untitled%2022.png)

Para sair do modo de visualização de diferenças, pressionamos `q` (quit). Agora precisamos adicionar os arquivos alterados, mas agora faremos isso pela barra lateral, clicando no sinal de “+” ao lado do arquivo, mandando ele para a área de staging:

![Untitled](img/Untitled%2023.png)

Escrevemos uma mensagem de commit, neste caso pode ser “Dados pessoais preenchidos”, e clicamos no botão “Commit”

![Untitled](img/Untitled%2024.png)

## Mandando a branch pro GitHub e abrindo um Pull Request

Agora precisamos publicar a branch, clicando no botão “Publish Branch”. Pronto, as alterações agora já estão no GitHub separadas em uma branch separada. Quando visualizamos a página do projeto no GitHub nos é mostrada a seguinte mensagem:

![Untitled](img/Untitled%2025.png)

As nossas alterações estão em uma “linha do tempo” paralela, e isso é útil para fazermos alterações e revisar essas informações antes de o código ir para “produção”. Vamos clicar no botão “Compare & pull request”. Aqui podemos escrever uma mensagem descrevendo o que fizemos, analisar as diferenças de código e criar o pull request para que alguém revise (fluxo real das empresas)

![Untitled](img/Untitled%2026.png)

Ao clicar no botão “Create pull request” somos levados à página de pull requests, onde vamos revisar as alterações feitas, e se estiver tudo ok vamos clicar no botão “Merge pull request”

![Untitled](img/Untitled%2027.png)

Caso esta informação seja mostrada, clique no botão “Confirm Merge”

![Untitled](img/Untitled%2028.png)

Pronto! Agora que o Pull Request (PR) foi mergeado (mesclado) com a branch principal (main), já podemos apagar esta branch na qual fizemos as alterações (não obrigatório), clicando no botão “delete branch”

![Untitled](img/Untitled%2029.png)

Agora no VS Code, vamos alternar para a branch principal (main) e baixar as alterações que acabamos de fazer com o comando

`git checkout main` para retornarmos para nossa branch principal

`git pull` para baixarmos as últimas alterações

![Untitled](img/Untitled%2030.png)

Pronto! Agora a sua branch principal está atualizada com todas as alterações feitas.
