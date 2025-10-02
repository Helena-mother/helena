# Helena - Sistema de Gestão de Negócios Multi-Tenant

![Helena Logo](https://img.shields.io/badge/Helena-Business_Management-blue)
![Made in Angola](https://img.shields.io/badge/Made%20in-Angola-red)
![Status](https://img.shields.io/badge/Status-Active-success)

## 🇦🇴 Sobre a Helena

**Helena** é uma empresa angolana dedicada ao desenvolvimento de soluções tecnológicas inovadoras para a gestão empresarial. Nosso produto principal é uma aplicação multi-tenant completa que facilita a gestão de negócios de forma eficiente e integrada.

### O que é o Sistema Helena?

O Sistema Helena é uma plataforma completa de gestão empresarial desenvolvida para atender às necessidades de negócios de diversos portes. Com uma arquitetura multi-tenant, permitimos que múltiplas empresas utilizem a mesma infraestrutura de forma segura e isolada, mantendo seus dados protegidos e acessíveis.

## 🚀 Funcionalidades Principais

- **Multi-tenant**: Suporte para múltiplas empresas na mesma plataforma
- **Gestão de Vendas**: Controle completo de vendas e faturamento
- **Gestão de Estoque**: Controle de inventário e produtos
- **Gestão Financeira**: Controle de receitas, despesas e fluxo de caixa
- **Relatórios**: Dashboards e relatórios analíticos
- **Gestão de Clientes**: CRM integrado
- **Gestão de Funcionários**: Controle de RH e folha de pagamento
- **Multi-plataforma**: Disponível para Web, Desktop e Mobile

## 📥 Downloads

### Aplicação Mobile (Android)

Baixe a aplicação Helena para Android:

- **APK Direto**: [Download Helena.apk](#) *(em breve)*
- **Google Play Store**: [Ver na Play Store](#) *(em breve)*

**Requisitos:**
- Android 6.0 ou superior
- 100MB de espaço livre
- Conexão com internet

### Aplicação Desktop (Windows)

Baixe a aplicação Helena para Windows:

- **Instalador EXE**: [Download Helena-Setup.exe](#) *(em breve)*
- **Versão Portátil**: [Download Helena-Portable.zip](#) *(em breve)*

**Requisitos:**
- Windows 10 ou superior
- 4GB de RAM (recomendado)
- 500MB de espaço livre
- Conexão com internet

### Aplicação Web

Acesse nossa plataforma web diretamente pelo navegador:

🌐 **Portal Web**: [https://app.helena.ao](#) *(em breve)*

**Navegadores Suportados:**
- Google Chrome (recomendado)
- Mozilla Firefox
- Microsoft Edge
- Safari

## 🐳 Docker - Implantação em Rede Interna

Para empresas que desejam hospedar o sistema Helena em sua própria rede interna, oferecemos suporte completo via Docker com proxy para integração com suas contas web.

### Pré-requisitos

- Docker 20.10 ou superior
- Docker Compose 2.0 ou superior
- Conexão com internet (para autenticação inicial)
- Conta válida no portal web Helena

### Instalação Rápida

1. **Clone o repositório de configuração:**

```bash
git clone https://github.com/Helena-mother/helena-docker.git
cd helena-docker
```

2. **Configure suas credenciais:**

Crie um arquivo `.env` baseado no exemplo:

```bash
cp .env.example .env
nano .env
```

Edite o arquivo `.env` com suas informações:

```env
# Credenciais da sua conta Helena
HELENA_EMAIL=seu-email@empresa.ao
HELENA_TOKEN=seu-token-de-api

# Configurações do Proxy
PROXY_HOST=0.0.0.0
PROXY_PORT=8080

# Configurações do Banco de Dados
DB_HOST=localhost
DB_PORT=5432
DB_NAME=helena_db
DB_USER=helena
DB_PASSWORD=senha-segura-aqui
```

3. **Inicie os serviços:**

```bash
docker-compose up -d
```

4. **Verifique o status:**

```bash
docker-compose ps
```

### Configuração do Proxy

O proxy Helena permite que você use sua conta web existente enquanto executa o sistema em sua rede interna. Isso garante:

- ✅ Sincronização automática de dados
- ✅ Backups na nuvem
- ✅ Atualizações automáticas
- ✅ Suporte técnico remoto
- ✅ Funcionamento offline (dados em cache)

**Arquitetura do Proxy:**

```
Internet ←→ Proxy Helena ←→ Rede Interna ←→ Aplicações Locais
              (Docker)
```

### Portas Utilizadas

| Serviço          | Porta | Descrição                    |
|------------------|-------|------------------------------|
| Aplicação Web    | 8080  | Interface web principal      |
| API              | 8081  | API REST                     |
| Proxy            | 8082  | Proxy de sincronização       |
| PostgreSQL       | 5432  | Banco de dados               |
| Redis            | 6379  | Cache e sessões              |

### Comandos Úteis

```bash
# Iniciar serviços
docker-compose up -d

# Parar serviços
docker-compose down

# Ver logs
docker-compose logs -f

# Atualizar para versão mais recente
docker-compose pull
docker-compose up -d

# Backup do banco de dados
docker-compose exec db pg_dump -U helena helena_db > backup.sql

# Restaurar banco de dados
docker-compose exec -T db psql -U helena helena_db < backup.sql
```

### Solução de Problemas

**Problema: Não consigo conectar ao proxy**
```bash
# Verifique se o serviço está rodando
docker-compose ps

# Verifique os logs do proxy
docker-compose logs proxy
```

**Problema: Erro de autenticação**
```bash
# Verifique suas credenciais no arquivo .env
# Regenere seu token no portal web se necessário
```

## 📖 Documentação Completa

Para documentação detalhada, visite:

- 📚 **Wiki**: [https://github.com/Helena-mother/helena/wiki](#)
- 📘 **API Docs**: [https://api.helena.ao/docs](#)
- 🎥 **Vídeos Tutorial**: [https://youtube.com/@helena-ao](#)

## 🤝 Suporte e Contato

### Suporte Técnico

- 📧 **Email**: suporte@helena.ao
- 💬 **WhatsApp**: +244 XXX XXX XXX
- 🎫 **Portal de Suporte**: [https://suporte.helena.ao](#)

### Horário de Atendimento

- Segunda a Sexta: 08:00 - 18:00 (WAT)
- Sábado: 09:00 - 13:00 (WAT)
- Emergências 24/7 para clientes empresariais

### Redes Sociais

- 🔵 **Facebook**: [@HelenaAngola](#)
- 📸 **Instagram**: [@helena.ao](#)
- 💼 **LinkedIn**: [Helena Business Solutions](#)
- 🐦 **Twitter**: [@HelenaAO](#)

## 📄 Licença

Este projeto é propriedade da Helena - Business Solutions, Angola.

Para informações sobre licenciamento empresarial, entre em contato conosco.

## 🌟 Desenvolvido em Angola 🇦🇴

Orgulhosamente desenvolvido em Angola, para Angola e para o mundo.

---

© 2024 Helena - Business Solutions. Todos os direitos reservados.