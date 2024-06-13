# P-App_Logs-M10

# Introdução

Implementar um sistema de logs para armazenar as ações que acontecem no sistema. Vocês podem utilizar o sistema de logs que foi apresentado em sala ou outro sistema de logs que vocês acharem interessante.

## Aplicações

Microserviços:

- Aplicação em Flutter
- Backend Auth
- Banco de Dados Postgres
- Filtro de Imagem
- Log (Log dos Microserviços)
- Gateway
- Sistema 3 (Repositório Murilo)

## Sistema de Log

### Gateway

O Gateway tem um sistema de log implementado na qual quando acessado qualquer rota de uma aplicação que esteja programada no gateway, é gerado um log com informações de data de acesso, qual foi o tipo de requisição, se a requisição teve exito e em qual rota. Ela é amarzenada em na pasta /logs, no arquivo access.log ou no error.log quando a requisção não foi bem sucedida ou ainda quando tenta acessar um rota inexistente.

### Back_Auth

O Log do Back_Auth é um micro serviço separado que recebe requisições de log das outras aplicações (Filtro, Flutter e Login)e resgitram todas em um banco de dados Postgres. Os log da aplicação e do Gateway estão separados.

### Sistema 3

A aplicação utilizada em sala de aula, utiliza a mesma pasta /logs nos arquivos app.log e app.log-{data}.txt para armazenar os acessos as rotas cadastradas na aplicação.

### Log da Aplicação:

1. Na pasta raiz:

```bash
docker compose up
```

- Logs da Aplicação

1. Acesse a porta 8080

2. Credenciais:

Banco: Postgres
users: postgres
senha: postgres

3. Acesse a tabela de logs

4. Abra um novo no terminal o diretório app_hibrido execute os comandos:

```bash
flutter pub get
```

e depois:

```bash
flutter run
```

* Tenha o ambiente Android Studio instalado e configurado.

5. Credenciais de Login:

User:   kil.teste@inteli.com
Senha:  123

6. Recarrege a página do banco de dados e veja o log surgindo da aplicação.

### Log do Sistema 3 e Gateway

Após rodar o ***docker compose up***, acesse o arquivo access.log, app.log e error.log no Vscode e comece a acessar as rotas da aplicação, veja que os arquivos vão começar a gerar log's:

- /
- /usuários
- /produtos

## Arquiterura

![Arquitetura](/img/arquitetura_page.jpg)