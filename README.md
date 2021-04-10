# Projeto-DIO-ANGULAR-Single-Page-Angular

:spiral_calendar: Atualizado em 10 de abril de 2021 :heart:

<img align="right" alt="GIF" height="160px" src="https://github.com/rdeconti/rdeconti-resources/blob/main/Digital%20Innovation%20One%20-%20Logotipo.png" />

# Projeto Digital Innovation One MRV .Net Developer

# Vaquinha on-line

Este projeto foi proposto pela Digital Innovation One - Link do código original: https://github.com/elizarp/dio-dotnet-poo-lab-1

Professor: Eliézer Zarpelão

Aula: https://web.digitalinnovation.one/project/implementando-sua-stack-de-testes-de-unidade-e-integrados-em-um-projeto-net-de-crowdfunding/learning/eb3bfe30-1f25-45cd-9219-d814db37fa3d?back=/track/mrv-net-developer&bootcamp_id=2aa1519c-08ce-4f37-873f-368794f735d2

# Descrição

Quer se sentir mais seguro nas entregas de suas aplicações? Aprenda a testar um projeto de crowdfunding (vaquinha online) desenvolvida em .Net Core com a arquitetura MVC. Você ira baixar uma aplicação completa feita por pelo expert e a sua missão será implementar a parte de testes desta aplicação. Veja na teoria e na prática os principais conceitos de testes para aumentar a qualidade de entrega de seus projetos com testes de unidade, integrados e TDD.

# Detalhes obtidos das aulas

- Banco de dados "in-memory"
- Testes comuns (fixtures): executados com uma view válida e outra view inválida
- Testes de interface: utilizou o "selenium"
- Utilizou TDD: desenvolvimento orientado a testes
- Utilizou biblioteca "BOGS" para criar os "FAKERS" (gera dados válidos e a partir das informações do Model) (CEP está hard-code pois o "BOGS" não consegue gerar CEP)
- Para doação "FAKER" gera dados levando em conta a regra de negócio definida
- Cada entity tem validações para garantir a integridade do banco de dados
- Para os testes são gerados dados válidos e inválidos (massa de teste)

 -***************************************************************************************************************************

- Teste de unidade: utilza o "XUNIT": [fact] define o caso de teste e [trait] documenta parametros e organiza os testes

- no Visual Studio Code é necessário instalar a extensão ".NET TEST EXPLORER". No Visual Studio 2019 é nativo.
- Fluxo principal (caminho feliz): teste sem problemas
- Fluxo alternativo: teste com problema
- Todo teste tem "TRIPLE A": Arrange, Act, Assert (Prepara, Excuta, Audita)
- Instalado o "FLUENTE ASSERTIONS" para corrigir a utilização do Assert
- Na validação da entity existem as mensagens de erro que serão utilizadas na saída dos testes inválidos
- Os testes podem ser "debugados"
- "FAKER+FIXTURE" podem gerar e-mails válidos e inválidos para realizar os testes
- Utilizou "THEORY" que passa uma sequência de parâmetros para os testes serem executados 
- -- exemplo: valor da doação com vários valores passados para o teste
- -- boa ferramenta para testar os limites e conversão numéricas
- -- chamado de teste inline
- Também são testados os "controllers" para impedir que mesmo com dados inválidos o processo passe de uma view para outra sem apresentar erros
- Para testar o "controller" é utilizado o "MOCK" que emula um determinado componente ("FAKE" gera dados e "MOCK" simula comportamento da classe)

-****************************************************************************************************************************

- Testes de integração: teste a integração entre os módulos
- Utiliza "FACTORY" para simular a aplicação
- Verifica se as páginas são carregadas com os dados completos de acordo com os dados de teste

-****************************************************************************************************************************

- Testes de automação de interface: realizados com Selenium
- Utiliza DRIVER FACTORY
- Utiliza WEB DRIVER
- Testes feitos com FireFox e Google Chrome
- Selenium sobe a instância da URL para executar os testes na aplicação
- Procurou o LOGO da Vaquinha para saber se carregou a página
- Procurou os botões na página para saber se encontra a outra tela
- A ferramenta simula o comportamento do usuário
- Este tipo de teste é recomendado para os processos mais críticos da aplicação
- *****************************************************************************************************************************
- TDD: primerio cria o teste e depois cria o código

# Problemas encontrados e soluções

- NETSDK1004: arquivo de ativos ' C:\path\to\project.assets.jsem ' não encontrado ---> solução: executar no terminal o comando "dotnet restore"

# Testes executados (utilizando IDE Visual Studio Code)

- Ao executar o projeto Vaquina.MVC.csproj o Visual Studio Code procura todos os testes existentes: forma encontrados 37 testes para serem executados

## Telas dos testes executados

- Tela inicial
<img src="https://github.com/rdeconti/Projeto-DIO-.Net-Vaquinha-On-Line/blob/main/Execution-tests/telas-aplicativo.jpg" />

- Tela da doação
<img src="https://github.com/rdeconti/Projeto-DIO-.Net-Vaquinha-On-Line/blob/main/Execution-tests/telas-aplicativo-doa%C3%A7%C3%A3o.jpg" />

- Tela com a lista dos testes (utilizando a extensão ".NET TEST EXPLORER")
<img src="https://github.com/rdeconti/Projeto-DIO-.Net-Vaquinha-On-Line/blob/main/Execution-tests/telas-lista-dos-testes.jpg" />

- Tela iniciando a execução de um teste
<img src="https://github.com/rdeconti/Projeto-DIO-.Net-Vaquinha-On-Line/blob/main/Execution-tests/telas-execu%C3%A7%C3%A3o-de-um-teste.jpg" />

- Tela com o log de execução do teste
<img src="https://github.com/rdeconti/Projeto-DIO-.Net-Vaquinha-On-Line/blob/main/Execution-tests/telas-execu%C3%A7%C3%A3o-de-um-teste-log.jpg" />

- Tela com o resultado de um teste
<img src="https://github.com/rdeconti/Projeto-DIO-.Net-Vaquinha-On-Line/blob/main/Execution-tests/telas-execu%C3%A7%C3%A3o-indivudual-dos-testes.jpg" />
