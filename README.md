# T3: Arquitetura de Microsserviços com Spring Boot
Este repositório contém a implementação prática da disciplina de Engenharia de Software II (Unimontes). O projeto consiste em um sistema distribuído composto por dois microsserviços autônomos que se comunicam de forma síncrona.

📋 Sobre o Projeto

O objetivo principal foi desenvolver uma aplicação empresarial simulada onde o gerenciamento de usuários (user-service) e o gerenciamento de departamentos (department-service) operam isoladamente, cada um com seu próprio banco de dados, respeitando o padrão Database per Service.

A integração entre os serviços é realizada via RestTemplate, permitindo que a API de usuários consulte e agregue informações da API de departamentos em tempo real para compor a resposta ao cliente.

⚙️ Arquitetura e Tecnologias

O sistema foi construído utilizando as seguintes tecnologias e padrões:


- Linguagem: Java 17.


- Framework: Spring Boot (Spring Data JPA, Spring Web).


- Banco de Dados: MySQL (Gerenciado via HeidiSQL).


- Comunicação: RestTemplate para requisições HTTP entre serviços.


- Padrão de Projeto: MVC (Model-View-Controller) e DTO (Data Transfer Object).


- Testes de API: Postman.

🚀 Implementações e Diferenciais

Além de seguir o tutorial base, este projeto inclui correções e melhorias arquiteturais importantes documentadas no relatório técnico:


- Uso de DTOs: Implementação de classes UserDto, DepartmentDto e ResponseDto para evitar a exposição direta das entidades JPA e garantir uma resposta unificada (Wrapper) ao cliente.


- Injeção de Dependência: Configuração manual correta dos Beans e anotações @Autowired e @Repository, corrigindo lacunas do material original.


- Configuração do RestTemplate: Criação de uma classe @Configuration dedicada para instanciar o RestTemplate, permitindo sua injeção nos serviços.

📄 Documentação

O relatório técnico completo (.pdf), detalhando o passo a passo do desenvolvimento, diagramas e análise comparativa, encontra-se disponível neste repositório.

Autor: Samuel Freitas de Oliveira 
Professor: Allysson Costa e Silva 
Semestre: 2025/01
