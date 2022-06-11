# Compass UOL: Sprint 6

# Sobre o Projeto

Seu início se dá pela pasta Teste, onde está contido o desenvolvimento dos teste, assim como o report em newman, testes em postman arquitetados em JavaScript, provas visuais dos teste funcionando, anotações e afins.
Navegando entre os arquivos supracitados temos os testes extraidos do postman no formato Json, assim como os recursos necessarios para usa-los, Local.postman_enviroment, ServeREst.postman_collection e ServeRest.postman_teste_run, estes serão acrescidos ao newman para obter o report html, conforme constamos na pasta Newman.


Adendos: O autor trabalho simulando uma equipe, onde o mesmo sempre criava uma branch para cada “funcionalidade” nova a ser implementada no código. Com isso o mesmo antes de fazer update dava um pull para receber os arquivos atualizado e conseguintemente introduzia os novos arquivos, a fim de evitar conflito e deturbar o andamento do projeto.


## Tecnologias e ferramentas utilizadas
- Git 
- GitHub
- Visual Studio Code
- Javascript
- Postman
- Nodejs
- Mocha
- Chai

## Conteúdo do Projeto 
- Testes
- Newman
- Postman
- Local.postman_environment
- ServeRest.postman_collection
- ServeRest.postman_test_run

# Sobre o Projeto

## Prepraração para execução do projeto

- Requer o Nodejs 14.0 ou superior instalado, postman e newman instalados na sua maquina.(Na instalação você verá onde baixar e como instalar.)
- Baixar o repositório ou cloná-lo
- Iniciar o Postman e importar os arquivos '.postman' nas pastas. 
- Os Arquivos estão localizados na pasta 'teste'com nome Local.postman... e ServeRest.postman...


## Instalação


- Para instalação do postman deve-se seguir ao site oficial (https://www.postman.com/downloads/) e baixar a versão correspondente ao seu sitema operecional.

- Para instalação do newman deve-se seguir os seguintes passos:

- Baixar o NodeJS do site oficial ( https://nodejs.org/ ). Apenas certifique-se de instalar a versão que corresponde ao seu sistema operacional. 
- Durante a configuração da instalação, confirme se o gerenciador de pacotes npm está selecionado, pois usaremos este pacote na próxima etapa.

- Verificando o sucesso da instalação
- Podemos verificar se o NodeJS e o npm foram instalados com sucesso abrindo cmd e digitando:

- node-v

- A versão do NodeJS deve aparecer.

- npm -v

- A versão Npm deve aparecer.

- Instalando Newman e HTML Reporters
- Newman é o executor de coleção que nos permite executar e testar uma coleção Postman a partir da linha de comando. A instalação é bem simples. 
- Use cmd mais uma vez e digite:

- npm install -g newman

- Assim que a instalação do Newman estiver concluída, podemos instalar os repórteres digitando:

- npm install -g newman-reporter-html
- npm install -g newman-reporter-htmlextra

- Finalmente, estamos prontos para criar os relatórios HTML!

## Execução no newman

- Executando nossos arquivos JSON
- Esta é a nossa última etapa na criação dos relatórios HTML. 

- Primeiro, precisamos abrir o cmd e acessar a pasta onde salvamos nossos arquivos JSON (por exemplo, cd C:\Users\YourName\ExportedJSONs). 

- Uma vez que acessamos esta pasta, podemos executar os arquivos dentro dela usando este comando:

- newman run ServeRest.postman_collection.json -e Local.postman_environment.json -n 4 -r htmlextra

# Considerações Finais

 Este Projeto não seria possível sem o apoio dos meus queridos colegas de estágio, assim como meu Scrum Master Matheus Domingos.
 Durante todo a trilha foi possivel um vislumbre de todo o andamento desse mundo tão vasto chamados de testes. Ser um analista QA não é facil requer muito estudo e dedicação, assim como atenção e cuidado. Agradeço muito aos meus companheiros que ajudaram a todo momento na criação de todos os testes, assim como a Alexandre por auxiliar na criação desse readme.

## Autor

José Milton de Oliveira Neto
