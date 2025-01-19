# event-management-system

## Descrição
Sistema modular para organização e gerenciamento de eventos, como conferências, workshops, feiras e shows. A plataforma permite que organizadores criem, personalizem e acompanhem eventos com facilidade, além de gerenciar inscrições e enviar notificações automatizadas aos participantes. Com arquitetura baseada em microserviços, o sistema utiliza autenticação segura via AWS Cognito e oferece alta resiliência e escalabilidade ao integrar tecnologias como DynamoDB para armazenamento, SQS para filas de mensagens e SNS para envio de notificações. Simplifica processos complexos e melhora a experiência tanto para organizadores quanto para o público.

## Arquitetura

Arquitetura modular baseada em microserviços.
- **Módulos**:
  - **auth-service**: Gerencia autenticação e autorização, integrando-se ao AWS Cognito.
  - **event-service**: CRUD de eventos, incluindo criação, edição, exclusão e listagem.
  - **participant-service**: Inscrições e gerenciamento de participantes em eventos.
  - **notification-service**: Processa notificações e envia mensagens via AWS SNS.
  - **api-gateway**: Centraliza o roteamento, autenticação e controle de acesso.
  - **common**: Código compartilhado entre os serviços, como DTOs e utilitários.
