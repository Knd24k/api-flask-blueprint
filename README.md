## Servidores e Portas 
| Serviço | Porta  |
|--|--|
| flask|
| python|
| mysql-connector-python | <definir> |
| flask_cors |

## Cria o seu ambiente virtual

```php
https://flask.palletsprojects.com/en/3.0.x/installation/
```

## Execute os seguintes comando dentro do ambiente virtual

```php
pip install flask
pip install mysql-connector-python
pip install flask_cors
```
## Execute a Aplicação

```php
python3 app.py 
```

# API VENDAS

### DOCUMENTAÇÃO

## Iniciar o Serviço

Essas instruções ajudarão você a executar uma cópia do projeto em sua máquina local para desenvolvimento e testes. Para informações sobre como implantar o projeto em um sistema ativo, consulte a seção de implantação.

## Funcionalidades para o usuário

### Criar Usuário
- **Método**: POST
- **URL**: `/usuario`
- **Campos**:
  1. `name`
  2. `email`
  3. `password`
  4. `is_active`
  5. `cpf_cnpj`

**Exemplo de `curl`**:

```bash
curl -X POST http://localhost:8080/usuario \
     -H "Content-Type: application/json" \
     -d '{
           "name": "John Doe",
           "email": "john.doe@example.com",
           "password": "password123",
           "is_active": true,
           "cpf_cnpj": "12345678901"
         }'
```
### Atualizar Usuário
- **Método**: PUT
- **URL**: `/usuario/{id}`
- **Campos**:
  1. `name`
  2. `email`
  3. `password`
  4. `is_active`
  5. `cpf_cnpj`

**Exemplo de `curl`**:

```bash
curl -X PUT http://localhost:8080/usuario \
     -H "Content-Type: application/json" \
     -d '{
           "name": "John Doe",
           "email": "john.doe@example.com",
           "password": "password123",
           "is_active": true,
           "cpf_cnpj": "12345678901"
         }'
```
### Encontrar Usuário pelo ID
- **Método**: GET
- **URL**: `/usuario/{id}`

**Exemplo de `curl`**:

```bash
curl -X GET http://localhost:8080/usuario/{id}
```

### Inativar ou Ativar usuário pelo ID
- **Método**: PUT
- **URL**: `/usuario/{id}/status`
- **Campos**:  
  1. `is_active`
  
**Exemplo de `curl`**:

```bash
curl -X PUT http://localhost:8080/usuario/{id}/status \
     -H "Content-Type: application/json" \
     -d '{
           "is_active": false
         }'

```
