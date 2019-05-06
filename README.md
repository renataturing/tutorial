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

Se aparecer a versão do git, ou uma lista com os comandos que podem ser usados, o git está instalado no seu computador normalmente.  

Para começar a usar o git, vamos baixar os arquivos para fazer algusn testes.  
Abra a linha de comando e digite:  

```console
$ git clone https://github.com/renataturing/tutorial.git
```
Para checar em qual branch você está, digite:

```console
$ git checkout
```

Isso irá retornar os arquivos estão presentes nesse branch.
Por examplo:

```console
M	tutorial.py
Your branch is up to date with 'origin/master'.
```

Isso quer dizer que no *branch* **master** (M) há o arquivo **tutorial.py**.

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
Vamos agora fazer uma alteração no código que está no arquivo tutorial.py.  
- Abra o arquivo em algum editor de texto,
- Escreva 
```python
print("*seu nome*")
```




