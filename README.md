# intmed-desafio
## INSTRUCOES PARA RODAR O PROJETO

### Dependências
```
Python: 3.10.2
django: 4.0.4
```

### 1.1 Configurando o ambiente virtual
1. `python3 -m venv myenv`
2. `source venv/bin/activate`
3. `pip install django`
3. `pip install djangorestframework`

### EXECUTANDO O PROJETO
1. `python manage.py makemigrations`
2. `python manage.py migrate`
3. `python manage.py runserver`

### EXPLORANDO  O PROJETO 
* Para cadastrar os médicos e as agendas você deve entrar na seguinte url: `http://127.0.0.1:8000/admin`.

>user: andar1n0

>password: yo199

## Endpoints

Método | Recurso | Descricão
-------|---------|----------
GET| /consultas/| Lista todos as consultas 
GET| /agenda/| Lista as agendas 
POST| /consulta | Cadastra uma consulta
DELETE| /consultas/<pk> |Exclui a Consulta com a PK informada
 
- Exemplo de como marcar uma consulta:
	
```POST http://127.0.0.1:8000/consulta/ ```
  
  ```json
  {
	"dia": "2029-07-03",
  	"horario": "14:00",
	"doctor_agenda": 2
}
```

	
### Notas importantes:
- [x] A listagem não deve exibir consultas para dia e horário passados
 
- [x] Agendas para datas passadas ou que todos os seus horários já foram preenchidos devem ser excluídas da listagem 
  
- [x] Não deve ser possível desmarcar uma consulta que nunca foi marcada (identificador inexistente)
  
- [x] Não deve ser possível criar uma agenda para um médico em um dia passado
  
- [x] Não deve ser possível marcar consultas para dia e horário passados
  
- [x] Não deve ser possível criar mais de uma agenda para um médico em um mesmo dia
  
- [x] Não deve ser possível marcar consultas para um dia e horário não disponível
   
Notas/Impressões: No [Issues](https://github.com/Intmed-Software/desafio/issues) do desafio consta que o referido é para pleno ou sênior, no entanto, gostaria de ressaltar que, como conversamos na entrevista, almejo a vaga de backend júnior. Esse foi meu primeiro contato com django, apesar de previamente já ter trabalhado com spring e python, foquei no projeto em backend porque esse é meu objetivo de carreira, lidar com um framework novo foi realmente desafiador, durante a semana do desafio me dediquei ao máximo lendo a documentação e aplicando os conceitos ao projeto. O CRUD está funcional e operante, qualquer dúvida: tj.vinci97@gmail.com. Abraços.
