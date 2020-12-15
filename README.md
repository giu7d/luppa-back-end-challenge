# Luppa Back-End Challenge

O objetivo deste desafio é avaliar seu domínio em desenvolvimento back-end e onde suas habilidades tem maior destaque. Este documento descreve o que esperamos e recomendamos na sua implementação.

Não é necessário que você entregue 100% da aplicação. Ainda que iremos avaliar o quanto você implementou, não é o indicador mais importante na nossa avaliação. A ideia principal deste desafio é que ele nos permita conhecer como você desenvolve e quais são os seus conhecimentos e experiências.

## O Desafio

A aplicação proposta neste desafio é uma API de análise de documentos para identificação de fraudes. Abaixo estão relacionados os endpoints que gostaríamos de ver na aplicação e alguns exemplos de resposta.

**Importante:** Não esperamos que você realmente faça essa análise (apenas a gere aleatoriamente).

### Criar Análise

#### Requisição

```
{
  "fullName": "Nome Completo",
  "cpf": "000.111.222-00",
  "documents": [""] // ou Array com URL ou Base64
}
```

#### Resposta

```
{
  "analysisId": "id da analise"
}
```

**Importante:** Você deve apenas criar um `job assíncrono` que adicione o status de cada document como `fraud`, `valid` ou `error` (aleatoriamente) no banco de dados.

### Listar Análises

#### Resposta

```
[
  {
    "analysisId": "id da analise",
    "fullName": "Nome Completo",
    "cpf": "000.111.222-00",
    "analyzedAt": "date",
    "documents": [
      {
        "id": "id do doc",
        "status": "valid", // fraud, valid ou error
        "src": "http://..." // link para o documento
      }
    ]
  }
]
```

### Mostrar Análise Especifica

#### Resposta

```
{
  "analysisId": "id da analise",
  "fullName": "Nome Completo",
  "cpf": "000.111.222-00",
  "analyzedAt": "date",
  "documents": [
    {
      "id": "id do doc",
      "status": "valid", // fraud, valid ou error
      "src": "http://..." // link para o documento
    }
  ]
}
```

## Requisitos

- README com instruções de uso da aplicação
- Versionamento usando Git
- Seguir a especificação REST usando JSON

## Recomendações

Os itens abaixo são aqueles geralmente utilizados em nossos projetos. Eles não são obrigatórios, mas podem te ajudar a entender o nosso dia-a-dia.

- NodeJS
- Typescript
- TypeORM (utilizando Postgres)
- Redis
- Jest
- Código e documentação
- Build para produção com Babel

## O que será avaliado

- Clean code, SOLID e DRY
- Testes unitários e de integração
- Design patterns

## Diferenciais

- Docker
- CI/CD
- Swagger/OpenAPI
- Versionamento do banco de dados
- Tratamento de erros
- Paginação, ordenação e projeção
