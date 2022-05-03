
# Olá 👋, seja bem vindo(a) ao desafio "Trabalhando com middlewares"

### Aplicação desenvolvida durante o segundo desafio da trilha de NodeJS do Ignite da Rocketseat

![Logo](https://repository-images.githubusercontent.com/341683746/42e1ab80-77af-11eb-9e07-47f9e46b3e6e)



## Stack utilizada

**Backend:** NodeJS



## Aprendizados

Com essa aplicação pude reaprender o conceitos do Node além de entender o básico sobre desenvolvimento de apis e melhores práticas no backend.
## Funcionalidades

Será permitida a criação de um usuário com name e username, bem como fazer o CRUD de todos:

- Criar um novo todo;
- Listar todos os todos;
- Alterar o title e deadline de um todo existente;
- Marcar um todo como feito;
- Excluir um todo;

Tudo isso para cada usuário em específico. Além disso, dessa vez teremos um plano grátis onde o usuário só pode criar até dez todos e um plano Pro que irá permitir criar todos ilimitados, isso tudo usando middlewares para fazer as validações necessárias.

### Middlewares da aplicação

Com o template já clonado e o arquivo index.js aberto, você deve completar onde não possui código com o código para atingir os objetivos de cada teste.

Nesse desafio não será necessário alterar o código de nenhuma rota, apenas dos middlewares. Os testes iram também testar o funcionamento das rotas mas o resultado depende apenas da dos middlewares.

Aqui teremos uma breve descrição do que cada middleware deve fazer e na seção Especificação de testes, você verá com mais detalhes o que precisa ser feito para satisfazer cada teste.

### checksExistsUserAccount
Esse middleware é responsável por receber o username do usuário pelo header e validar se existe ou não um usuário com o username passado. Caso exista, o usuário deve ser repassado para o request e a função next deve ser chamada.

### checksCreateTodosUserAvailability
Esse middleware deve receber o usuário já dentro do request e chamar a função next apenas se esse usuário ainda estiver no plano grátis e ainda não possuir 10 *todos* cadastrados ou se ele já estiver com o plano Pro ativado.

### checksTodoExists
Esse middleware deve receber o username de dentro do header e o id de um todo de dentro de request.params. Você deve validar o usuário, validar que o id seja um uuid e também validar que esse id pertence a um todo do usuário informado.

Com todas as validações passando, o todo encontrado deve ser passado para o request assim como o usuário encontrado também e a função next deve ser chamada.

### findUserById
Esse middleware possui um funcionamento semelhante ao middleware checksExistsUserAccount mas a busca pelo usuário deve ser feita através do id de um usuário passado por parâmetro na rota. Caso o usuário tenha sido encontrado, o mesmo deve ser repassado para dentro do request.user e a função next deve ser chamada.
## Rodando localmente

Clone o projeto

```bash
  git clone https://github.com/caiquemoreiradev/.git
```

Entre no diretório do projeto

```bash
  cd ignite-desafio-trabalhando-com-middlewares
```

Instale as dependências

```bash
  npm install
```

Inicie o servidor

```bash
  npm run dev
```

ou 

```bash
  yarn dev
```


