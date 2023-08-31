# Fazer commit e revisar as alterações no seu projeto no GitHub Desktop

### À medida que você edita os arquivos, o GitHub Desktop monitora todas as alterações feitas. É possível decidir como você pretende agrupar as alterações para criar commits relevantes.

## Sobre commits
Assim como ao salvar um arquivo que foi editado, um commit registra alterações em um ou mais arquivos no seu branch. O Git atribui a cada commit um ID exclusivo, denominado SHA ou hash, que identifica:

+ Cada uma das alterações feitas;
+ O momento em que as alterações foram feitas;
+ O autor das alterações.

Ao fazer um commit, você deve incluir uma mensagem que descreva brevemente as alterações. Você também pode adicionar um coautor em qualquer commit em que colaborar.

Se os commits que você cria em GitHub Desktop estiverem associados à conta errada no GitHub, atualize o endereço de e-mail na configuração do Git usando GitHub Desktop. Para obter mais informações, confira [Configurar o Git para o GitHub Desktop](https://docs.github.com/pt/desktop/installing-and-configuring-github-desktop/configuring-and-customizing-github-desktop/configuring-git-for-github-desktop)

### Comandos: 

### Comando para comentar apenas:
``` 
git commit -m "Descrição desejada"
```

### Comando para adicionar e comentar:
```
git commit -a -m "Descrição desejada"
```