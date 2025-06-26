# Guia para Geração de Diagramas Arquiteturais com LLM
Este guia orienta como gerar Diagramas de Classe e Diagramas de Componentes usando Claude.ai, com base em ADRs existentes da empresa BioInnovate Corp., utilizando a técnica Diagram as Code com Mermaid.js.



## 🧠 LLM Usado
- Modelo: Claude.ai
- Técnica: Diagramas baseados em decisões arquiteturais descritas em [ADRs](https://github.com/yanjustino/ai-prompting/tree/main/samples/adr)

## 🧾 Prompt Principal
```xml
<context>
Você irá atuar como arquiteto de software sênior para atender as demandas da BioInnovate Corp., uma empresa de biotecnologia em crescimento. Na tag <attachment>, estão os arquivos nos quais descrevem os ADR’s que representam as decisões arquiteturais registradas. Siga estritamente as instruções na tag <instructions> para gerar um {{DIAGRAMA DE CLASSE}} e um {{DIAGRAMA DE COMPONENTES}}.
</context>

<attachment>
{{ADR1.pdf}}
{{ADR2.pdf}}
</attachment>

<instruction>
1. Siga estritamente as <restrictions>
2. Analise o conteúdo de <attachment> focando no {{ADR2.pdf}}
3. Construa um {{DIAGRAMA DE CLASSE}}
4. Construa um {{DIAGRAMA DE COMPONENTES}}.
</instruction>

<restrictions>
1. Os Diagramas irão ser escritos usando a técnica de Diagram as Code
2. Utilize o formato Mermaid JS na geração do {{DIAGRAMA DE CLASSE}} e do {{DIAGRAMA DE COMPONENTES}}
3. Não escreva comentários no código dos diagramas.
4. Não escreva nada além dos códigos dos diagramas.
</restrictions>
```

## 💡 Notas sobre o Uso
- O LLM deve focar no conteúdo do ADR2 ao extrair as informações relevantes para os diagramas.
- Os diagramas devem ser expressos exclusivamente em Mermaid.js, sem comentários ou explicações extras.
- A técnica Diagram as Code facilita integração com documentação versionada, como o uso em ferramentas como MkDocs, Docusaurus, GitHub Pages, etc.

## ✅ Exemplos de Sintaxe Mermaid.js

```
Diagrama de Classe

classDiagram
    class User {
        +String name
        +String email
        +login()
    }
    class Session {
        +startTime: Date
        +endTime: Date
        +isActive(): boolean
    }
    User --> Session

Diagrama de Componentes

graph TD
    A[Frontend App] -->|REST API| B[Backend Service]
    B -->|Reads/Writes| C[(Database)]
    B --> D[Auth Service]
    D --> E[(Identity Provider)]
```


## 📎 Referências
- Mermaid.js Documentation
- Exemplo de Classe – Claude.ai
- Exemplo de Componentes – Claude.ai
- ThoughtWorks – Visualizar Arquitetura com Mermaid
