# 🔰Curso de Git e GitHub - Udemy

## 🔁Ciclo de vida dos Status dos arquivos

    🔸Untracked (não marcado - adicionado no repositório, mas não visto pelo git, o git não reconhece a existÈencia desse arquivo)
    🔸Unmodified (arquivo modificado, existente no git mas com nehuma modicação em cima dele)
    🔸Modified (arquivo depois de modificado)
    🔸Staged (área que será criada a versão, momento em que a versão é fechada comitada e se torna unmodified novamente, ou seja está pronto para ser salvo)

- *git status* (reporta como está o repositório no momento)
- *git add arquivo-escolhido.* (adiciona o arquivo e o prepara para commitar)

Caso haja modificações no arquivo:

O status será **modified**, devendo dar um **add** denovo para deixar pronto par commitar.

**git commit -m "comentário"** (Este comando faz o versionamento local do arquivo, onde no nome do commit é interessande colocar as alterações que foram feitas para a identificação posterior)

**git commit -am "comentário"** (adiciona todos os arquivos modificados")

Não é possível commitar sem adicionar a nova modificação.


## 📌Mostrando histórico do commit

    git log (mostra a hash do commit, autor e email e data)
    git log --decorate (apresenta mais informações)
    git log --author="nome do autor" (vai listar os commits deste autor)
    git shortlog (mostra quais os autores, quantos commits feitos e quais foram )
    git shortlog -sn (mostra a quantidade de commits e os nomes)
    git log --graph (mostra de forma gráfica o que está acontecendo com os branchs e as versões)
    git show (número da hash) mostra informações sobre o commit



## 👀Visualizando o diff
    git diff (mostra as alterações com a modificação antes de ser adicionada ou commitar)
    git diff --name-only (só apresenta uma lista dos aqruivos que foram modificados)


## ↩️Voltando atrás
    git checkout nome-do-arquivo (retorna o arquivo para antes da mudança feita quando ainda está no estado de edição se for dar add não haverá mais mudanças, já estará consolidado)
    git reset HEAD nome-do-arquivo (tira o arquivo da fila do stage, ou seja para ser commitado)


## ◀️Desfazendo coisas:
**Após o commit**, se quiser voltar:
- Lembrando que aqui o reset deve ser feito com o hash anterior ao que você quer apagar

    git reset --soft hash (apaga o commit mas deixa todas as modificações do arquivo em staged para ser commitado de novo)
    git reset --mixed hash (apaga o commit e volta os arquivos para antes do staged)
    git reset --hard hash (acaba com o commit e todas as alteraçõres realizdas após o commit anterior a este que foi feito antes dele)

## 🔝Adicionando no repositório remoto com repositório existente.
    git remote add origin "url do repositório" (adiciona no repositório remoto)
    git remote (diz o repositório)
    git remote -v (fornece mais informações)
    git push -u origin master (envia os arquivos para o git hub)

Se fizer modificação nos arquivos que jâ estão remotos

    git commit -am "nome do commit" (já faz add e commit)
    git push origin master (envia para o tepositório remoto)


Clonando repositórios remotos: faz o clone/cópia dos arquivos para sua máquina

Fork em arquivos: faz a cópia dentro do GitHub
    git clone

Branches: ramos

    Ramo principal -master;
    Quais são as vantagens;
    - é possível modificar os arquivos, sem modificar o branch principal;
    - facilmente desligável;
    - multiplas pessoas trabalhando;
    - evita conflitos;


Criando o branch no git

    git checkout -b nome-da-branch (cria uma branch)
    git branch (mostra/ lista as branchs disponíveis)

Navegando  entre as branchs

    Para mudar de branchs, basta:
        git checkout nome-do-branch;
        git branch -D nome-do-branch (deleta a branch);

Mesclando/Unindo os branchs

    Merge: operação não destrutiva (não mexe no histórico, pois cria um commit extra para juntar as coisas)
    Rebase: apenas coloca o branch secundário e inclui ao início da fila no branch master, criando uma linearidade, perdendo a ordem cronológica)
