# Teste Técnico Quality Assurance Full Stack (Nivanderson Coutinho)

Este projeto apresenta a resolução dos testes técnicos apresentados.

### Blocos do Teste
- **Bloco 1 – Análise de Requisitos:** interpretação da história de usuário e definição de cenários de teste.  
- **Bloco 2 – Execução de Testes:** testes de usabilidade e validação das principais funcionalidades da plataforma.  
- **Bloco 3 – Report de Bugs:** documentação clara e objetiva das falhas encontradas.  
- **Bloco 4 – Proatividade em Processos:** proposta de criação e estruturação de um setor de QA.  
- **Bloco Bônus – Mini Desafio:** automação de um cenário crítico com pseudocódigo em Cypress.  

---

## 📂 Bloco 1: Análise de Requisitos

Esta seção contém todos os documentos e artefatos de apoio relacionados à fase de Análise de Requisitos do projeto.

| Tipo de Arquivo | Descrição | Link para Acesso |
| :--- | :--- | :--- |
| **PDF** | Documento consolidado e pronto para leitura, contendo toda a análise de requisitos. | **[Visualizar Requisitos em PDF](./bloco-1/BLOCO%201%20–%20ANÁLISE%20DE%20REQUISITOS.pdf)** |
| **Planilha (XLSX)** | Planilha demonstrativa com detalhes da rastreabilidade e priorização de requisitos. | **[Baixar Planilha Demonstrativa](./bloco-1/BLOCO%201%20–%20ANÁLISE%20DE%20REQUISITOS%20(Planilha%20demonstrativa).xlsx)** |

### 💡 Notas sobre Acesso aos Arquivos

* Os links para **arquivos PDF** devem abrir a visualização diretamente no seu navegador.
* Os links para **arquivos XLSX e PPTX** iniciarão o download do arquivo.

---

## 📂 Bloco 2 – EXECUÇÃO DE TESTES

Esta seção contém o material de apoio sobre o processo e a execução dos testes no projeto.

| Tipo de Arquivo | Descrição | Link para Acesso |
| :--- | :--- | :--- |
| **Documento (PDF)** | Guia e relatório consolidado sobre a execução dos testes. | **[Visualizar Relatório de Testes (PDF)](./bloco-2/BLOCO%202%20–%20EXECUÇÃO%20DE%20TESTES.pdf)** |
| **Apresentação (PPTX)** | Slides da apresentação com os principais pontos e resultados da execução dos testes. | **[Baixar Apresentação (PPTX)](./bloco-2/BLOCO%202%20–%20EXECUÇÃO%20DE%20TESTES.pptx)** |

### 💡 Notas sobre Acesso aos Arquivos

* Os links para **arquivos PDF** devem abrir a visualização diretamente no seu navegador.
* Os links para **arquivos XLSX e PPTX** iniciarão o download do arquivo.

---

### 📂 Bloco 3: Relatório de Bugs

Esta seção apresenta o documento consolidado do relatório final com os **bugs encontrados**, sua classificação e o status de resolução.

| Tipo de Arquivo | Descrição | Link para Acesso |
| :--- | :--- | :--- |
| **Relatório (PDF)** | Documento final com o detalhamento completo de todos os bugs reportados. | **[Visualizar Relatório de Bugs (PDF)](./bloco-3/Bloco%203%20–%20Report%20de%20Bugs.pdf)** |

---

### 💡 Notas sobre Acesso aos Arquivos

* Os links para **arquivos PDF** devem abrir a visualização diretamente no seu navegador.
* Os links para **arquivos XLSX e PPTX** iniciarão o download do arquivo.

---

## 📂 Bloco 4 – Proatividade em processos

Esta seção contém o documento chave sobre a implementação de **práticas proativas** e melhoria contínua nos processos de Quality Assurance.

| Tipo de Arquivo | Descrição | Link para Acesso |
| :--- | :--- | :--- |
| **Documento (PDF)** | Guia e diretrizes sobre a aplicação de proatividade na gestão e execução dos processos. | **[Visualizar Proatividade em Processos (PDF)](./bloco-4/BLOCO%204%20–%20PROATIVIDADE%20EM%20PROCESSOS.pdf)** |

---

### 💡 Notas sobre Acesso aos Arquivos

* Os links para **arquivos PDF** devem abrir a visualização diretamente no seu navegador.
* Os links para **arquivos XLSX e PPTX** iniciarão o download do arquivo.


---

## 📂 BLOCO BÔNUS – MINI DESAFIO
### Objetivo
O objetivo deste cenário é garantir que o sistema impeça adicionar produtos sem estoque ao carrinho. Este tipo de teste é crítico porque valida uma regra de negócio essencial: impedir pedidos inválidos que poderiam gerar inconsistências e prejuízos. A automação permite que esse teste seja repetido rapidamente e de forma confiável, garantindo regressão segura a cada release.

Esta seção contém um material extra em formato de mini desafio para aprimoramento de habilidades em Quality Assurance.

| Tipo de Arquivo | Descrição | Link para Acesso |
| :--- | :--- | :--- |
| **Documento (PDF)** | Proposta de um mini desafio prático para exercitar conhecimentos de QA. | **[Visualizar Mini Desafio (PDF)](./bloco-bonus/Bloco%20bônus%20-%20Mini%20desafio.pdf)** |

### Lógica do Teste

1.	Acessar a página principal do sistema.
2.	Pesquisar o produto específico (“Cadeira Y”) que possui estoque zerado.
3.	Validar a informação de estoque exibida na interface (“Estoque: 0”).
4.	Tentar adicionar o produto ao carrinho.
5.	Verificar se o sistema exibe a mensagem correta de erro (“Produto indisponível”), garantindo que a regra de negócio foi aplicada.


### Estrutura do Pseudo-código em Cypress (javascript)

``` describe('Adicionar produto ao carrinho', () => {
  it('Deve impedir adicionar produto sem estoque', () => {
    // 1. Visita a página inicial
    cy.visit('/home')
    // 2. Pesquisa pelo produto específico
    cy.get('#search').type('Cadeira Y')
    cy.get('#btnSearch').click()
    // 3. Verifica se o produto está com estoque 0
    cy.contains('Estoque: 0')
    // 4. Tenta adicionar ao carrinho
    cy.get('#addToCart').click()
    // 5. Valida que o sistema exibe mensagem de erro
    cy.contains('Produto indisponível')
  })
})
```
### Explicação de cada comando
 - describe: Agrupa testes relacionados a um fluxo funcional. Aqui define o escopo “Adicionar produto ao carrinho”.
 - it: Define um caso de teste individual, descrevendo o comportamento esperado.
 - cy.visit(): Navega para a URL inicial da aplicação (setup do teste).

---


## 💾 Relatório Completo - (Todos os blocos em arquivo único)

Este repositório contém o relatório completo referente ao **Teste Técnico de Quality Assurance Full Stack**, detalhando todas as etapas, resultados e análises.

Caso você queira uma **versão completa e formatada do relatório**, que inclui o **relatório completo de todos os blocos**, baixe o arquivo PDF anexo.

### 🔗 Link para Download

Para ter o documento completo em mãos, clique no link abaixo:

[**⬇️ Download: Teste Técnico – Quality Assurance Full Stack.pdf**](Teste%20T%C3%A9cnico%20%E2%80%93%20Quality%20Assurance%20Full%20Stack.pdf)

