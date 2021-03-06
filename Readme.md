# Github

# Configurações
- Configurar nome
  - git config --global user.name "Paulo Ricardo"
- Configurar email
  - git config --global user.email "paulo.silva@ma9.com.br"
- Configurar editor principal
  - git config --global core.editor vim


# Criar Repositório
- 1° Criar uma pasta para o projeto
  - mkdir <Nome Do Projeto>
- 2° Entrar na pasta
  - cd <Diretorio Do Projeto>
- 3° Inicializar o repositório
  - git init


# Editar Texto
- 1° Entrar no arquivo
  - vim Readme.md
- 2° Aperta a tecla "i" para entrar no modo insert
- 3° Após edição aperta a tecla "esc" para sair do modo insert
- 4° Salva o texto e retorna
  - :wq   (w = salvar, q = sair do modo edição)


# Respositório
- Verificar status
  - git status
- Adicionar arquivos
  - git add <Nome Do Arquivo>
- Commitar arquivos
  - git commit -m "<comentário>"
  - git commit -am "<comentário>"
- Visualizar logs
  - git log
  - git log --author="<Nome do autor>" 
  - git show
- Visualizar logs de forma curta (os autores, quantos commits e quais foram)
  - git shortlog
  - Mostra só a quantidade de commits e os autores
    - git shortlog -sn
  - Mostra em forma gráfica
    - git log --graph
- Visualizar alterações nos arquivos
  - git diff
- Visualizar o nome dos arquivos que sofreram alterações
  - git diff --name-only


# Desfazer alterações
- Arquivos antes de stage
  - git checkout <Nome do Arquivo>
- Arquivos no stage
  - git reset HEAD <Nome do Arquivo>


# Desfazer commit
- Arquivo vai ficar em staged pronto para ser commitado
  - git reset --soft
- Arquivo permanercerá modificado mas não em staged
  - git reset --mixed
- Arquivo não estará modificado
  - git reset --hard


# SSH - Protocolo para identificar o usuário ao servidor
- 1° Gerar chave SSH
  - https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh
- 2° Abrir a chave publica no git
  - cat <Nome da chave>
- 3° Ir nas configurações do Github e colar a chave SSH


# Push
- 1° Informar o git remote
  - git remote add origin https://github.com/PauloRicardoMA9/CursoGit.git
- 2° Realizar o push (origin = pra onde vai, master = de onde vem)
  - git push -u origin master
- Visualizar o repositorio
  - git remote -v

  
# Clonar repositorio do github
- 1° Pegar o SSH do repositorio pelo github
  - git clone <SSH> <nome pro repositorio local>

 
# Branch
- Criar
  - git checkout -b <Nome do Branch>
- Mostrar quais branchs existem
  - git branch
- Navegar entre os branchs
  - git checkout <Nome do Branch>
- Apagar um branch
  - git branch -D <Nome do Branch>


# Merge
- git merge <Nome do Branch>


# Rebase
- git rebase <Nome do Branch>


# Ignore
- Serve para não commitar arquivos
- É possível não só especificar um arquivo específico, como também arquivos com determinadas extensões
- Cria um arquivo .gitignore e dentro dele escreve *<extensão desejada> ex: *.json
  - vim .gitignore
- Para ignorar um arquivo específico basta colocar o nome do arquivo dentro do .gitignore


# Stash
- Responsável por guardar modificações que ainda não foram commitadas em um arquivo em que eu posso chamar quando achar necessário
  - git stash
- Para aplicat as mudanças que estavam salvas
  - git stash apply
- Listar todas as mudanças no stash
  - git stash list
- Limpar todas as mudanças no stash
  - git stash clear


# Alias
- git config --global alias.<comando que quer> <comando que deseja que seja feito>
- ex: git config --global alias.s status


# Tags
- Criar tag
  - git tag -a <versão> -m "<mensagem>"
  - ex: git tag -a 1.0.0 -m "Readme Finalizado"
- Visualizar tags
  - git tag


# Revert
- Abre o log
  - git log
- Seleciona para qual commit deseja voltar
- Retorna para aquele commit
  - git revert <id do commit>


# Remover tags e branches remotos
- git push origin :<tag ou branch>

 
# Pull
- git pull origin master --rebase
