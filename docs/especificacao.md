# Especificação

> **Para que serve:** regra de redirect por dia da semana.
> **Fonte da verdade:** script em `index.html`.
> **Relacionados:** [context](context.md)

## Comportamento

1. Lê o dia (`0` domingo … `6` sábado).
2. Se o dia está em `COMPANY_DAYS`, vai para `COMPANY_IP_ADDRESS`.
3. Caso contrário, vai para `HOME_IP_ADDRESS`.

## O que não faz

- Não descobre IP sozinho (use `sync-local-ip` para atualizar os arquivos)
- Não tem build nem servidor próprio além de hospedagem estática
