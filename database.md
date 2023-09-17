# Databas langguage

## Mongo

- URI: `mongodb://<username>:<password>@<ip-address>:<port>/<database>?authSource=admin`

- Sem Auth: `MONGO_URI='mongodb://mongo:27017/mongo-dev'`
- Executar bash: `docker exec -it mongo bash`
- Conexão sem Auth: `mongo`

- Exibir dbs: `show dbs`
- Acesso admin: `use admin`
- Criar Adm: `db.createUser({user:"admin",pwd:"admin",roles:["root"]});`
- Exibir users: `show users`

- Acesso user: `use mongo-dev`
- Criar user: `db.createUser({user:"admin",pwd:"admin",roles:[{"role":"readWrite","db":"mongo-dev"}]});`
- Exibir users: `show users`

- Manifesto Auth: `command: [--auth]`
- Com auth: `MONGO_URI='mongodb://admin:admin@mongo:27017/mongo-dev'`
- Acessar mongo: `mongo mongo-local -u admin --authenticationDatabase admin -p`

mongoose.connect('mongodb://admin:admin@172.18.0.3:27017/?authSource=admin')
mongoose.connect('mongodb://admin:admin@mongo:27017/?authSource=admin')
