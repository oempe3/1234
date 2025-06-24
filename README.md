# Sistema de Monitoramento de Equipamentos - Pernambuco III

## 📋 Descrição

Sistema reformulado para monitoramento e controle de status de equipamentos da UTE Pernambuco III, com interface moderna e funcionalidades avançadas de edição linha a linha.

## 🚀 Funcionalidades Implementadas

### ✅ Sistema de Login
- **Senha fixa**: `p3rnambuco3`
- **Redirecionamento automático** para página status após login
- **Interface moderna** com design responsivo

### ✅ Página Status
- **Classificação semáforo** com indicadores visuais:
  - 🟢 **OPE** (Verde): Em Operação
  - 🟡 **ST-BY** (Amarelo): Stand-by
  - 🔴 **MNT** (Vermelho): Em Manutenção
- **Filtros interativos**: Clique nos quadros para filtrar
- **Texto atualizado**: "Previsão para retorno" em vez de "Retorno"
- **Navegação simplificada**: Link único para entrada de dados

### ✅ Página Entrada (Reformulada)
- **Layout moderno tipo Flutter**
- **Edição linha a linha** com seleção na tabela
- **Filtros avançados** por equipamento e status
- **Validação de dados automática**
- **Campos condicionais** baseados no status selecionado

## 🎯 Como Usar

### 1. Acesso ao Sistema
1. Abra o arquivo `index.html` no navegador
2. Digite qualquer usuário (campo obrigatório)
3. Digite a senha: `p3rnambuco3`
4. Clique em "Entrar"

### 2. Visualização de Status
- **Página Status**: Visualize todos os equipamentos com classificação semáforo
- **Filtros interativos**: Clique nos quadros coloridos para filtrar por status
- **Busca**: Use o campo de busca para encontrar equipamentos específicos
- **Atualização**: Clique em "Atualizar" para recarregar os dados

### 3. Edição de Dados
1. **Acesse**: Clique em "Entrada de Dados" no menu
2. **Filtre**: Use os filtros à esquerda para encontrar equipamentos
3. **Selecione**: Clique em uma linha da tabela para editar
4. **Configure Status**: Escolha o status (ST-BY, MNT, OPE)
5. **Preencha Campos**: Complete os campos conforme o status:

#### Para ST-BY (Stand-by):
- **Motivo**: Conveniência operacional ou do sistema
- **Observações**: Texto livre (máx. 100 caracteres)
- **Modificado Por**: Nome do responsável
- **Data e Hora**: Timestamp da modificação

#### Para MNT (Manutenção):
- **Motivo**: Corretiva, preventiva ou preditiva
- **PTS**: Número da Permissão de Trabalho
- **OS**: Número da Ordem de Serviço
- **Observações**: Texto livre (máx. 100 caracteres)
- **Modificado Por**: Nome do responsável
- **Data e Hora**: Timestamp da modificação

#### Para OPE (Operação):
- **Modificado Por**: Nome do responsável
- **Data e Hora**: Timestamp da modificação

6. **Salve**: Clique em "Salvar Alterações"

## 📁 Estrutura de Arquivos

```
status/
├── index.html          # Página de login
├── status.html         # Página de visualização de status
├── entrada.html        # Página de entrada de dados (reformulada)
├── style.css          # Estilos CSS
├── logomarca.png      # Logo da empresa
├── favicon.png        # Ícone do site
└── README.md          # Este arquivo
```

## 🔧 Configuração

### Integração com Google Sheets
O sistema está configurado para integrar com Google Sheets através do endpoint:
```
https://script.google.com/macros/s/AKfycbwSwlJATYl9L0GHOwNrGzRnhRsrNbaZedUd0lLGujwiF4noP8xHP8dUH9SrfVh7fAi0Sw/exec
```

### Estrutura da Planilha
- **Coluna A**: TAG do equipamento
- **Coluna B**: STATUS (ST-BY, MNT, OPE)
- **Coluna C**: MOTIVO
- **Coluna D**: PTS
- **Coluna E**: OS
- **Coluna F**: RETORNO
- **Coluna G**: CADEADO
- **Coluna H**: OBSERVACOES
- **Coluna I**: MODIFICADO_POR
- **Coluna J**: DATA

## 🎨 Características do Design

### Layout Moderno
- **Design tipo Flutter**: Interface clean e moderna
- **Responsivo**: Funciona em desktop e mobile
- **Cores semáforo**: Indicadores visuais intuitivos
- **Transições suaves**: Animações e efeitos visuais
- **Tipografia moderna**: Fonte Inter para melhor legibilidade

### Experiência do Usuário
- **Navegação intuitiva**: Fluxo lógico entre páginas
- **Feedback visual**: Mensagens de sucesso/erro
- **Loading states**: Indicadores de carregamento
- **Validação em tempo real**: Verificação instantânea de dados
- **Campos condicionais**: Interface adaptativa baseada no contexto

## 🔒 Segurança

- **Validação de entrada**: Todos os campos são validados
- **Sanitização de dados**: Prevenção contra injeção de código
- **Controle de sessão**: Timeout automático
- **Logs de auditoria**: Registro de todas as alterações

## 📱 Compatibilidade

### Navegadores Suportados
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### Dispositivos
- ✅ Desktop (1024px+)
- ✅ Tablet (768px - 1023px)
- ✅ Mobile (320px - 767px)

## 🐛 Solução de Problemas

### Erro ao Carregar Equipamentos
- **Causa**: Problema de conectividade com Google Sheets
- **Solução**: Verificar conexão de internet e configuração do endpoint

### Login Não Funciona
- **Causa**: Senha incorreta ou campos vazios
- **Solução**: Usar senha `p3rnambuco3` e preencher campo usuário

### Dados Não Salvam
- **Causa**: Problema na integração com Google Sheets
- **Solução**: Verificar permissões e configuração do Google Apps Script

## 📞 Suporte

Para suporte técnico ou dúvidas sobre o sistema, consulte o arquivo `SUGESTOES_MELHORIAS.md` para ideias de evolução do sistema.

## 📄 Licença

Sistema desenvolvido para uso interno da UTE Pernambuco III.

---

**Versão**: 2.0  
**Data**: Junho 2025  
**Status**: Produção

