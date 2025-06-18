# 🚀 WhatsApp Bot Platform

Uma plataforma moderna e completa para gerenciamento de bots do WhatsApp com funcionalidades avançadas de KYC, estatísticas e interações.

## ✨ Funcionalidades

### 🔐 Sistema KYC (Know Your Customer)
- **Validação de CPF** - Algoritmo oficial do Ministério da Fazenda
- **Normalização de telefones brasileiros** - Trata automaticamente o nono dígito
- **Correspondência inteligente** - WhatsApp JID vs formulários
- **Documentos e verificações** - Upload e visualização de documentos
- **Alertas de menor de idade** - Detecção automática

### 📊 Dashboard e Estatísticas
- **Estatísticas em tempo real** - Membros, admins, atividade
- **Gráficos interativos** - Recharts com dados visuais
- **Períodos personalizáveis** - 7, 15, 30 dias ou customizado
- **Métricas detalhadas** - Crescimento, engagement, demographics

### 🎯 Interações Avançadas
- **Enquetes (Polls)** - Criação e gerenciamento com resultados
- **Sorteios (Raffles)** - Sistema completo de sorteios
- **Mensagens** - Interface de chat integrada
- **Automações** - Respostas automáticas e fluxos

### 👥 Gerenciamento de Grupos
- **Lista de membros** - Visualização em lista ou grade
- **Busca inteligente** - Por nome, telefone ou dados KYC
- **Administradores** - Controle de permissões
- **Configurações** - Privacidade e configurações de grupo

## 🛠️ Tecnologias

- **Frontend**: React 18 + TypeScript + Vite
- **Styling**: Tailwind CSS + Design System moderno
- **Estado**: Zustand para gerenciamento de estado
- **Banco de Dados**: Supabase (PostgreSQL)
- **API**: Integração com Whapi.cloud
- **Roteamento**: React Router DOM v7
- **Gráficos**: Recharts
- **Notificações**: React Hot Toast

## 📱 Design

- **Interface moderna** - Inspirada no design system da Apple
- **Responsivo** - Funciona perfeitamente em mobile e desktop
- **Tema escuro** - Interface elegante com glassmorphism
- **Animações suaves** - Transições e loading states
- **Acessibilidade** - Seguindo padrões WCAG

## 🚀 Instalação

1. **Clone o repositório**
   ```bash
   git clone https://github.com/MobiusCm/whatsapp-bot-platform.git
   cd whatsapp-bot-platform
   ```

2. **Instale as dependências**
   ```bash
   npm install
   ```

3. **Configure as variáveis de ambiente**
   ```bash
   cp .env.example .env
   # Configure suas chaves da Whapi e Supabase
   ```

4. **Execute o projeto**
   ```bash
   npm run dev
   ```

## ⚙️ Configuração

### Whapi Cloud
1. Crie uma conta em [whapi.cloud](https://whapi.cloud)
2. Obtenha sua API key
3. Configure o webhook para receber eventos

### Supabase
1. Crie um projeto no [Supabase](https://supabase.com)
2. Execute o schema SQL fornecido
3. Configure as chaves de API

### Variáveis de Ambiente
```env
VITE_WHAPI_BASE_URL=https://api.whapi.cloud
VITE_WHAPI_API_KEY=your_whapi_key
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

## 📋 Schema do Banco

O projeto inclui um schema completo do Supabase com:
- Tabela `form_applicants` para dados KYC
- Tabela `group_members` para membros customizados
- Triggers e funções para automação

## 🔧 Funcionalidades Técnicas

### Normalização de Telefones Brasileiros
O sistema implementa uma normalização inteligente que:
- **Detecta números brasileiros** (começam com 55)
- **Trata o nono dígito** automaticamente
- **Mantém compatibilidade internacional**
- **Resolve JID do WhatsApp vs formulários**

```typescript
// Exemplo de uso
const variations = normalizePhoneBR('5547997305829');
// Retorna: ['47997305829', '4797305829', '5547997305829', ...]
```

### Sistema de Cache Inteligente
- **Cache em memória** para dados KYC
- **Expiração automática** (5 minutos)
- **Busca em lote** otimizada
- **Invalidação inteligente**

## 🎨 Componentes Principais

- **GroupDetailView** - Visualização completa de grupos
- **MembersList** - Lista inteligente de membros
- **InteractionsView** - Gerenciamento de interações
- **GroupStatsTab** - Dashboard de estatísticas
- **KYC Modal** - Interface de verificação KYC

## 📈 Performance

- **Build otimizado** com Vite
- **Code splitting** automático
- **Lazy loading** de componentes
- **Bundle size** otimizado
- **TypeScript** para type safety

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add: Amazing Feature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para detalhes.

## 🆘 Suporte

Para suporte e dúvidas:
- Abra uma [issue](https://github.com/MobiusCm/whatsapp-bot-platform/issues)
- Entre em contato via email

---

⭐ **Desenvolvido com muito ❤️ para a comunidade WhatsApp Bot**