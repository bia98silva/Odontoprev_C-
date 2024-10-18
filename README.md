Projeto de Newsletter Odontológica da OdontoPrev

![Diagrama](https://github.com/bia98silva/Odontoprev_C-/blob/main/diagrama.png)

Visão Geral do Projeto

Este projeto é parte de uma iniciativa da OdontoPrev para melhorar a comunicação com profissionais da área odontológica e clientes. O sistema consiste em uma aplicação web desenvolvida em .NET MVC para gerenciar e enviar newsletters com informações relevantes sobre procedimentos odontológicos, atualizações da empresa e dicas de saúde bucal.

O objetivo principal é manter os assinantes informados sobre as últimas novidades no campo da odontologia, promover boas práticas de higiene bucal e divulgar serviços e promoções da OdontoPrev.

Arquitetura do Projeto

Este projeto segue os princípios da Clean Architecture para manter o código desacoplado e facilitar a manutenção e escalabilidade. A estrutura do projeto é dividida nas seguintes camadas:

Camadas da Aplicação

Apresentação

Controllers: RedatorController, NewsletterController
Views (não implementadas neste projeto MVC API)
Aplicação

Services: RedatorService, NewsletterService
ViewModels: RedatorViewModel, NewsletterViewModel, LoginViewModel
Domínio

Models: Redator, Newsletter
Infraestrutura

Data: NewsletterDbContext
Repositories: RedatorRepository, NewsletterRepository
Definição do Projeto
Objetivo do Projeto
O objetivo deste projeto é criar uma plataforma para gerenciar e enviar newsletters odontológicas. Esta plataforma servirá como um canal de comunicação eficiente entre a OdontoPrev e seus assinantes, incluindo profissionais de odontologia e clientes.

Escopo

Este projeto abrange o desenvolvimento de uma aplicação web utilizando .NET MVC para gerenciar assinantes, criar e enviar newsletters. O escopo inclui:

Sistema de autenticação para redatores
Interface de administração para criar, editar e enviar newsletters
Gerenciamento de assinantes
API para possível integração futura com outros sistemas
Requisitos Funcionais
Autenticação de redatores

Login seguro para redatores
Gerenciamento de perfis de redator
Gerenciamento de Newsletters

Criação de novas newsletters
Edição de newsletters existentes
Envio de newsletters para assinantes
Visualização do histórico de newsletters enviadas
Gerenciamento de Assinantes

Adição e remoção de assinantes
Segmentação de assinantes por categorias (ex: dentistas, clientes)
API RESTful

Endpoints para gerenciar newsletters e assinantes
Requisitos Não Funcionais
Segurança

Utilização de HTTPS para todas as comunicações
Armazenamento seguro de senhas (hashing)
Proteção contra ataques comuns (SQL Injection, XSS, CSRF)
Desempenho

Capacidade de enviar newsletters para pelo menos 10.000 assinantes em menos de 1 hora
Tempo de resposta da API inferior a 500ms para 95% das requisições
Usabilidade

Interface responsiva para acesso via desktop e dispositivos móveis
Design intuitivo para facilitar a criação e envio de newsletters
Manutenibilidade

Código bem documentado
Utilização de padrões de projeto para facilitar futuras expansões
Compatibilidade

Suporte aos principais navegadores (Chrome, Firefox, Safari, Edge)
Newsletters compatíveis com os principais clientes de e-mail
Escalabilidade

Arquitetura que permita fácil escalabilidade horizontal para suportar aumento no número de assinantes
Detalhes das Classes Principais
Redator
Propriedades:
Id
Nome
Email
Username
PasswordHash
Especializacao
DataCadastro
Ativo
Newsletter
Propriedades:
Id
Titulo
Conteudo
DataCriacao
DataEnvio
RedatorId
Enviada
RedatorController
Métodos:
POST: Login
GET: GetAllRedatores
POST: CreateRedator
PUT: UpdateRedator
DELETE: DeleteRedator
NewsletterController
Métodos:
GET: GetNewsletters
GET: GetNewsletter
POST: CreateNewsletter
PUT: UpdateNewsletter
DELETE: DeleteNewsletter
POST: SendNewsletter
Fluxo de Funcionamento
Redator

Acessa a aplicação
Realiza login
Cria ou edita newsletters
Envia newsletters para assinantes
Sistema

Gerencia assinantes
Processa o envio de newsletters
Mantém histórico de newsletters enviadas
Assinante

Recebe newsletters por e-mail
Pode se inscrever ou cancelar a inscrição (através de um link na newsletter)
Tecnologias Utilizadas
.NET 8.0 ou superior
ASP.NET Core MVC
Entity Framework Core
Banco de dados Oracle
JWT para autenticação
Integrantes
Turma: 2TDSPS
Bia Silva 552600 Pedro henrique S araujo 553801
