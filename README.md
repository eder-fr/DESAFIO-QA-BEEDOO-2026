# Desafio técnico QA – Beedoo (2026)

## 1. Introdução

Este repositório apresenta a execução do Desafio técnico de qualidade de software da Beedoo, com o objetivo de avaliar a capacidade de análise de sistemas, criação de cenários de teste, execução de testes e identificação de defeitos em uma aplicação web.

A atividade consiste em analisar e testar o módulo de **cadastro e listagem de cursos** disponível na aplicação proposta.

Aplicação analisada:  
https://creative-sherbet-a51eac.netlify.app/

---

## 2. Objetivo da aplicação

Com base na análise realizada, a aplicação tem como objetivo permitir o **gerenciamento de cursos**, possibilitando ao usuário:

- Cadastrar novos cursos  
- Visualizar cursos cadastrados  
- Excluir cursos existentes  

O sistema funciona como um módulo simples de administração de cursos, onde cada curso possui informações como:

- Nome
- Descrição
- Instrutor
- Período de realização
- Quantidade de vagas
- Formato (presencial ou online)

---

## 3. Estrutura da aplicação

Durante a exploração inicial da aplicação foram identificadas as seguintes páginas e elementos.

## Página inicial / listagem de cursos

A aplicação não possui uma página inicial dedicada. Ao acessar o sistema pela primeira vez, o usuário é direcionado automaticamente para a página **LISTAR CURSOS**.

## Cabeçalho da aplicação

O cabeçalho da aplicação possui os seguintes elementos:

- Texto **"Beedoo QA Chalenge"** posicionado no canto superior esquerdo  
  *(observação: o correto seria "Challenge", com duas letras "l")*

- Menu de navegação no canto superior direito com as opções:

- **LISTAR CURSOS**
- **CADASTRAR CURSOS**

---

## Página LISTAR CURSOS

Esta página apresenta a listagem dos cursos cadastrados no sistema.

Quando não há cursos cadastrados, é exibido apenas o título:

**Lista de cursos**

Quando existem cursos cadastrados, eles são exibidos em formato de **card**, contendo as seguintes informações:

- Tipo do curso (Presencial ou Online)
- Nome do curso
- Descrição do curso
- Data de início
- Data de término
- Número de vagas

Cada card também possui um botão:

**EXCLUIR CURSO**

Este botão permite remover o curso da lista.

---

## Página CADASTRAR CURSOS

Esta página permite o cadastro de novos cursos.

O formulário de cadastro possui os seguintes campos:

- Nome do curso
- Descrição do curso
- Instrutor
- URL da imagem da capa
- Data de início
- Data de fim
- Número de vagas
- Tipo de curso (Presencial ou Online)

Os campos de data podem ser preenchidos de duas formas:

- Inserção manual
- Seleção através de um calendário exibido ao clicar no ícone de calendário

Ao final do formulário existe o botão:

**CADASTRAR CURSO**

---

## 4. Fluxos principais da aplicação

Durante a análise da aplicação foram identificados os seguintes fluxos principais.

---

## Fluxo 1 – Navegação inicial

1. O usuário acessa a aplicação.
2. O sistema direciona automaticamente para a página **LISTAR CURSOS**.
3. Caso não existam cursos cadastrados, apenas o título **Lista de cursos** é exibido.

---

## Fluxo 2 – Cadastro de curso

1. O usuário clica na opção **CADASTRAR CURSOS** no menu superior.
2. O sistema direciona para a página de cadastro de cursos.
3. O usuário preenche os campos do formulário.
4. O usuário clica no botão **CADASTRAR CURSO**.
5. O sistema redireciona o usuário para a página **LISTAR CURSOS**.
6. Uma notificação é exibida na parte superior central da página com a mensagem:

**Curso cadastrado com sucesso!**

Essa notificação permanece visível por alguns segundos.

---

## Fluxo 3 – Listagem de cursos

1. O usuário acessa a página **LISTAR CURSOS**.
2. O sistema exibe todos os cursos cadastrados em formato de **card**.
3. Cada card apresenta as informações do curso cadastrado.

---

## Fluxo 4 – Exclusão de curso

1. O usuário acessa a página **LISTAR CURSOS**.
2. O usuário localiza o curso desejado.
3. O usuário clica no botão **EXCLUIR CURSO**.
4. O sistema remove o curso da lista.
5. Uma notificação é exibida com a mensagem:

**Curso excluído com sucesso!**

