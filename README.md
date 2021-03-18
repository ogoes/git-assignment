# Git Assignment
## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo

Abra uma issue nesse reposit�rio aqui indicando o link para o arquivo no seu repo.

1. Descreva qual � a sa�da dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
git branch > Mostra a branch atual do projeto;
git checkout BRANCH_NAME (USE THE NAME OF AN EXISTING BRANCH) > Muda a branch atual;
git log --decorate > Mostra o hist�rico de commit no projeto (branch atual); 
```

2. Tente usar `git log --graph --all`. O que acontece?
```
O hist�rico de commits � mostrado com apenas o commit inicial do projeto
```

3. Use `git diff BRANCH_NAME`  para ver as diferen�as de um ramo e do ramo atual.
   Sumarize as diferen�as do master e do outro ramo.

```
� mostrado as adi��es/remo��es naquela branch referente a branch referida
```

4. Escreva uma sequencia de comandos para mesclar o ramo n�o-master no `master`

```
git checkout master && git merge BRANCH
```


5. Escreva um comando (ou sequ�ncia) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
git checkout master && git checkout -b math
```
   
6. Edite B.java adicionando o c�digo abaixo ao conte�do do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudan�as
```
git commit -a -m MESSAGE
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte c�digo-fonte (confirme sua mudan�a para` master`):
```java
System.out.println("Hello World")
```

9. Escreva uma sequ�ncia de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
git checkout master && git merge math
```
  Houve um conflito de merge:

```
Auto-merging handson/B.java
CONFLICT (content): Merge conflict in handson/B.java
Automatic merge failed; fix conflicts and then commit the result.
```


10. Escreva um conjunto de comandos para abortar a mesclagem
```
git merge --abort
```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as fun��es implementadas s�o necess�rias. Explique o seu procedimento

Arquivo B.java ap�s o comando `git merge math`: 

```
public class B {


}
<<<<<<< HEAD
System.out.println("Hello World")
=======
System.out.println("I know math, look:")
System.out.println(2+2)
>>>>>>> math

```

Para resolve isso � necess�rio escolher qual das altera��es ser� efetivada, caso as duas sejam aceitas � necess�rio alterar o c�digo para que n�o haja problemas, resultado da altera��o:

```
public class B {


}
System.out.println("Hello World")
System.out.println("I know math, look:")
System.out.println(2+2)
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
git commit -a -m "resolve merge master-math"
```


