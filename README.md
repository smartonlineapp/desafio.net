![logo-smartonline](https://www.smartonline.app/logo.a3cd84b4d14610f7.png)

## Desafio para vaga desenvolvedor .NET

Por favor leia este documento do começo ao fim, com muita atenção. O intuito deste teste é avaliar seus conhecimentos técnicos de programação.

O teste consiste em parsear este arquivo de texto [CNAB](https://github.com/smartonlineapp/desafio.net/blob/main/CNAB.txt) e salvar suas informações (transações financeiras) em uma base de dados a seu critério.

## Entrega do desafio

1. Primeiro, faça um fork deste projeto para sua conta no Github (_crie uma se você não possuir_).
2. Em seguida, implemente o projeto tal qual descrito abaixo, em seu clone local.
3. Por fim, envie via e-mail o projeto ou o fork/link do projeto para o RH (andressa.monteiro@onlineapp.com.br).

## Descrição do projeto

Você recebeu um arquivo CNAB com os dados das movimentações finanaceiras de várias lojas.

É necessário que estes dados sejam importados para um banco de dados.

Sua tarefa é criar uma interface web que aceite upload do [arquivo CNAB](https://github.com/smartonlineapp/desafio.net/blob/main/CNAB.txt), normalize os dados e armazene-os em um banco de dados relacional ou NoSQL e exiba essas informações em tela.

## Documentação do CNAB

| Campo | Inicio | Fim | Tamanho | Descrição |
| ----- | ------ | --- | ------- | --------- |
| Tipo  | 1  | 1 | 1 | Tipo da transação |
| Data  | 2  | 9 | 8 | Data da ocorrência |
| Valor | 10 | 19 | 10 | Valor da movimentação (_o valor precisa ser divido por cem para normalizá-lo_) |
| CPF | 20 | 30 | 11 | CPF do beneficiário |
| Cartão | 31 | 42 | 12 | Cartão utilizado na transação |
| Dono da loja | 43 | 56 | 14 | Nome do representante da loja |
| Nome da loja | 57 | 74 | 18 | Nome da loja |

## Tipos das Transações

| Tipo | Descrição |
| ---- | --------- |
| 1 | Débito |
| 2 | Crédito |
| 3 | Pix |
| 4 | Financiamento |

**Sua aplicação Web Deve:**

1. Possuir uma tela para fazer o upload do arquivo;
2. Interpretar (_parsear_) o arquivo recebido, normalizar os dados, e salvar corretamente as informações em um banco de dados (_se atente as documentações que estão logo abaixo_);
3. Verificar se os dados de CPF estão válidos;
4. Exibir uma lista das operações importadas por lojas, e nesta lista deve conter um totalizador do saldo em conta;
5. Exibir uma lista das operações que deram errado;
6. Ser escrita obrigatoriamente em .NET em versões recentes, pode ser .NET Core, ASP.MVC, etc;
7. Ser simples de configurar e rodar. Ela deve utilizar apenas linguagens e bibliotecas livres ou gratuitas;
8. Git com commits atomicos e bem descritos;
9. PostgreSQL, MySQL, SQL Server ou MongoDb (pode usar qualquer banco relacional ou NoSQL, lembrando que o NoSQL é opcional);
10. Readme file descrevendo bem o projeto e seu setup;
11. Incluir informação descrevendo como consumir o endpoint da API.

**Você ganhará pontos adicionais se:**

1. Lidar com autenticação ou autorização (mais pontos extras se a autenticação for feita via OAuth);
2. Documentar sua API;
3. Desenvolver testes automatizados;
4. Utilizar Docker Compose.

## Avaliação

Avaliaremos a sua familiarização com as bibliotecas padrões (_standard libs_), bem como sua experiência com programação orientada a objetos a partir da estrutura de seu projeto.

---

Boa sorte!
