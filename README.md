 AngelChat
=========

`AngelChat` é um app de atendimento ao vivo e CRM. 


Desenvolvido para integrar com um CRM ou E-commerce, ele recebe os parâmetros externos para `produtos`, e ajuda a simular `frete`

Rotas
----

  Cliente
  ----
  - `/atendimento` cliente que acessa o atendimento

   Operador
   ----
  - `/operador` Funcionário que atende.
  - `/operador/respostas` get: exibe todas respostas | post: cria nova
  - `/operador/respostas/:id` put: Atualiza resposta | delete: Apaga

  Campos
  -----
  Os campos são os seguintes:
  Resposta
  ------
   Respostas são pré-definidas para perguntas que acontecem com muita frequencia.
   Elas podem ser inseridas à qualquer momento pela rota `/operador/respostas/`,
   atualizadas pelo `/operador/respostas/:id` `PUT` e del na mesma rota com `DELETE`

   São constituidas por:
 - `name`: String
 - `criadoPor`: `{nome: String, refId: mongoose.Schema.ObjectId }`,
 - `criadoEm`: Date;
 - `content`: String,
 - `tipo`: String,
 - `published`: `true`, ou `false`
