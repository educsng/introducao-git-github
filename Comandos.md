# Lista de comandos básicos



## Criando Repositório local

1. Comando `git init` no diretório desejado ou passando novo diretório

   `git init`

   ou

   `git init <nomedorepositorio>`



## Ciclo de vida dos arquivos

1. Coloca os arquivos modificados para o status staged:

   ```git add <nomedoarquivo>```

2. Efetua o commit com as mudanças realizadas. Pode-se passar uma mensagem ou não.

   ```git commit```

   ```git commit -m "Primeiro commit"```

3. Visualizando o status dos arquivos

   `git status`



## Logs

```
git log
git log --decorate
git shortlog
git shortlog -sn
git log --graph
git show <hash>
```



## Visualizando diferenças

1. Comando `git  diff` é utilizado para revisão de modificações. Utilizar antes de fazer um commit como forma de revisão;
   ```git diff```

2. Comando `git diff --name-only` é utilizado para mostrar somente o nome dos arquivos modificados;

   ```git diff --name-only ```



## Desfazendo coisas com o reset

1. Se um arquivo foi editado de forma incorreta e deseja-se resetar a alteração. Não funciona se o arquivo estiver em staged.

   ```git checkout <nomedoarquivo>```

   - Para tirar um arquivo de staged:

     ```git reset HEAD <nomedoarquivo>```

   

   ### Tipos de reset

   1. Reset `soft`. Desfaz o commit e volta o(s) arquivo(s) para staged com status já pronto(s) para ser(em) comitado(s) novamente.

      ```git reset --soft <hash>```

   2. Reset `mixed`. Desfaz o commit e volta o(s) arquivo(s) para o(s) estado(s) anterior(es).

      `git reset --mixed <hash>`

   3. Reset `hard`. Remove o commit e tudo que vinha antes dele.

      `git reset --hard <hash>`

      

      OBS: A hash a ser utilizada é a anterior ao commit que se deseja resetar. Pois significa que a partir daquele ponto, tudo será resetado.

      

## Criando repositório remoto no GitHub



1. Acessar a plataforma do GitHub, criar um conta e depois criar um novo repositório passando um nome.



## Ligando repositório local com remoto



1. Copiar o endereço remoto (SSH ou HTTP) e executar o comando abaixo:

   `git remote add origin <endereço>` //Ex.: git@github.com:username/repositoryname.git

2. Enviar os arquivo para o repositório remoto.

   `git push -u origin master`

   onde `origin` é o destino remoto (para onde vai) e `master` é o repositório local (de onde vem).



## Enviando mudanças para o repositório remoto



1. Após fazer modificações locais, basta dar um commit para efetuar as mudanças e empurrar para o repositório remoto usando o `push`.

   `git commit -m "Adicionado [...]"`

2. Enviando para o remoto.

   `git push origin master`
