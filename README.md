# Database

## :dart: Overview

<details>
<summary>:package: Mongo</summary>

**:mailbox_with_no_mail: Comandos**

- URI:

  ```
  mongodb://<username>:<password>@<ip-address>:<port>/<database>?authSource=admin
  mongodb://<ip-address>:<port>/<database>
  ```

- Access bash:

  ```
  docker exec -it mongo bash
  docker exec -it mongo mongo -u<username> -p<password>
  docker exec -it mongo mongo
  mongo <database> -u <username> --authenticationDatabase <password> -p

  show dbs
  use <database>
  show users
  use admin
  db.createUser({user:"admin",pwd:"admin",roles:["root"]});
  db.createUser({user:"admin",pwd:"admin",roles:[{"role":"readWrite","db":"mongo-dev"}]});
  ```

</details>

<details>
<summary>:package: PostgreSQL</summary>

**:mailbox_with_no_mail: Comandos**

- Access bash:
  ```
  docker exec -it <service-name> psql -U <username> <database>

  \dt
  SELECT * FROM pg_catalog.<table>;
  ```

</details>

