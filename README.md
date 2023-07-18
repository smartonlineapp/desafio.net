![logo-smartonline](https://www.smartonline.app/logo.a3cd84b4d14610f7.png)
## Desafio para vaga desenvolvedor .NET

Por favor leiam este documento do começo ao fim, com muita atenção. O intuito deste teste é avaliar seus conhecimentos técnicos de programação.<br/>
O teste consiste em parsear este arquivo de texto [CNAB](https://github.com/smartonlineapp/desafio.net/blob/main/CNAB.txt) e salvar suas informações (_transações financeiras_) em uma base de dados a critério do candidato.<br/>
Este desafio deve ser feito por você em sua casa. Gaste o tempo que você quiser, porém normalmente você não deve precisar de mais do que algumas horas.

## Entrega do desafio

1. Primeiro, faça um fork deste projeto para sua conta no Github (_crie uma se você não possuir_).
2. Em seguida, implemente o projeto tal qual descrito abaixo, em seu clone local.
3. Por fim, envie via email o projeto ou o fork/link do projeto para o e-mail do RH.

## Descrição do projeto

Você recebeu um arquivo CNAB com os dados das movimentações finanaceira de várias lojas.<br/>
Precisamos criar uma maneira para que estes dados sejam importados para um banco de dados.

Sua tarefa é criar uma interface web que aceite upload do [arquivo CNAB](https://github.com/smartonlineapp/desafio.net/blob/main/CNAB.txt), normalize os dados e armazene-os em um banco de dados relacional ou NOSQL (_opcional - pontos extras se utilizar_) e exiba essas informações em tela.

**Sua aplicação Web Deve:**

1. Ter uma tela (_via um formulário_) para fazer o upload do arquivo (_pontos extras se não usar um popular CSS Framework_);
2. Interpretar ("_parsear_") o arquivo recebido, normalizar os dados, e salvar corretamente a informação em um banco de dados, **se atente as documentações** que estão logo abaixo;
3. Verificar se os dados de CPF estão válidos;
4. Exibir uma lista das operações importadas por lojas, e nesta lista deve conter um totalizador do saldo em conta;
5. Exibir uma lista das operações que deram errado;
6. Ser escrita obrigatoriamente em .NET em versões recentes, pode ser .NET Core, ASP.MVC, etc;
7. Ser simples de configurar e rodar. Ela deve utilizar apenas linguagens e bibliotecas livres ou gratuitas;
8. Git com commits atomicos e bem descritos;
9. PostgreSQL, MySQL, SQL Server ou MongoDb (_pode usar qualquer banco relacional ou NOSQL, lembrando que o NOSQL é opcional_);
10. Readme file descrevendo bem o projeto e seu setup;
11. Incluir informação descrevendo como consumir o endpoint da API.

**Sua aplicação Web não precisa:**

1. Lidar com autenticação ou autorização (_pontos extras se ela fizer, mais pontos extras se a autenticação for feita via OAuth_);
2. Não ser escrita usando algum framework específico (_mas não há nada errado em usá-los também, use o que achar melhor_);
3. Documentação da api. (_será um diferencial e pontos extras se fizer_);
4. Ter testes automatizados (_opcional - pontos extras se utilizar_);
5. Docker compose (_opcional - pontos extras se utilizar_).

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

## Avaliação

Seu projeto será avaliado de acordo com os seguintes critérios.

1. Sua aplicação preenche os requesitos básicos?
2. Você documentou a maneira de configurar o ambiente e rodar sua aplicação?
3. Você seguiu as instruções de envio do desafio?
4. Qualidade e cobertura dos testes unitários (_opcional_).

Adicionalmente, tentaremos verificar a sua familiarização com as bibliotecas padrões (_standard libs_), bem como sua experiência com programação orientada a objetos a partir da estrutura de seu projeto.

---

Boa sorte!
