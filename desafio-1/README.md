# Desafio 

Esse é um teste feito para conhecer um  pouco mais de cada candidato. Não se trata de um teste objetivo, capaz de gerar uma nota ou uma taxa de acerto, mas sim de um estudo de caso com o propósito de analisar os conhecimentos, experiências e modo de trabalhar de um candidato. Sinta-se livre para desenvolver sua solução para o problema proposto e em caso de dúvidas entre em contato no especialistafaz@mandic.net.br.

Nesse diretorio existe uma aplicação escrita em Python que apresenta as informações dos personagens do filme "O senhor dos Anéis".
Seu objetivo é fazer deploy dessa aplicação na AWS. Você provavelmente precisará criar uma conta free-tier na AWS, ou utilizar uma sua já existente. Mas não se preocupe, não iremos olhar sua conta ou chamar sua aplicação já rodando, queremos que você crie uma forma de podermos recriar toda sua infraestrutura em nossa conta de maneira simples. Você escolhe como. Crie um arquivo resolucao.md descrevendo todos os passos para que possamos executar sua infraestrutura em nosso ambiente.

* Você deverá partir de um ambiente na AWS sem nenhuma infraestrutura criada.
* A aplicação deverá rodar em container docker.

#### Extra

* Adicionar endpoint para atualizar ou deletar personagens.
* Implementar autenticação na API para garantir que apenas as pessoas autorizadas tenha o acesso.
* Adicionar um endpoint no qual seja possivel pesquisar personagens pelo nome.
* Aplicação salva os dados em mémoria. Quando reiniciamos a aplicação perdemos os dados adicionados. Adicione persistência de dados.

-------------------------------
## Executar a aplicação
Aplicação sobe por default na porta 5000
```sh
$ pip install -r requirements.txt
$ python main.py
```

### Testar a aplicação
Teste GET
```sh
$ curl http://localhost:5000/characters
```
Teste POST
```sh
$ curl -X POST -H "Content-Type: application/json" -d '{
  "Race": "Hobbit",
  "age": "589",
  "name": "Gollum"
}' http://localhost:5000/characters
```

----

# Entrega

* Você deve clonar esse repositório e commitar todas as modificações, porém, não abra um pull request ou deixe seu código de resposta aberto em um fork, por exemplo.
* Depois que terminar, compacte todo o diretório e nos envie. **Queremos analisar seus commits**.
* Envie para o email especialistafaz@mandic.net.br.

Bom trabalho!