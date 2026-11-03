<p align="center">
  <strong>serveruler-redirect</strong>
</p>

<p align="center">
  <strong>Um bookmark. Dois destinos. O dia da semana decide.</strong><br />
  Redireciona para o Serveruler da empresa ou de casa sem escolher IP à mão.
</p>

---

## Por que existe

O mesmo hostname (DNS local ou favorito) precisa apontar para a LAN certa. Em dia útil, escritório; no fim de semana, casa. Esta página estática faz só isso.

## O que você ganha

| | |
|---|---|
| **Zero build** | HTML + JS no navegador |
| **Regra simples** | `COMPANY_DAYS` vs resto da semana |
| **Par com sync-local-ip** | Os IPs no arquivo podem ser atualizados pela ferramenta de sync |
| **Bookmark estável** | Um URL, dois destinos |

## Como funciona

```text
Abrir index.html
    ↓
dia ∈ COMPANY_DAYS ? COMPANY_IP_ADDRESS : HOME_IP_ADDRESS
    ↓
location → Serveruler Client
```

Cliente: [`serveruler-client`](https://github.com/RafaelHDSV/serveruler-client).

## Posicionamento

| redirect é | redirect não é |
|---|---|
| Página estática de decisão | Descoberta automática de IP |
| Companion do Serveruler | Servidor Node |
| Config por constantes | UI de settings |

## Começar

Constantes e exemplos: [`docs/ambiente-e-operacao.md`](docs/ambiente-e-operacao.md). Contexto: [`docs/context.md`](docs/context.md).

Contribuição: [`CONTRIBUTING.md`](CONTRIBUTING.md) · conduta: [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) · mudanças: [`CHANGELOG.md`](CHANGELOG.md).
