# Regras de negócio

> **Para que serve:** algoritmos e regras do domínio que a IA não deve reinventar
> **Fonte da verdade:** módulos de domínio no código
> **Relacionados:** [especificacao](especificacao.md) · [api](api.md) · [banco-de-dados](banco-de-dados.md)

## Regras

1. Lê o dia (`0` domingo … `6` sábado).
2. Se o dia está em `COMPANY_DAYS`, vai para `COMPANY_IP_ADDRESS`.
3. Caso contrário, vai para `HOME_IP_ADDRESS`.
