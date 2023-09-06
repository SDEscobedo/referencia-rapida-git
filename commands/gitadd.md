# GIT ADD - O QUE É? PARA QUE SERVE?
## Leia esse documento e entenda todos os conceitos, funcionamentos e utilizações do **GIT ADD**

Dentro do sistema de controle de versionamento _git_, o comando **git add** é de suma importância e parte fundamental nesse processo.

O **GIT ADD** é parte fundamental na preparação, identificação e rastreamento das alterações feitas antes de efetuar um **commit**. Ainda está com dúvidas? Aqui está mais uma breve definição e, posteriormente, exemplos de quando usar, como utilizar e porque utilizar:<br>
**Ele é usado para selecionar arquivos e/ou alterações específicas em seu diretório de trabalho e prepará-los para serem registrados em um commit.**

**Quando utilizar?**<br><br><br>
- O objetivo principal do comando `git add` é incluir ou “encenar” as mudanças feitas nos arquivos para o “stage” do Git. O stage é uma área intermediária onde você coloca as mudanças que deseja incluir no próximo commit. Isso permite selecionar quais mudanças específicas deseja gravar, em vez de cometer todas as alterações no diretório de trabalho de uma só vez;

- Além de incluir arquivos inteiros no estágio, é possível utilizar o comando git add para selecionar partes específicas de um arquivo. Essa prática é conhecida como “hunk staging” e é útil quando você fez várias alterações em um arquivo, mas deseja realizar o commit apenas de algumas delas: 
```
git add -p
```
ou
```
git add --patch
```

- Se por acaso você adicionou um arquivo ou fez uma alteração ao _stage_ e deseja desfazer isso, você pode utilizar o comando __git reset__ para remover os arquivos do stage sem perder as alterações no seu diretório de trabalho.<br>
Mas esse tema com o comando "git reset" deixemos para outro documento, o nosso foco, neste momento, é o aprendizado do comando **git add**.

- A função do comando **git add** é possibilitar que você faça commits em etapas separadas, o que é conveniente quando você deseja dividir suas alterações em commits menores e mais claros.

- O comando **git add** é uma etapa crucial no fluxo de trabalho do Git, pois permite que você gerencie quais alterações são incluídas em um commit. Ao utilizá-lo de forma eficaz, você pode criar commits bem estruturados e detalhados, o que é fundamental para ter um histórico de projeto claro e compreensível.

# SINTAXE BÁSICA

```
git add <nome-do-arquivo>   -> Adiciona um arquivo específico ao stage
```
```
git add .  -> Adiciona todas as alterações no diretório atual
```


