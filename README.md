# Rate Limiter


## Passos para execução:

- docker-compose up -d

- Testes em cmd/middleware/limiter_test.go
  
## Constantes de configuração - localizadas no arquivo .env
* ENABLE_RATE_LIMIT_BY_IP
    - Permite que o limite de taxa funcione por IP quando seu valor for [true]

* ENABLE_RATE_LIMIT_BY_TOKEN
    - Permite que o limite de taxa funcione em Tokens quando seu valor for [true]

* MAX_REQUESTS_BY_IP
    - Define o valor máximo de solicitações recebidas por segundo por um IP (Exemplo: [10])

* BLOCK_DURATION_IP 
    - Define o tempo em minutos que um IP ficará bloqueado para executar novas requisições (Exemplo: [1])

* BLOCK_DURATION_TOKEN
    - Define o tempo em minutos que um TOKEN ficará bloqueado para executar novas requisições (Exemplo: [1])

* TOKEN_LIMIT_LIST 
    - Define o valor máximo de solicitações recebidas por segundo por um Token específico (Exemplo: [{ "ABC123": 2, "ABC456": 4, "DEF122": 5}])

* STORAGE_TYPE
    - Define o tipo de armazenamento que o aplicativo utilizará
        - Defina-o como [redis] se quiser redis
        - Qualquer outro valor (ou nenhum) o aplicativo usará um armazenamento na memória

