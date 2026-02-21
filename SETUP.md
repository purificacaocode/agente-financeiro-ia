# 🚀 GUIA DE SETUP - AGENTE FINANCEIRO INTELIGENTE

## Pré-requisitos
- Docker e Docker Compose instalados
- VPS ou Render com acesso SSH
- OpenRouter API Key (fornecida)
- Google Sheets OAuth2 configurado

## ⚡ INÍCIO RÁPIDO

### 1. Clonar o repositório
```bash
git clone https://github.com/purificacaocode/agente-financeiro-ia.git
cd agente-financeiro-ia
```

### 2. Configurar variáveis de ambiente
```bash
cp .env.example .env
# Edite .env e atualize com seus dados
```

### 3. Subir os containers
```bash
docker-compose up -d
```

### 4. Verificar status
```bash
docker-compose ps
```

## 🔧 CONFIGURAÇÕES

### Evolution API - WhatsApp
1. Aguarde que a API esteja rodando
2. Acesse o swagger: `http://localhost:8080/api/swagger`
3. Gere uma nova instância com QR Code
4. Escaneie com seu WhatsApp pessoal

### n8n - Workflow
1. Acesse: `https://seu-dominio:5678`
2. Configure as credenciais:
   - OpenRouter API Key
   - Google Sheets OAuth2
   - Evolution API Endpoint
3. Crie o workflow conforme documentado

## 📋 Logs e Troubleshooting

```bash
# Ver logs da Evolution
docker logs evolution-api

# Ver logs do n8n
docker logs n8n-agente

# Ver logs do MongoDB
docker logs evolution-mongo

# Reiniciar containers
docker-compose restart
```

## 🎯 Próximas etapas

1. Configuraré System Prompt no n8n (veja documentação completa)
2. Configure os nodes do workflow
3. Teste com mensagens como:
   - "Ganhei 3000 de salário"
   - "Gastei 150 no mercado no crédito"
   - "Reservei 500 para emergência"

## 📚 Documentação completa

Para documentação detalhada sobre System Prompt, workflow n8n e testes, veja:
https://docs.google.com/document/d/1o87LezXFexIcpYIKlg8qgdn3wZOZRWBH0jPwIjlC7iw/

## 📞 Suporte

Para dúvidas sobre a integração ou testes, abra uma issue neste repositório.
