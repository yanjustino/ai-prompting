# Guia para Geração de ADR com LLM
Este documento fornece instruções para utilizar um Large Language Model (LLM) — especificamente o Google Gemini — com técnicas de prompt engineering baseadas na metodologia da Anthropic, para gerar Architecture Decision Records (ADR) de maneira estruturada e eficaz.

## Objetivo
Automatizar a geração de ADRs para decisões arquiteturais relevantes na empresa BioInnovate Corp., com base em problemas reais descritos em documentos técnicos, utilizando tecnologias modernas de computação em nuvem.


## 🧠 LLM Usado  
- Modelo: Google Gemini
- Técnica:
  - [Prompt engineering baseado em Anthropic Claude Prompting Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
  - [One Shoot Prompting](https://www.ibm.com/think/topics/one-shot-prompting)


## 🧾 Prompt Principal
```xml
<context>
Você irá atuar como arquiteto de software sênior para atender as demandas da BioInnovate Corp., uma empresa de
biotecnologia em crescimento. Na tag <attachment>, está o arquivo no qual descreve os {{SISTEMAS}} utilizados e
os {{PROBLEMAS}} os quais a empresa passa ao utilizar esses {{SISTEMAS}}. Siga estritamente as instruções na tag
<instructions> para gerar um Arquitetura Decision Record ({{ADR}}), que é um documento que descreve uma decisão
arquitetural significativa tomada em um projeto de software, junto com o raciocínio por trás dela e o impacto
que ela tem.
</context>

<attachment>
{{BioInnovate Corp.pdf}}
</attachment>

<instruction>
1. Analise o conteúdo de <attachment> focando nos {{SISTEMAS}} e nos {{PROBLEMAS}}
2. Sugira uma solução para os {{PROBLEMAS}} listados 
3. Ao sugerir soluções para os {{PROBLEMAS}} siga as <restrictions> 
4. Apresente a solução como um {{ADR}} (Architecture Decision Record).
5. O {{ADR}} deve seguir o <template>
</instruction>

<restrictions>
1. A solução deve ser baseada em Cloud Computer.
2. Procure sugerir o uso de tecnologias modernas.
3. O resultado deve ser um {{ADR}} conforme o <template>.
4. Não escreva nada além do {{ADR}}.
</restrictions>

<template>
# ADR X: [Título da Decisão]

## Status
[Proposto | Aceito | Rejeitado | Substituído por ADR-Y | Obsoleto]

## Contexto
Descreva claramente o problema ou a motivação que levou à necessidade desta decisão de arquitetura.
Inclua:
- Desafios técnicos ou de negócio
- Restrições identificadas
- Alternativas consideradas inicialmente

## Decisão
Explique qual decisão foi tomada. Seja conciso e objetivo. Inclua:
- Qual caminho foi escolhido
- Justificativas
- Implicações imediatas

## Consequências
Liste as consequências da decisão, tanto positivas quanto negativas.
Inclua:
- Impactos técnicos
- Mudanças em processos
- Possíveis débitos técnicos
- Requisitos futuros

## Alternativas Consideradas
Liste as outras opções avaliadas e por que foram descartadas.

## Referências
Inclua links, artigos, documentos ou outras ADRs relevantes que embasaram a decisão.
</template>
```


## 🔄 Prompt Derivado (para comparativo AWS x Azure)

Após gerar o primeiro ADR com o prompt principal, um prompt adicional pode ser utilizado para expandir ou comparar decisões:

```
Crie um novo ADR comparativo com tecnologias AWS e Azure
```

Esse prompt deve ser executado após a geração do ADR1, aproveitando o contexto anterior e solicitando uma comparação baseada nos mesmos problemas, mas contrastando as soluções em AWS e Azure.


## ✅ Boas Práticas
- Utilize documentos reais como entrada (ex.: BioInnovate Corp.pdf).
- Garanta que o modelo está “instruído” corretamente com o contexto e as instruções estruturadas.
-	Sempre valide tecnicamente as recomendações antes de aplicar no ambiente de produção.
- Documente os ADRs em repositório versionado (como Git), mantendo rastreabilidade das decisões.


## 📎 Referências
-	Anthropic Prompting Overview
-	Architecture Decision Record – Michael Nygard
-	ThoughtWorks – ADR Guide
