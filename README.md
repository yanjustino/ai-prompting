# 🧠 IA para Devs - Geração de artefatos de Arquitetura

## 🏛️ Estudo de caso - BioInnovate Corp.

A BioInnovate Corp., **uma empresa de biotecnologia** em crescimento, especializada no desenvolvimento de tratamentos para doenças crônicas!
a empresa utiliza sistemas como:
- **Sistemas de Gestão de Informações de Laboratório (LIMS)** para rastrear experimentos e amostras.
- **Sistemas de gerenciamento de ensaios clínicos** para monitorar dados de pacientes e progresso de estudos.
- **Bancos de dados genômicos** para armazenar e analisar dados genéticos.
- **Sistemas financeiros e de gerenciamento de projetos** para acompanhar orçamentos e marcos.
- **Plataformas de colaboração** para compartilhar descobertas com parceiros.


> [!CAUTION] 
> A BioInnovate Corp. **enfrenta desafios significativos na integração de dados**. Esses sistemas operam de forma isolada, criando silos de dados que dificultam o acesso a informações abrangentes.
> Os principais problemas incluem: **Silos de Dados, Formatos Inconsistentes, Qualidade Deficiente, Escalabilidade, Falta de Insights em Tempo Real, Conformidade**.

## 🎯 Objetivo

Fornecer exemplos reais e funcionais de como utilizar LLMs para:
- Gerar documentação técnica estruturada
- Criar diagramas arquiteturais
- Automatizar processos de decisão arquitetural
- Demonstrar boas práticas de prompt engineering

## 📚 Samples Disponíveis

### 📋 [ADR (Architecture Decision Records)](samples/adr/)

**Objetivo**: Demonstrar como gerar ADRs estruturados usando LLMs baseado em problemas reais de uma empresa.

**Conteúdo**:
- Guia completo de prompt engineering para ADRs
- Exemplo prático com a empresa BioInnovate Corp
- Templates estruturados para decisões arquiteturais
- Técnicas baseadas na metodologia Anthropic Claude

**Arquivos**:
- `README.md` - Guia detalhado de uso
- `BioInnovate Corp.pdf` - Documento de contexto da empresa
- `ADR1.pdf` - Exemplo de ADR gerado
- `ADR2.pdf` - Exemplo de ADR comparativo (AWS vs Azure)

**LLM Utilizado**: Google Gemini

### 🏗️ [Diagramas Arquiteturais](samples/diagrams/)

**Objetivo**: Mostrar como gerar diagramas de classe e componentes usando Diagram as Code com Mermaid.js.

**Conteúdo**:
- Geração de diagramas baseados em ADRs existentes
- Técnica Diagram as Code com Mermaid.js
- Prompts estruturados para diferentes tipos de diagramas
- Integração com documentação versionada

**Arquivos**:
- `README.md` - Guia de geração de diagramas
- `class_diagram.mermaid` - Exemplo de diagrama de classes
- `component_diagram.mermaid` - Exemplo de diagrama de componentes

**LLM Utilizado**: Claude.ai

## 🚀 Como Usar

1. **Escolha o sample** que melhor se adequa ao seu caso de uso
2. **Leia o README** específico do sample para entender o contexto
3. **Adapte os prompts** para seu cenário específico
4. **Execute com seu LLM preferido** seguindo as instruções

## 💡 Benefícios

- **Produtividade**: Automatize tarefas repetitivas de documentação
- **Consistência**: Mantenha padrões em documentação técnica
- **Rastreabilidade**: Documente decisões arquiteturais de forma estruturada
- **Visualização**: Gere diagramas automaticamente baseados em decisões

## 🔧 Tecnologias Demonstradas

- **Prompt Engineering**: Técnicas estruturadas da Anthropic
- **Diagram as Code**: Mermaid.js para diagramas versionáveis
- **Documentação Técnica**: ADRs e diagramas arquiteturais
- **Cloud Computing**: Exemplos com AWS e Azure

## 📖 Referências

- [Anthropic Claude Prompting Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Architecture Decision Records](https://adr.github.io/)
- [Mermaid.js Documentation](https://mermaid.js.org/)

---

**Contribuições**: Sinta-se à vontade para contribuir com novos samples ou melhorias nos existentes!
