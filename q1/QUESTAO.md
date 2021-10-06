# Backend - Q1

Valor: 1.5 pt

Corrija e otimize o Dockerfile existente no diretório.
O projeto inicial buildado pesará, aproximadamente, 1.1GB.

🏋️ Reduza o peso geral da imagem o máximo possível.  
⏰ Reduza o tempo de build o máximo que conseguir. Considere que o código pode mudar.

Crie uma versão "Dockerfile.otimizado" contendo suas alterações e mantenha o original.

Para executar o build, utilize o script bash ```docker-build.bash``` disponibilizado:

```bash
bash docker-build.bash -t q1:dev .
```

O script irá gerar um JSON contendo os tempos de build em cada etapa.
Compartilhe a saída JSON do bash executado, tal como o exemplo abaixo:

```json
[
  {
    "time": 1632846937,
    "step": 0,
    "cmd": "START"
  },
  {
    "time": 1632846958,
    "step": 1,
    "cmd": "FROM python:latest"
  },
  {...}
]
```

Descreva abaixo, em poucas linhas, o que você fez e por que o fez para melhorar o
Dockerfile e colocar o projeto para funcionar.

---

Correção 1:
  Troca da imagem base - Foi utilizado uma imagem da versão 3.9 do python( versão recente) com os pacotes mínimos necessários para rodar o python ```FROM python:3.9-slim-buster```      
  
Correção 2:
  Bibliotecas desnecessárias - Foram comentadas bilbiotecas consideradas desnecessárias a execução do código (algumas bibliotecas excluídas foram requisitadas por dependência posteriormente)
 
Resultado :   tamanho da imagem ficou em 327MB

