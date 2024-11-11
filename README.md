# Sistema Hospitalar 🏥

Este projeto visa desenvolver um **sistema hospitalar** com foco em **gestão de dados**, utilizando **MongoDB** como banco de dados. A aplicação está em desenvolvimento e o diagrama do banco de dados está em construção.

## 📊 Funcionalidades
- Gestão de **pacientes** e **atendimentos**.
- Cadastro e controle de **médicos** e **especialidades**.
- Acompanhamento de **quartos** e **internações**.
- Relatórios e **histórico de tratamentos**.

## 🚧 Em Construção
Este repositório está em constante evolução! A estrutura do banco de dados e o sistema hospitalar ainda estão sendo desenvolvidos.

---

## 🔍 Parte 1 - Mãos à Obra (Em Construção)

**Descrição:**
O hospital necessita de um sistema para sua área clínica que ajude a controlar consultas realizadas. Os médicos podem ser generalistas, especialistas ou residentes e têm seus dados pessoais cadastrados em planilhas digitais. Cada médico pode ter uma ou mais especialidades, que podem ser pediatria, clínica geral, gastroenterologia e dermatologia. Alguns registros antigos ainda estão em formulário de papel, mas será necessário incluir esses dados no novo sistema.

Os pacientes também precisam de cadastro, contendo dados pessoais (nome, data de nascimento, endereço, telefone e e-mail), documentos (CPF e RG) e convênio. Para cada convênio, são registrados nome, CNPJ e tempo de carência.

As consultas também têm sido registradas em planilhas, com data e hora de realização, médico responsável, paciente, valor da consulta ou nome do convênio, com o número da carteira. Também é necessário indicar na consulta qual a especialidade buscada pelo paciente.

Deseja-se ainda informatizar a receita do médico, de maneira que, no encerramento da consulta, ele possa registrar os medicamentos receitados, a quantidade e as instruções de uso. A partir disso, espera-se que o sistema imprima um relatório da receita ao paciente ou permita sua visualização via internet.

🔨 **Em construção**: O diagrama está sendo elaborado.

---

## 🔍 Parte 2 - Internações (Em Construção)

**Descrição:**
No hospital, as internações têm sido registradas por meio de formulários eletrônicos que gravam os dados em arquivos. Para cada internação, são anotadas a data de entrada, a data prevista de alta e a data efetiva de alta, além da descrição textual dos procedimentos a serem realizados. As internações precisam ser vinculadas a quartos, com a numeração e o tipo. Cada tipo de quarto tem sua descrição e o seu valor diário (a princípio, o hospital trabalha com apartamentos, quartos duplos e enfermaria).

Também é necessário controlar quais profissionais de enfermaria estarão responsáveis por acompanhar o paciente durante sua internação. Para cada enfermeiro(a), é necessário nome, CPF e registro no conselho de enfermagem (COREN). A internação, obviamente, é vinculada a um paciente – que pode se internar mais de uma vez no hospital – e a um único médico responsável.

### Funcionalidades da Parte 2:
- Cadastro e controle de **internações**, incluindo data de entrada, data de alta e procedimentos realizados.
- Vinculação das **internações** a **quartos** e **médicos responsáveis**.
- Cadastro de **enfermeiros** responsáveis por acompanhar as internações.
- Relacionamento entre **internações** e **pacientes**.

🔨 **Em construção**: O diagrama da Parte 2 está sendo desenvolvido.

---
## Parte 3 - Jogando nas regras que você criou 🚀

Crie scripts de povoamento dos documentos desenvolvidas na atividade anterior.

### Atividades:

### 1) **Inclua ao menos dez médicos de diferentes especialidades.**