A notificação permanece visível por alguns segundos na parte superior central da página.

---

## 5. Estratégia de testes

A estratégia adotada neste desafio envolveu as seguintes etapas:

- Análise exploratória da aplicação
- Identificação dos fluxos principais do sistema
- Elaboração de cenários de teste positivos e negativos
- Execução manual dos testes
- Registro das evidências
- Documentação dos defeitos encontrados

Os testes foram focados principalmente nos seguintes pontos:

- Validação de campos obrigatórios
- Validação de formatos e limites de dados
- Regras de negócio relacionadas aos tipos de curso
- Persistência de dados
- Funcionamento da exclusão de cursos
- Comportamentos inesperados do sistema

---

## 6. Pontos críticos para teste

Durante a análise da aplicação foram identificados alguns pontos considerados críticos para testes.

## Validação dos campos do formulário

Verificar se o sistema impede o cadastro de cursos com informações inválidas ou incompletas.

---

## Validação das datas

Garantir que:

- A data de término não seja anterior à data de início
- O sistema trate corretamente datas inseridas manualmente

---

## Número de vagas

Validar se o sistema aceita apenas valores numéricos válidos e se existe algum limite mínimo ou máximo de vagas.

---

## Persistência dos dados

Garantir que os cursos cadastrados sejam exibidos corretamente na página de listagem.

---

## Exclusão de cursos

Verificar se a exclusão remove corretamente o curso da lista e se a interface é atualizada após a ação.

---

## Comportamentos inesperados

Testar entradas inválidas, campos vazios, valores extremos e formatos incorretos para identificar possíveis falhas no sistema.

---

## 7. Casos de teste

Os cenários e casos de teste elaborados para este desafio foram documentados em uma planilha do Google Sheets.

Link da planilha de casos de teste:

https://docs.google.com/spreadsheets/d/1jUtukUffTZ0He2Suh5dkm7_8gvskM9QpjWwcgEiGEQo/edit?gid=0#gid=0

---

## 8. Evidências da execução dos testes

As evidências da execução dos testes foram registradas por meio de **capturas de tela realizadas durante a execução dos cenários de teste**.

Para facilitar a navegação e organização, as evidências foram separadas por funcionalidade testada:

- Cadastro de cursos
- Listagem de cursos
- Bugs identificados

Link para acesso às evidências:

https://drive.google.com/drive/folders/1UZQKavrdLfshjoPN2S2O53WbYROzRZq2

---

## 9. Relatório de bugs

Os bugs identificados durante a execução dos testes foram documentados contendo:

- Título do bug
- Passos para reprodução
- Resultado atual
- Resultado esperado
- Severidade ou impacto

Link do relatório de bugs:

https://docs.google.com/spreadsheets/d/1-0wdhaeobJ2hxqAbAluVOe8VcwNetXshcHdMfYilxUs/edit?gid=0#gid=0

---

## 10. Resumo da execução dos testes

| Métrica | Resultado |
| Total de casos de teste executados | 22 |
| Testes aprovados | 5 |
| Testes reprovados | 17 |
| Bugs identificados | 7 |

---

## 11. Possíveis melhorias para a aplicação

Durante a execução dos testes foram identificadas algumas oportunidades de melhoria que podem aumentar a confiabilidade do sistema e melhorar a experiência do usuário.

Principais melhorias sugeridas:

- Implementação de validações de **campos obrigatórios no formulário**
- Validação de **formatos de dados**, como datas, URLs e valores numéricos
- Definição de **limites para o campo número de vagas**
- Implementação de **validação de campos condicionais**, como endereço para cursos presenciais e link de inscrição para cursos online
- Correção do comportamento da funcionalidade **Excluir curso**, garantindo que o item seja removido da lista após a ação
- Padronização de mensagens de erro e validação exibidas ao usuário
- Implementação da funcionalidade **Editar curso**, permitindo que o usuário faça a edição de informações de um curso cadastrado
- Correção ortográfica do texto **"Beedoo QA Chalenge"** para **"Beedoo QA Challenge"**

---

## 12. Considerações finais

Este desafio foi realizado com foco na análise da aplicação, estruturação de cenários de teste, execução dos testes e registro de defeitos, seguindo boas práticas utilizadas em processos de **Qualidade de Software**.

A atividade permitiu exercitar habilidades importantes para atuação em QA, como:

- análise de requisitos
- identificação de cenários de teste
- execução de testes manuais
- documentação de evidências
- registro estruturado de defeitos
