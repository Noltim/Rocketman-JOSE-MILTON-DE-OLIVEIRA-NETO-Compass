# Compass UOL: Sprint 6

# Sobre o Projeto

Seu início se dá pela pasta Teste, onde está contido o desenvolvimento dos teste, assim como o report em newman, testes em postman arquitetados em JavaScript, provas visuais dos teste em pleno funcionamento, Apache JMeter com teste de performance, anotações e afins.
Navegando entre os arquivos supracitados temos os testes extraidos do postman no formato Json, assim como os recursos necessarios para usa-los, Local.postman_enviroment, ServeREst.postman_collection. Estes serão acrescidos ao newman para obter o report html, conforme constamos mais abaixo.


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
- Apache JMeter

## Conteúdo do Projeto 
- Testes
- Newman
- Postman
- Local.postman_environment
- ServeRest.postman_collection
- ServeRest.postman_test_run
- Mapa atualizado dos Status code
- Apache JMeter e seus resultados

# Sobre o Projeto

## Prepraração para execução do projeto

- Requer o Nodejs 14.0 ou superior instalado, postman, newman instalados na sua maquina e o Apache JMeter.(Na instalação você verá onde baixar e como instalar.)
- Baixar o repositório ou cloná-lo
- Iniciar o Postman e importar os arquivos '.postman' nas pastas. 
- Os Arquivos estão localizados na pasta 'teste'com nome Local.postman... e ServeRest.postman...

PS: O JMeter não é obrigatorio, mas caso deseje ver ou executar o teste de performance localmente pode baixa-lo.

## Instalação

### Apache JMeter

- Instalando o JMeter
Na data de hoje a versão mais atual é a 5.5, vamos para o passo a passo da instalação:

- Faça o download do JMeter no site oficial (https://jmeter.apache.org/download_jmeter.cgi).

- Extraia o arquivo "apache-jmeter-5.5.zip" para uma pasta desejada.

- Pronto estamos pronto para usar o JMeter.

### Postman
- Para instalação do postman deve-se seguir ao site oficial (https://www.postman.com/downloads/) e baixar a versão correspondente ao seu sistema operacional.

### Newman + Nodejs
- Para instalação do newman deve-se seguir os seguintes passos:

- Baixar o NodeJS do site oficial ( https://nodejs.org/ ). Apenas certifique-se de instalar a versão que corresponde ao seu sistema operacional. 
- Durante a configuração da instalação, confirme se o gerenciador de pacotes npm está selecionado, pois usaremos este pacote na próxima etapa.

- Verificando o sucesso da instalação
- Podemos verificar se o NodeJS e o npm foram instalados com sucesso abrindo cmd e digitando:

- node-v

- A versão do NodeJS deve aparecer.

- npm -v

- A versão Npm deve aparecer.

- Instalando Newman e HTML Reports
- Newman é o executor de coleção que nos permite executar e testar uma coleção Postman a partir da linha de comando. A instalação é bem simples. 
- Use cmd mais uma vez e digite:

- npm install -g newman

- Assim que a instalação do Newman estiver concluída, podemos instalar os reports digitando:

- npm install -g newman-reporter-html
- npm install -g newman-reporter-htmlextra

- Finalmente, estamos prontos para criar os relatórios HTML!

## Execução


### JMeter

- Para executar o JMeter, devemos ir no diretório $Local de instalação do JMeter\bin\.
- Para executar no Windows devemos utilizar o arquivo jmeter.bat, para executar no Linux ou Mac devemos utilizar o arquivo jmeter.
- Ao acessar o diretório, navegue até a aba "Exibir" e marque a opção "Extensões de nomes de arquivos". Após selecionar o arquivo que corresponde ao seu SO o JMeter será executado e está pronto para uso.
- Bom agora estamos sabendo como executar nosso JMeter. Estão prontos para começar a rodar nossos testes?

- Para rodar nossos teste abra o JMeter e clique em file > Open > teste > JMeter > TesteServeRest.jmx. Pronto abrimos nosso teste.
PS: a pasta teste é baixada deste repositorio.

- Para rodar nosso testes clique em grupo de usuários e preencha os campos: Number of Threads(users) com quantos usuarios desejas para o teste, por default recomendo 500, pois é o modelo que fizemos para o teste. E em Loop Count coloque quantas interações deseja por usuário, por default recomendamos 2.

- Configurado nosso teste para iniciar clique Edit > Start e para ver os resultado você deve expandir a aba grupo de usuários e clica em: Aggregate Graph e Aggregate Report ambos externam os testes realizados.

### Newman

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
