graph TD
  A[Início: Análise do Suporte] --> B[Abertura de Demanda do Produto]
  B --> C[Levantar o máximo de informações com o cliente]
  C --> D{Tipo de cliente}
  D -->|Clínicas usando nosso servidor| E[Incluir na fila "Clínicas MKData"]
  D -->|Outros clientes| F[Incluir na fila da organização]
  E --> G[Definir status do chamado como "Enviado para Produto"]
  F --> G
  G --> H[Agente acompanha o chamado até entrega]
  H --> I{Chamado homologado?}
  I -->|Sim| J[Fim do Processo]
  I -->|Não| K[Cliente devolve chamado para ajustes]
  K --> H
