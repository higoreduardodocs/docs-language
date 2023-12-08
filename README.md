# Python

## :dart: Overview

Linguagem dinâmica, possui IDLE (python3) já no instalador da linguagem. As variáveis são armazenadas referenciando endereço de memória, fazendo com que seja possíveis várias variáveis apontarem para mesmo endereço reduzindo consumo de memória. Suas classes possuem atributos e comporamentos quando instanciadas. O escopo da linguagem é fechado com indentação de código e não blocos. As funções podem receber parâmetros obrigatórios `no-default arguments` como opcionais `default arguments`, além disso em sua chamada esses parâmetros podem ser passados de forma posicional ou nomeadas também conhecido como `keywords arguments`. Atributos protected/private devem ter `undescore` em sua declação como exemplo: "\_variable". No desenvolvimento de API's é usual quando trabalhar com data/hora usar UTC-0 de acordo com padrão `ISO 8601`. Em testes a utilização de mocks é ideal para simular condições reais não fazendo requisições externas ou consumindo muito recursos da máquina, é ideal utilizar a cobertura completa de testes no projeto `text coverage`.

<details>
<summary>:keyboard: Descrição</summary>

**:book: Tipos primitivos**

    - String `"Hello world"`
    - Int `10`
    - Float `9.99`
    - Bool `True/False`
    - Vazio: `""`
    - Nulo: `None`

**:books: Estruturas de dados**

    - Tuple (Heterogênea) `(10, "Name")`
    - List (Homogênea): `[10, 20]`
    - Set: `{"Name", 20}`
    - Dict: `{"key": 20}`

**:abacus: Operadores aritméticos**

    - Soma: `10 + 15`
    - Subtração: `10 - 15`
    - Multiplicação: `10 * 15`
    - Divisão: `10 / 15`
    - Divisão inteira: `10 // 15`
    - Potência: `10 ** 15`
    - Módulo: `10 % 15`

**:floppy_disk: Operadores relacionais**

    - Igualdade: `2 == 2`
    - Diferença: `2 != 2`
    - Maior: `2 > 2`
    - Maior/Igual: `2 >= 2`
    - Menor: `2 < 2`
    - Menor/Igual: `2 <= 2`

**:bulb: Operadores lógicos**

    - Negação: `not`
    - Conjunção: `and`
    - Disjunção: `or`

**:flashlight: Estruturas condicionais**

```
a = 10
if a > 20:
  print("a > 20")
elif a > 10:
  print("a > 10")
else:
  print("a < 10")
```

**:cd: Estruturas de repetição**

```
i = 1
while i < 10:
  print(i)
  i += 1
```

- Repetição em tuplas:

```
values = 10, 20, 30
for value in values:
  print(value)
```

- Repetição em dicionários:

```
values = { "key1": 10, "key2": 20 }

for value in values:
  print(f"{value} = {values[value]}")

for key in values.keys():
  print(values[key])

for value in values.values():
  print(value)

for k, v in values.items():
  print(f"{k} = {v}")
```

**:scarf: Métodos usuais**

    - Listas: `variable = [10, 8]`
    - Listas Append: `variable.append(10)`
    - Listas Insert: `variable.insert(0, 10)`
    - Listas Index: `print(variable[0])`
    - Listas Sort (Implacement): `variable.sort(reverse=True)`
    - Listas Sorted: `sorted(variable)`
    - Listas Pop: `variable.pop(2)`
    - Listas (Matriz): variable = `[[2, 5], [1, 6]]`
    - Listas Length: `len(variable)`

    - Tuplas: `variable = 5, 10, True`
    - Listas/Tuplas desempacotamento: `first, second, cond = variable`

    - Conjuntos: `variable = {"Name", "Lastname", 10}`
    - Conjuntos: `variable = set(["Name", "Lastname", 10])`
    - Conjuntos Add: `variable.add(20)`
    - Conjuntos Union:
      ```
      variable.union(variable_2)
      variable | variable_2
      ```
    - Conjuntos Intersection:
      ```
      variable.intersection(variable_2)
      variable & variable_2
      ```
    - Conjuntos Difference:
      ```
      variable.difference(variable_2)
      variable - variable_2
      ```

    - Dicionários: `variable = {"key": value}`
    - Dicionários key: `variable["key"]`
    - Dicionários keys: `variable.keys()`
    - Dicionários values: `variable.values()`
    - Dicionários items: `variable.items()`
    - Dicionários unios: `dict({"id": 1, **old_dict})`
    - Dicionários JSON:
      ```
      json.dumps(json_variable)
      json.loads(dict_variable)
      ```

**:electric_plug: Funções**

```
def hello_world(params, other_params=None):
  print(params)
  print(other_params)
  return f"{params} {other_params}"

hello_world("My name is", other_params="Is my name")

def function_blank():
  ...
def function_pass():
  pass
```

**:page_with_curl: Classes**

