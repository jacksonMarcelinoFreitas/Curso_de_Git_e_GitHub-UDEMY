
Ciclo de vida dos Ststus dos arquivos

Untracked (não marcado - adicionado no repositório, mas não visto pelo git, o git não reconhece a existencia desse arquivo)
Unmodified (arquivo modificado, existente no git mas com nehuma modicação em cima dele)
Modified (arquivo depois de modificado)
Staged (area que será criada a versão, momento em que a versão é fechada comitada e se torna unmodified novamente, ou seja está pronto para ser salvo)

git status (reporta como está o repositório no momento)
git add "file..." (adiciona o arquivo e preparado para commitar)
Caso haja modificações no arquivo:
O status será modified, devendo add denovo para deixar pronto par commitar
git commit -m "comentário" (Este comando faz o versionamento local do arquivo) (no nome do commit é interessande colocar as alterações que foram feitas)
Não é possível commitar sem adicionar a nova modificação