# serveruler-redirect

Página estática que redireciona automaticamente para a instância do cliente [Serveruler](https://github.com/joaolfern/serveruler-client) (Vite) conforme o dia da semana: rede da empresa em dias úteis e rede de casa nos demais dias.

Útil quando você acessa sempre o mesmo hostname (por exemplo via DNS local ou bookmark) e quer que o destino mude sem escolher manualmente o IP.

## Como funciona

O `index.html` executa um script que:

1. Lê o dia da semana (`0` = domingo … `6` = sábado).
2. Verifica se o dia está em `COMPANY_DAYS` (por padrão segunda a sexta: `1`–`5`).
3. Redireciona para `COMPANY_IP_ADDRESS` ou `HOME_IP_ADDRESS`.

Não há build nem dependências — apenas HTML e JavaScript no navegador.

## Configuração

Edite as constantes no início do script em [`index.html`](index.html):

| Constante | Descrição |
|-----------|-----------|
| `COMPANY_DAYS` | Array com os dias em que vale o IP da empresa (`0`–`6`) |
| `COMPANY_IP_ADDRESS` | URL completa do Serveruler na rede corporativa |
| `HOME_IP_ADDRESS` | URL completa do Serveruler em casa |

Exemplo:

```javascript
const COMPANY_DAYS = [1, 2, 3, 4, 5];
const COMPANY_IP_ADDRESS = "http://10.10.0.154:5173/";
const HOME_IP_ADDRESS = "http://172.24.0.189:5173/";
```

Os endereços acima são exemplos de rede local; ajuste para os IPs/portas do seu ambiente.

## Uso local

Sirva a pasta com qualquer servidor estático. Exemplos:

```bash
# Python
python -m http.server 8080

# Node (npx, sem instalar no projeto)
npx serve .
```

Abra `http://localhost:8080` (ou a porta escolhida). O navegador será redirecionado imediatamente.

## Deploy

Publique o conteúdo da raiz (principalmente `index.html` e `favicon.ico`, se existir) em:

- GitHub Pages
- nginx / Apache
- qualquer host de arquivos estáticos

Garanta que a URL raiz sirva `index.html` como documento padrão.

## Estrutura

```
serveruler-redirect/
├── index.html    # lógica de redirecionamento
├── README.md
├── LICENSE
└── .gitignore
```

## Licença

MIT — ver [LICENSE](LICENSE).
