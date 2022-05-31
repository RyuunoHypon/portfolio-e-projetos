Para começar, instalei o Git usando os seguintes comandos(no meu caso é o Ubuntu):

###### $ apt-get install git
###### $ add-apt-repository ppa:git core/ppa
Executando o último comando você adiciona um repositório para o Git. Então executei:

###### $ apt update
###### $ apt install git
Depois de instalar, precisaremos configurar uma chave SSH, que serve para autenticar nossas mudanças nos repositórios do Git e GitHub.
Criei uma chave específica, mencionada nos cursos da Digital Innovation One (DIO._) com o seguinte comando em uma pasta que eu criei:

###### $ ssh-keygen -t ed25519 -c "meu email".
E, para acessar o código:

###### $ cat id_ed25519.pub
Eu vou exportar a chave pública para o GitHub, então usarei a chave com o final .pub no final do comando. Copiei o codigo associado e o meu email e fui no site do GitHub.

#### GitHub
Lá, eu criei a chave e colei o código que estava no comando "$ cat id_ed25519.pub" no local apropriado. Após isso, voltei ao terminal e digitei:

###### $ eval $(ssh-agent -s)
###### $ssh-add id_ed25519
E, para finalizar, eu clonei o repositório copiando o link SSH e colando o no terminal com o seguinte comando:

###### $ git clone "código SSH"
Configurei meu email e nome para sincronizar o Git com o do GitHub usando estes comandos:

###### $ git config --global user.email "meu email"
###### $ git config --global user.name "RyuunoHypon"
Depois executei:

###### $ git add *
###### $ git commit -m "commit inicial"
E, concluindo, eu finalizei usando estes comandos para empurrar as mudanças para o repositório:

###### $ git remote add origin "endereço do repositório"
###### $ git push origin master