```javascript
db.medicos.insertMany([
  { 
    nome: "Dr. Rafael Almeida", 
    tipo: "Especialista", 
    especialidades: ["Pediatria"], 
    contato: { telefone: "123456789", email: "rafael.almeida@email.com" }, 
    documentos: { CPF: "123.456.789-10", RG: "MG123456" } 
  },
  { 
    nome: "Dra. Isabel Cardoso", 
    tipo: "Generalista", 
    especialidades: ["Clínica Geral"], 
    contato: { telefone: "987654321", email: "isabel.cardoso@email.com" }, 
    documentos: { CPF: "987.654.321-00", RG: "SP987654" } 
  },
  { 
    nome: "Dr. Fábio Costa", 
    tipo: "Especialista", 
    especialidades: ["Gastroenterologia"], 
    contato: { telefone: "112233445", email: "fabio.costa@email.com" }, 
    documentos: { CPF: "456.123.789-21", RG: "RJ456123" } 
  },
  { 
    nome: "Dra. Paula Tavares", 
    tipo: "Residente", 
    especialidades: ["Dermatologia"], 
    contato: { telefone: "332211665", email: "paula.tavares@email.com" }, 
    documentos: { CPF: "564.789.123-00", RG: "PR564789" } 
  },
  { 
    nome: "Dr. Hugo Martins", 
    tipo: "Especialista", 
    especialidades: ["Cardiologia"], 
    contato: { telefone: "445566778", email: "hugo.martins@email.com" }, 
    documentos: { CPF: "124.567.890-12", RG: "BA124567" } 
  },
  { 
    nome: "Dra. Camila Ferreira", 
    tipo: "Generalista", 
    especialidades: ["Clínica Geral"], 
    contato: { telefone: "556677889", email: "camila.ferreira@email.com" }, 
    documentos: { CPF: "789.456.123-45", RG: "CE789456" } 
  },
  { 
    nome: "Dr. Alexandre Lima", 
    tipo: "Especialista", 
    especialidades: ["Neurologia"], 
    contato: { telefone: "223344556", email: "alexandre.lima@email.com" }, 
    documentos: { CPF: "321.654.987-32", RG: "RS321654" } 
  },
  { 
    nome: "Dra. Fernanda Rocha", 
    tipo: "Especialista", 
    especialidades: ["Ortopedia"], 
    contato: { telefone: "667788990", email: "fernanda.rocha@email.com" }, 
    documentos: { CPF: "765.432.109-98", RG: "GO765432" } 
  },
  { 
    nome: "Dr. Ricardo Souza", 
    tipo: "Residente", 
    especialidades: ["Gastroenterologia"], 
    contato: { telefone: "334455667", email: "ricardo.souza@email.com" }, 
    documentos: { CPF: "910.111.213-31", RG: "SC910111" } 
  },
  { 
    nome: "Dra. Mariana Santos", 
    tipo: "Especialista", 
    especialidades: ["Cardiologia"], 
    contato: { telefone: "998877665", email: "mariana.santos@email.com" }, 
    documentos: { CPF: "215.314.151-41", RG: "DF215314" } 
  }]);

---
---


### 2) **Inclua ao menos sete especialidades.**

Considere que entre as especialidades há **pediatria**, **clínica geral**, **gastroenterologia** e **dermatologia**. Aqui está o script para povoar as especialidades no banco de dados:

```javascript
db.especialidades.insertMany([
  { nome: "Pediatria", descricao: "Especialidade médica voltada para o atendimento de crianças e adolescentes." },
  { nome: "Clínica Geral", descricao: "Especialidade médica que lida com diagnósticos e tratamentos gerais." },
  { nome: "Gastroenterologia", descricao: "Especialidade médica focada no sistema digestivo e doenças relacionadas." },
  { nome: "Dermatologia", descricao: "Especialidade médica dedicada ao estudo da pele e suas doenças." },
  { nome: "Cardiologia", descricao: "Especialidade médica voltada ao estudo e tratamento das doenças do coração." },
  { nome: "Neurologia", descricao: "Especialidade médica que lida com o sistema nervoso e suas patologias." },
  { nome: "Ortopedia", descricao: "Especialidade médica focada no diagnóstico e tratamento de doenças ósseas e articulares." }
]);

