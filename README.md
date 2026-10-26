# FakeStoreAPI — QA Squad

Collection do Postman para validar endpoints de usuários, autenticação e carrinhos da [FakeStoreAPI](https://fakestoreapi.com).

## Como executar

1. Importe `FakeStoreAPI - QA SQUAD.postman_collection.json` no Postman.
2. Confira a variável `baseUrl` (`https://fakestoreapi.com`) na collection.
3. Execute os requests individualmente ou a pasta **01 - Happy path** em ordem.
4. Consulte os resultados na aba **Test Results**.

## Cenários

| Pasta | O que valida |
| --- | --- |
| **01 - Happy path** | Lista usuários e carrinhos, faz login e solicita a exclusão do usuário `1`. |
| **02 - Negative testing** | Login com senha incorreta, sem senha, JSON inválido e exclusão com ID inválido. |
| **03 - Extra test: login status** | Cenário demonstrativo que espera HTTP `200` no login. |

O login no fluxo principal espera HTTP `201`. A pasta extra espera `200` e, conforme descrito na collection, falha com a resposta atual da API (`201`).

## Observações

- A API é de demonstração: operações de escrita e exclusão podem não persistir alterações.
- A resposta de usuários pode conter senhas. Não compartilhe respostas brutas nem credenciais.
- O teste de login verifica a presença do token, mas não testa seu uso ou validade.
