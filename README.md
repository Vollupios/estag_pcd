# Gerador de Relatório de Contratação

Uma aplicação web para análise automática de necessidades de contratação de **Estagiários** e **Pessoas com Deficiência (PCD)** com base na legislação brasileira.

## 📋 Descrição

Esta ferramenta processa arquivos CSV com dados de empresas e funcionários para gerar relatórios detalhados sobre as cotas obrigatórias de contratação, incluindo:

- **Estagiários**: Para empresas com regime diferente de "Simples Nacional" e "Sem Regime", com 7+ funcionários
- **PCD**: Para empresas com 100+ funcionários

## ✨ Funcionalidades

- 📊 **Análise Automática**: Processamento de dados CSV com cálculo automático das cotas
- 📈 **Visualizações**: Gráficos de barras interativos mostrando as empresas com maior necessidade de contratação
- 📋 **Tabelas Detalhadas**: Listagem completa das empresas elegíveis com número de funcionários ativos e vagas necessárias
- 📄 **Relatório PDF**: Geração de relatório completo em PDF com gráficos e tabelas
- 🔍 **Interface Responsiva**: Design adaptativo para desktop e mobile

## 🎯 Critérios de Contratação

### Estagiários

- **Empresas elegíveis**: Regime diferente de "Simples Nacional" e "Sem Regime"
- **Mínimo de funcionários**: 7 ou mais funcionários ativos
- **Cota**: 5% do total de funcionários ativos (arredondado para cima)

### Pessoas com Deficiência (PCD)

- **Empresas elegíveis**: Todas as empresas
- **Mínimo de funcionários**: 100 ou mais funcionários ativos
- **Cotas por faixa**:
  - 100 a 200 funcionários: 2%
  - 201 a 500 funcionários: 3%
  - 501 a 1000 funcionários: 4%
  - Mais de 1000 funcionários: 5%

## 🚀 Como Usar

1. **Prepare o arquivo CSV** com as seguintes colunas obrigatórias:
   - `Nome_Empresa`: Nome da empresa
   - `ativos`: Número de funcionários ativos (formato numérico)
   - `Regime federal`: Regime tributário da empresa

2. **Abra o arquivo** `estag_pcd.html` em um navegador web moderno

3. **Carregue o arquivo CSV** clicando em "Selecione o arquivo CSV"

4. **Gere o relatório** clicando em "Gerar Relatório"

5. **Visualize os resultados** através dos gráficos e tabelas gerados

6. **Baixe o PDF** clicando em "Baixar Relatório PDF" (se disponível)

## 📁 Estrutura de Arquivos

```text
📂 PCD's e Estagiarios/
├── 📄 estag_pcd.html                    # Aplicação principal
├── 📄 README.md                         # Este arquivo
├── 📊 Empresas por regime federal.xlsx  # Dados de exemplo
├── 📊 funcionários ativos.xlsx          # Dados de exemplo
└── 📊 Funcionarios vs regime - Página1.csv # Dados de exemplo
```

## 🛠️ Tecnologias Utilizadas

- **HTML5 + CSS3**: Estrutura e estilização
- **JavaScript ES6+**: Lógica da aplicação
- **Tailwind CSS**: Framework de estilização responsiva
- **Papa Parse**: Biblioteca para processamento de arquivos CSV
- **Chart.js**: Geração de gráficos interativos
- **jsPDF**: Geração de relatórios em PDF
- **html2canvas**: Captura de elementos HTML para PDF

## 📊 Formato do CSV

O arquivo CSV deve conter as seguintes colunas:

| Coluna | Descrição | Exemplo |
|--------|-----------|---------|
| `Nome_Empresa` | Nome da empresa | "Empresa ABC Ltda" |
| `ativos` | Número de funcionários ativos | 150 |
| `Regime federal` | Regime tributário | "Lucro Real" |

### Exemplo de CSV

```csv
Nome_Empresa,ativos,Regime federal
Empresa ABC Ltda,150,Lucro Real
Empresa XYZ S.A.,25,Simples Nacional
Empresa 123 ME,8,Lucro Presumido
```

## 🎨 Interface

A aplicação apresenta uma interface moderna e intuitiva com:

- **Cabeçalho**: Título e botão de download do PDF
- **Área de Upload**: Seleção de arquivo CSV e botão de geração
- **Seção de Resultados**: Gráficos e tabelas organizados por categoria
- **Mensagens de Erro**: Feedback claro sobre problemas no processamento

## 📱 Responsividade

A interface se adapta automaticamente a diferentes tamanhos de tela:

- **Desktop**: Layout com duas colunas (gráfico + tabela)
- **Tablet/Mobile**: Layout em coluna única com componentes empilhados

## 🐛 Tratamento de Erros

A aplicação inclui tratamento robusto de erros para:

- Arquivos CSV malformados
- Colunas ausentes ou com nomes incorretos
- Dados numéricos inválidos
- Problemas na geração de PDF

## 📝 Licença

Este projeto é de uso interno e proprietário.

## 👥 Suporte

Para dúvidas ou suporte técnico, entre em contato com a equipe de desenvolvimento.

---

**Última atualização**: Julho 2025
