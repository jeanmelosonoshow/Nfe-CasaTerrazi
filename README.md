# Nfe-CasaTerrazi

Pagina publica para consulta de DANFE da Casa Terrazi.

## API da Vercel

O projeto chama a rota local da Vercel:

```js
const CONFIG = {
  apiUrl: "/api/nfe",
};
```

A rota `api/nfe.js` recebe:

```txt
POST /api/nfe
```

com o corpo:

```json
{ "chave": "33260505507218000150550050000097861003827552" }
```

e responde:

```json
{ "xml": "<?xml version=\"1.0\" encoding=\"UTF-8\"?><nfeProc..." }
```

## Variaveis da Vercel

Use as mesmas variaveis de conexao Firebird:

```txt
DB_HOST_FB
DB_PORT_FB
DB_PATH_FB
DB_USER_FB
DB_PASSWORD_FB
```

Se algum dia precisar trocar a consulta sem alterar o codigo, configure:

```txt
NFE_XML_SQL
NFE_XML_FIELD
```

O campo padrao de retorno e `XMLNFE`.
