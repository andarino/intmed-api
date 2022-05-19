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
POST| /consultas | Cadastra uma consulta
DELETE| /consulta/<pk> |Exclui a Consulta com a PK informada
 
- Exemplo de como marcar uma consulta:
	
```POST http://127.0.0.1:8000/consulta/ ```
  
  ```json
  {
	"dia": "2029-07-03",
  	"horario": "14:00",
	"doctor_agenda": 2
}


	
### Notas importantes:
- [x] A listagem não deve exibir consultas para dia e horário passados
 
- [x] Agendas para datas passadas ou que todos os seus horários já foram preenchidos devem ser excluídas da listagem 
  
- [x] Não deve ser possível desmarcar uma consulta que nunca foi marcada (identificador inexistente)
  
- [x] Não deve ser possível criar uma agenda para um médico em um dia passado
  
- [x] Não deve ser possível marcar consultas para dia e horário passados
  
- [x] Não deve ser possível criar mais de uma agenda para um médico em um mesmo dia
  
- [x] Não deve ser possível marcar consultas para um dia e horário não disponível
  
  
