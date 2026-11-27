# Diagnóstico do projeto herdado — MercadoÁgil

## Sobre o projeto

O projeto que recebemos da Squad 2 é um sistema de gerenciamento de pedidos de um marketplace, desenvolvido com JavaScript, Node.js e Zod. O código está separado em models, services, schemas, menus, configurações e testes. Já existe uma API HTTP feita com o próprio Node.js, mas os dados ainda são armazenados em memória.

## O que já funciona

Conseguimos instalar as dependências e rodar o projeto normalmente. Executamos os 28 testes existentes e todos passaram, inclusive o teste do pedido de R$ 193,00, que apresentou os valores esperados.

Os cadastros, cálculos, aplicação de cupons, confirmação e cancelamento de pedidos também já possuem uma boa base que pode ser aproveitada no M2.

## Problemas encontrados

Além dos testes que já existiam, fizemos alguns testes pela API e encontramos os seguintes problemas:

- **Estoque:** depois de atualizar um produto com 10 unidades e realizar a compra de uma unidade, a consulta continua mostrando 10, quando deveria mostrar 9.
- **Exclusão de vendedor:** conseguimos excluir um vendedor, mas os produtos vinculados a ele continuaram cadastrados.
- **CPF duplicado:** conseguimos cadastrar dois clientes com o mesmo CPF, um com pontuação e outro sem.
- **Validação de CPF:** o sistema aceitou o cadastro de um cliente com uma letra no CPF.
- **README:** a documentação informa que o `npm start` abre o menu no terminal, mas o comando inicia o servidor HTTP.

## O que pretendemos fazer

- **Manter:** as regras de negócio, os cálculos e os testes que já funcionam, evitando reescrever código sem necessidade.
- **Corrigir:** os problemas encontrados durante os testes e atualizar a documentação.
- **Reestruturar:** adaptar a API para Express e substituir o armazenamento em memória pelo PostgreSQL com Sequelize, seguindo os requisitos do M2.

A ideia é aproveitar o máximo possível do código recebido e fazer as mudanças aos poucos, testando para não quebrar o que já funciona. Essas propostas ainda serão alinhadas com toda a squad.