### Challenge 1

- [x] Criar um todo;
- [x] Listar todos os todos;
- [x] Alterar o title e deadline de um todo existente;
- [x] Marcar um todo como feito;
- [x] Excluir um todo;

- Tudo ocorrerá de acordo com o username que será passado pelo header.

### POST `/users`

A rota deve receber `name`, e `username` dentro do corpo da requisição. Ao cadastrar um novo usuário, ele deve ser armazenado dentro de um objeto no seguinte formato:

```jsx
{
	id: 'uuid', // precisa ser um uuid
	name: 'Danilo Vieira',
	username: 'danilo',
	todos: []
}
```

Certifique-se que o ID seja um UUID, e de sempre iniciar a lista `todos` como um array vazio.
O objeto do usuário deve ser retornado na resposta da requisição.

- [x] Concluído

### GET `/todos`

A rota deve receber, pelo header da requisição, uma propriedade `username` contendo o username do usuário e retornar uma lista com todas as tarefas desse usuário.

- [x] Concluído

### POST `/todos`

A rota deve receber `title` e `deadline` dentro do corpo da requisição e, uma propriedade `username` contendo o username do usuário dentro do header da requisição. Ao criar um novo _todo_, ele deve ser armazenada dentro da lista `todos` do usuário que está criando essa tarefa. Cada tarefa deverá estar no seguinte formato: . Certifique-se que o ID seja um UUID.

```jsx
{
	id: 'uuid', // precisa ser um uuid
	title: 'Nome da tarefa',
	done: false,
	deadline: '2021-02-27T00:00:00.000Z',
	created_at: '2021-02-22T00:00:00.000Z'
}
```

**Observação**: Lembre-se de iniciar a propriedade `done` sempre como `false` ao criar um _todo_.

**Dica**: Ao fazer a requisição com o Insomnia ou Postman, preencha a data de `deadline` com o formato `ANO-MÊS-DIA` e ao salvar a tarefa pela rota, faça da seguinte forma:

```jsx
{
	id: 'uuid', // precisa ser um uuid
	title: 'Nome da tarefa',
	done: false,
	deadline: new Date(deadline),
	created_at: new Date()
}
```

Usar `new Date(deadline)` irá realizar a transformação da string "ANO-MÊS-DIA" (por exemplo "2021-02-25") para uma data válida do JavaScript.
O objeto do `todo` deve ser retornado na resposta da requisição.

- [x] Concluído

### PUT `/todos/:id`

A rota deve receber, pelo header da requisição, uma propriedade `username` contendo o username do usuário e receber as propriedades `title` e `deadline` dentro do corpo. É preciso alterar **apenas** o `title` e o `deadline` da tarefa que possua o `id` igual ao `id` presente nos parâmetros da rota.

- [x] Concluído

### PATCH `/todos/:id/done`

A rota deve receber, pelo header da requisição, uma propriedade `username` contendo o username do usuário e alterar a propriedade `done` para `true` no _todo_ que possuir um `id` igual ao `id` presente nos parâmetros da rota.

- [x] Concluído

### DELETE `/todos/:id`

A rota deve receber, pelo header da requisição, uma propriedade `username` contendo o username do usuário e excluir o _todo_ que possuir um `id` igual ao `id` presente nos parâmetros da rota.

- [x] Concluído

  ##
<div>
  <a href="https://www.linkedin.com/in/jackson-antunes-143318182/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>