```
class ClassHelloWorld:
  def __init__(self, params): # constructor
    self.params = params

  def new_params(self, new_params): # comportamento
    self.params = new_params

  def instance_method(self): # Obrigatório ter um obj (instância)
    return ("Método de instância", self)

  @classmethod
  def class_method(cls): # Não obrigatório
    return ("Método de classe, cls)

  @staticmethod
  def static_method(): # Não obrigatório
    return ("Método estático")

hello_world = ClassHelloWorld("My name is")
hello_world.new_params("Is my name")
print(hello_world.params)
print(hello_world.instance_method())
print(ClassHelloWorld.class_method())
print(ClassHelloWorld.static_method())

class ClassBlank:
  ...

class ClassPass:
  pass
```

**:mailbox_with_no_mail: Comandos**

    - Run: `python3 <file-name>`
    - Input: `variable = input("Informe o valor")`
    - Output: `print("Hello world", variable)`
    - Concatenação:
      ```
      "Hello" + "World"
      "Hello" * 5
      ```
    - Type: `type(10)`
    - Endereço objeto memória: `id(10)`
    - Cast: `int(variable)`
    - Quebra linha: `\n`

**:gear: Ambiente virtual**

    - VENV create: `python3 -m venv venv`
    - VENV activate: `source ./venv/bin/activate`
    - VENV deactivate: `deactivate`
    - VENV dependencies:
      ```
      pip list
      pip freeze
      pip freeze > requirements.txt
      pip install <dependency-name>
      pip install -r requirements.txt
      ```

</details>

<details>
<summary>:package: Flask (Framework)</summary>

- Flask run: `flask run`
- Flask var env: `FLASK_APP=main.py FLASK_ENV=development flask run --port 8000`

</details>

<details>
<summary>:package: Django (Framework)</summary>

Aplicação deve ser conter as urls do endpoint, e seus templates ser importados na raíz `<settings.py -> INSTALLED_APPS>`. O acesso admin da aplicação é em `http://localhost:3000/admin` e para cada modelo a ser manipulado pelo superadmin deve ser exposto na page admin do próprio app.

Primeiro passo é criar o ambiente de desenvolvimento: `python3 -m venv venv` e ativá-lo para instalar dependêncies e rodar o projeto: `source ./venv/bin/activate`.
Para instalação individual de dependências pode ser feito por: `pip install Django==4.2.4` ou para instalar a partir de um gerenciador por: `pip install -r requirements/dev.txt`

Com a instalação do Django é realizado a criação do projeto: `django-admin startproject <project-name> .`, para testar seu êxito rode o servidor: `python manage.py runserver`.
A criação de aplicação se dá a nível de entidades logo para cada aplicação deverá ser criada por: `django-admin startapp <app-name>`.

Assim é possível com a aplicação criada gerar seus `Models`, como exemplo:

```
from django.db import models


class Agendamento(models.Model):
  data_agendamento = models.DateTimeField()
  nome_cliente = models.CharField(max_length=255)
  email_cliente = models.EmailField()
  telefone_cliente = models.CharField(max_length=20)
  cancelado = models.BooleanField(default=False)
```

Após a criação do models é nencessário gerar suas migrations: `python manage.py makemigrations` e `python manage.py migrate`

As configurações do projeto é importante ser separada pelo escopo do ambiente em questão. Assim em `/api/settings` gere um `__init__.py` para modularizar o dir, e dentro especifique suas configurações `base`, `dev` e `prod`. Após as configurações definidas devem ser passadas para os arquivos de carregamento em: `/api/asgi.py`, `/api/wsgi.py` e `/manage.py`

    - Django Create: `django-admin startproject <project-name> .`
    - Django Create app: `django-admin startapp <app-name>`
    - Django Run: `python manage.py runserver`
    - Django Migrations: `python manage.py makemigrations`
    - Django Migrate: `python manage.py migrate`
    - Django DBShell: `python manage.py dbshell`
    - Django PyShell: `python manage.py shell`
    - Django Superuser: `python manage.py createsuperuser`
    - Django Test:
      `  python manage.py test
    pytest
    pytest --cov`
    - Django Settings: `DJANGO_SETTINGS_MODULE=api.settings.prod python manage.py runserver`

### Shell

    - DbShell Tables: `.tables`
    - DbShell Header: `.header ON`
    - DbShell Null: `.nullvalue NULL`

### PyShell

    - PyShell ORM Import: `from agenda.models import Categoria, Evento`
    - PyShell ORM Create: `Categoria.objects.create(nome="BackEnd")`
    - PyShell ORM Save: `categoria.save()`
    - PyShell ORM All: `Categoria.objects.all()`
    - PyShell ORM Filter: `Categoria.objects.filter(nome="BackEnd")`
    - PyShell ORM Object: `Categoria.objects.filter(nome="BackEnd")[0]`
    - PyShell ORM ForeignKey: `Evento(nome="Nome", categoria=Categoria.objects.filter(nome="BackEnd")[0])`
    - PyShell ORM Filter ForeignKey: `Evento.objects.filter(categoria__nome="BackEnd")`
    - PyShell ORM Filter Date: `Evento.objects.filter(data__gte=date.today())`
    - PyShell ORM Filter Unique: `Evento.objects.get(id=id)`

</details>
