# Upag Documentation

Documentação pública da API Upag (Mintlify, pt-BR): uma única API para Pix, cartão com 3D Secure, checkout, assinaturas, transferências, subcontas e webhooks, com os SDKs [`upag`](https://www.npmjs.com/package/upag) (Node.js) e [`upag-js`](https://www.npmjs.com/package/upag-js) (browser).

- Produção: `https://api.upag.io/v1`
- Sandbox: `https://api.upag.dev/v1` (chaves `sk_test_` / `pk_test_`)

## Estrutura

```
docs.json          navegação (abas Guias, Referência, Webhooks, SDK, Simulador) e redirects
pages/guides/      quickstart, autenticação, convenções, erros e fluxos
pages/<recurso>/   referência por recurso (reference, create, list, get, ...)
pages/webhooks/    visão geral, segurança, endpoints e payloads
pages/sdk/         SDKs upag e upag-js
pages/simulator    cartões de teste do sandbox
llm.txt            índice para LLMs
```

Os endpoints têm exemplos em cURL e no SDK. A fonte da verdade é o código da API (`apps/api/src/entrypoints/api` no repositório `pix-api`) e os SDKs `upag-node` e `upag-js`.

## Desenvolvimento

Instale a [Mintlify CLI](https://www.npmjs.com/package/mint) para visualizar as alterações:

```
npm i -g mint
```

Na raiz (onde está o `docs.json`):

```
mint dev
```

A prévia fica em `http://localhost:3000`. Para checar links quebrados: `mint broken-links`.

## Publicação

Com o GitHub app da Mintlify instalado, as alterações na branch padrão são publicadas automaticamente.

## Ajuda

- Se o ambiente não subir, rode `mint update`.
- Se uma página retornar 404, confirme que está na pasta com um `docs.json` válido.
- [Documentação da Mintlify](https://mintlify.com/docs)
