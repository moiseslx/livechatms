# 💬 Live Chat Microservice

Este é um microserviço de chat em tempo real desenvolvido com **Spring Boot**, utilizando **WebSocket** com suporte a **STOMP**. A aplicação permite que mensagens enviadas por um usuário sejam transmitidas para todos os outros conectados ao canal.

## 📦 Tecnologias Utilizadas

- Java 21
- Spring Boot
- Spring WebSocket
- STOMP
- SockJS
- HTML/JS

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/livechat-ms.git
   cd livechat-ms
   ```

2. Execute a aplicação:
   ```bash
   ./mvnw spring-boot:run
   ```

   A aplicação estará disponível em: `http://localhost:8080`

---

## 📡 Endpoints WebSocket

- **Conexão WebSocket**:  
  ```
  ws://localhost:8080/buildrun-livechat-websocket
  ```

- **Prefixo da aplicação**:
  ```
  /app
  ```

- **Envio de mensagens**:
  ```
  /app/new-message
  ```

- **Assinatura de mensagens**:
  ```
  /topics/livechat
  ```

---

## 💬 Formato das Mensagens

### 📥 Envio (ChatInput)

```json
{
  "user": "MeuLord",
  "message": "Salve o chat!"
}
```

### 📤 Resposta (ChatOutput)

```json
{
  "content": "[MeuLord]: Salve o chat!"
}
```
