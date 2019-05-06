### Tutorial

Esse é um **tutorial** de como usar o GitHub!  

Para isso, vamos utilizar documentos simples como exemplos para o que vamos fazer.
Primeiramente, você deve ter o git instalado no seu computador. 

Para checar se você instalou corretamente, digite

```console
$ git --version
```

ou  

```console
$ git --help
```  

Se aparecer a versão do git, ou uma lista com os comandos que podem ser usados, o git está instalado no seu computador.

Para começar a usar o git, vamos baixar os arquivos para fazer alguns testes.  
Abra a linha de comando e digite:  

```console
$ git clone https://github.com/renataturing/tutorial.git
```
Agora, digite 

```console
$ git chekout
```

Isso irá retornar os arquivos estão presentes nesse branch, e se ele está atualizado ou não.
Por examplo:

```console
M	tutorial.py
Your branch is up to date with 'origin/master'.
```

Isso quer dizer que no *branch* há o arquivo **tutorial.py**.

Para criar um novo branch, e entrar nele, digite:

```console
$ git checkout -b *um nome qualquer*
```
Se você digitar o comando

```console
$ git branch
```
ele irá retornar em qual branch você está - o que é importante para saber em **qual branch você está realizando as alterações**. Por exemplo:

```console
$ git branch
  alteracaoRenata
* master
```

O nome que aparece com um * do lado é o nome do branch em que você está. Nesse caso, você está no master. Eu criei um outro branch chamado *alteracaoRenata*, por isso aparecem os dois. Agora vou retornar para o branch *alteracaoRenata*.

```console
$ git checkout alteracaoRenata
```

Escrevendo de novo o comando 

```console
$ git branch
* alteracaoRenata
  master
```

ele vai me informar que estou no branch alteracaoRenata.  

Se eu usar o comando *--remote*, ele vai me retornar quais são os branchs na origem.
 
 ```console
$ git branch --remote
  origin/HEAD -> origin/master
  origin/master
```

Vamos agora fazer uma alteração no código que está no arquivo tutorial.py. Para isso:  
- Abra o arquivo em algum editor de texto,
- Escreva 
```python
print("*seu nome*")
```
Agora vamos colocar esse arquivo nessa nova branch:
- Volte para a linha de comando,
- Digite
```console
$ git commit .
```

Isso vai mandar o arquivo para o novo branch que você fez.

Se você digitar *git checkout* vai ver quais são as diferenças que ocorreram após você alterar os arquivos, por exemplo:
```console
$ git checkout
Your branch and 'origin/master' have diverged,
and have 1 and 7 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)
```

Para mandar o arquivo e criar um pull request, digite:

```console
$ git push origin *nome do seu branch*
```

Isso vai retornar a seguinte mensagem:

```console
Username for 'https://github.com': *seu nome de usuário*
Password for 'https://*seu nome de usuário*@github.com': 
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for '*seu branch*' on GitHub by visiting:
remote:      https://github.com/renataturing/tutorial/pull/new/*seu branch*
remote: 
To https://github.com/renataturing/tutorial.git
 * [new branch]     *seu branch* -> *seu branch*
```
A partir desse link, você pode criar um pull request para o dono do repositório:

![Pull Request](/Pictures/tutorial1.png)














