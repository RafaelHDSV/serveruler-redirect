# Ambiente e operação

> **Para que serve:** configurar os IPs do redirect.
> **Fonte da verdade:** constantes no `index.html`.
> **Relacionados:** [context](context.md)

Edite no início do script em `index.html`:

| Constante | Descrição |
|---|---|
| `COMPANY_DAYS` | Dias da empresa (`0`–`6`) |
| `COMPANY_IP_ADDRESS` | URL completa do Serveruler na LAN corporativa |
| `HOME_IP_ADDRESS` | URL completa em casa |

Exemplo:

```javascript
const COMPANY_DAYS = [1, 2, 3, 4, 5];
const COMPANY_IP_ADDRESS = "http://10.10.0.154:5173/";
const HOME_IP_ADDRESS = "http://172.24.0.189:5173/";
```

Sirva o `index.html` como estático (qualquer host local ou bookmark + file/DNS interno).
