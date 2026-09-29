# Projeto CORETO — BI para Pequenos Negócios

## 1. Nome do projeto

**BI para Pequenos Negócios — Plataforma de Análise de Vendas e Apoio à Tomada de Decisão**

## 2. Nome da equipe

**A definir**

---

## 3. Integrantes e responsabilidades iniciais

| Nome | Matrícula | Responsabilidade inicial |
|---|---:|---|
| Pedro de Melo Albuquerque | 1608588 | Análise de dados, definição dos indicadores e desenvolvimento do dashboard |
| Valdeck Gomes do Carmo | 1306463 | Levantamento de requisitos e apoio na organização e tratamento dos dados |
| Pedro Victor Teixeira Bruno Lacerda | 1712849 | Desenvolvimento da interface e apoio na implementação da solução |
| Matheus José dos Santos Silva | 1597670 | Testes, documentação e apoio na validação das funcionalidades |

> As responsabilidades poderão ser ajustadas ao longo do desenvolvimento de acordo com as necessidades do projeto.

---

## 4. Descrição do problema

Micro, pequenas e médias empresas possuem grande importância para a economia, mas muitas vezes ainda tomam decisões relacionadas a vendas, estoque e operação com base principalmente na experiência do empreendedor, em registros manuais ou em informações pouco organizadas.

Essa realidade dificulta a identificação de quais produtos possuem maior saída, quais períodos apresentam maior volume de vendas e como o desempenho do negócio varia ao longo do tempo. A falta de informações estruturadas pode contribuir para problemas como excesso ou falta de estoque, desperdício, compras mal planejadas e perda de oportunidades comerciais.

Além disso, pequenos negócios nem sempre possuem acesso a ferramentas de análise de dados simples, acessíveis e adequadas à sua realidade.

Diante desse cenário, o projeto propõe a criação de uma plataforma de Business Intelligence capaz de receber, organizar e analisar dados históricos de vendas, apresentando indicadores visuais e de fácil interpretação para auxiliar o empreendedor na tomada de decisões.

Nesta primeira versão, a solução terá caráter descritivo e analítico, sem utilização de modelos de análise preditiva ou inteligência artificial para previsão de demanda.

---

## 5. Desafio escolhido na plataforma CORETO

**Desafio:** Previsão de demanda para pequenos negócios

**Link do desafio:**  
`INSERIR LINK DO DESAFIO CORETO`

Embora o desafio contemple previsão de demanda, a primeira versão do projeto será focada na estruturação dos dados e na análise histórica das vendas, criando uma base confiável para futuras evoluções da solução.

---

## 6. Objetivo da solução

Desenvolver uma plataforma de Business Intelligence simples, acessível e reutilizável para pequenos negócios, permitindo que cada empresa envie seus próprios dados de vendas e acompanhe indicadores de desempenho em um ambiente individualizado.

A plataforma deverá permitir o cadastro e acesso de cada empresa, o download de um modelo padrão de planilha, o envio dos dados de vendas, a validação dessas informações e a visualização de dashboards específicos para cada cliente.

O objetivo é transformar registros simples de vendas em informações organizadas e úteis para apoiar decisões relacionadas ao desempenho comercial, produtos, períodos de maior movimento e planejamento operacional.

---

## 7. Público beneficiado

A solução será direcionada principalmente para:

- microempreendedores individuais;
- micro e pequenas empresas;
- mercadinhos;
- padarias;
- lojas de bairro;
- farmácias;
- restaurantes;
- pequenos estabelecimentos comerciais;
- empreendedores que atualmente utilizam planilhas ou registros simples para acompanhar suas vendas.

A interface será pensada para usuários com baixa ou média familiaridade com ferramentas de análise de dados.

---

## 8. Funcionamento da solução

A plataforma deverá funcionar por meio de um fluxo simples, padronizado e de fácil utilização.

### 8.1 Cadastro e login

Cada empresa terá uma conta própria na plataforma.

O usuário realizará o acesso por meio de login e senha, permitindo que os dados de cada negócio sejam identificados e separados corretamente.

Cada conta estará associada a um identificador único da empresa.

Exemplo:

`Empresa 001 → Cliente A`

`Empresa 002 → Cliente B`

`Empresa 003 → Cliente C`

Esse identificador permitirá que os registros sejam armazenados em uma estrutura centralizada, mantendo os dados separados logicamente por empresa.

---

### 8.2 Área do cliente

Após realizar o login, o usuário terá acesso a uma área própria contendo:

- opção para baixar o modelo padrão de planilha;
- opção para enviar a planilha preenchida;
- informações sobre o último envio realizado;
- mensagens de validação dos dados;
- acesso ao dashboard da empresa.

---

### 8.3 Download do modelo de planilha

A plataforma disponibilizará um botão como:

**“Baixar modelo de planilha”**

O arquivo terá uma estrutura padronizada para facilitar o tratamento e a importação dos dados.

Campos previstos:

| Campo | Descrição |
|---|---|
| Data da venda | Data em que a venda ocorreu |
| Produto | Nome do produto vendido |
| Categoria | Categoria do produto |
| Quantidade | Quantidade vendida |
| Valor unitário | Valor unitário do produto |
| Valor total | Valor total da venda |

O uso de um modelo padrão reduz problemas relacionados à desorganização dos dados e facilita a utilização da solução por diferentes empresas.

---

### 8.4 Envio da planilha

Após preencher o modelo, o usuário poderá acessar a opção:

**“Enviar dados de vendas”**

A plataforma permitirá o upload de arquivos em formato CSV ou Excel.

Antes da importação, o sistema realizará validações básicas, verificando:

- presença das colunas obrigatórias;
- formato das datas;
- campos vazios;
- valores numéricos inválidos;
- registros incompletos.

Caso sejam encontrados problemas, o sistema deverá informar ao usuário quais dados precisam ser corrigidos.

---

### 8.5 Tratamento dos dados

A planilha será utilizada apenas como forma de entrada das informações.

Após o upload, os dados serão:

1. lidos pelo sistema;
2. validados;
3. tratados;
4. padronizados;
5. associados ao identificador da empresa;
6. armazenados no banco de dados.

Dessa forma, a solução não dependerá da planilha como armazenamento definitivo.

---

### 8.6 Identificação da base de cada empresa

Cada registro importado será vinculado automaticamente ao identificador da empresa que realizou o upload.

Exemplo:

| id_empresa | data | produto | categoria | quantidade | valor_total |
|---|---|---|---|---:|---:|
| 001 | 01/09/2026 | Refrigerante | Bebidas | 3 | 27,00 |
| 001 | 01/09/2026 | Pão | Padaria | 20 | 16,00 |
| 002 | 01/09/2026 | Shampoo | Higiene | 2 | 35,00 |

Os dados de diferentes empresas poderão ser armazenados em uma mesma estrutura de banco de dados, utilizando o campo `id_empresa` para identificar a qual cliente cada registro pertence.

Essa abordagem evita a criação de uma planilha ou banco independente para cada empresa, facilitando a manutenção e a escalabilidade da solução.

---

### 8.7 Dashboard individual

Depois do processamento dos dados, o usuário terá acesso ao dashboard correspondente à própria empresa.

O painel apresentará indicadores como:

- faturamento total;
- quantidade vendida;
- quantidade de vendas;
- ticket médio;
- produtos mais vendidos;
- produtos com menor saída;
- desempenho por categoria;
- vendas por dia, semana e mês;
- períodos de maior e menor movimento.

O usuário também poderá utilizar filtros para analisar períodos, produtos e categorias específicas.

---

## 9. Funcionalidades previstas para a primeira versão

### 1. Cadastro e login de empresas

Permitir que cada empresa possua acesso individual à plataforma, garantindo a identificação do usuário e a separação dos dados entre os clientes.

### 2. Download do modelo padrão de planilha

Disponibilizar um arquivo modelo contendo a estrutura necessária para o envio dos dados de vendas.

### 3. Upload e validação dos dados

Permitir o envio de arquivos CSV ou Excel e realizar validações antes da carga das informações.

### 4. Dashboard individual de vendas

Apresentar indicadores e visualizações específicas da empresa autenticada, incluindo faturamento, volume de vendas, produtos e comportamento das vendas ao longo do tempo.

### 5. Filtros e análises interativas

Permitir que o usuário explore seus dados utilizando filtros por período, produto e categoria.

---

## 10. Tecnologias previstas

### Front-end

**Next.js + React**

Serão utilizados para o desenvolvimento da interface da plataforma.

O front-end será responsável por:

- tela de cadastro;
- tela de login;
- área do cliente;
- download do modelo da planilha;
- upload dos arquivos;
- mensagens de validação;
- navegação até os dashboards.

---

### Back-end

**Python + FastAPI**

Será responsável pelas regras de negócio e pela comunicação entre a interface, o banco de dados e os processos de tratamento das informações.

O back-end deverá:

- autenticar os usuários;
- identificar a empresa vinculada ao usuário;
- receber os arquivos enviados;
- validar os dados;
- processar as informações;
- armazenar os registros no banco de dados;
- disponibilizar informações para a aplicação.

---

### Banco de dados

**PostgreSQL**

Será utilizado como banco de dados relacional central da plataforma.

Os dados de diferentes empresas poderão ser armazenados em uma mesma estrutura, utilizando um identificador único (`id_empresa`) para relacionar cada registro ao respectivo cliente.

Essa estrutura facilita a manutenção, organização e futura expansão da solução.

---

### Tratamento e preparação dos dados

**Python + Pandas**

Serão utilizados para:

- leitura dos arquivos Excel e CSV;
- validação das colunas obrigatórias;
- identificação de campos vazios;
- padronização de datas;
- conversão de valores numéricos;
- tratamento de inconsistências;
- preparação dos dados antes da gravação no PostgreSQL.

---

### Business Intelligence

**Power BI**

Será utilizado para a construção dos dashboards e indicadores de desempenho.

Entre os indicadores previstos estão:

- faturamento;
- quantidade vendida;
- número de vendas;
- ticket médio;
- produtos mais vendidos;
- produtos com menor saída;
- vendas por categoria;
- evolução das vendas;
- períodos de maior e menor movimento.

---

### Autenticação

A plataforma utilizará um sistema de autenticação baseado em login e senha.

Será utilizado **JWT (JSON Web Token)** para controlar a autenticação e o acesso dos usuários à aplicação.

Cada usuário estará vinculado a uma empresa, permitindo que o sistema identifique quais dados pertencem a cada cliente.

---

### Entrada dos dados

Inicialmente serão aceitos arquivos:

- `.xlsx`;
- `.csv`.

A plataforma disponibilizará um modelo padrão para download, facilitando a organização e a importação das informações.

---

### Versionamento e colaboração

**GitHub**

Será utilizado para:

- armazenamento do código-fonte;
- controle de versões;
- documentação;
- colaboração entre os integrantes da equipe.

---

### Gestão do projeto

**GitHub Projects ou Trello**

Será utilizado para acompanhamento das tarefas, responsáveis, prazos e evolução do projeto.

---

## 11. Arquitetura inicial da solução

O fluxo tecnológico da plataforma será:

**Usuário**

↓

**Next.js + React**

Interface da plataforma

↓

**FastAPI**

Autenticação, regras de negócio e recebimento dos arquivos

↓

**Python + Pandas**

Validação, tratamento e padronização dos dados

↓

**PostgreSQL**

Armazenamento estruturado e identificação por empresa

↓

**Power BI**

Análise e visualização dos indicadores

---

## 12. Segurança e separação dos dados

Os dados enviados por uma empresa não deverão ser acessíveis por outras empresas cadastradas.

Cada registro será relacionado ao identificador único da empresa autenticada.

O sistema deverá garantir que as informações apresentadas estejam associadas corretamente à empresa do usuário conectado.

As senhas dos usuários não deverão ser armazenadas em texto simples, sendo necessário utilizar técnicas adequadas de segurança, como hash de senha.

A implementação detalhada das regras de autenticação, autorização e segurança será evoluída durante o desenvolvimento do projeto.

---

## 13. Escopo inicial

A primeira versão do projeto terá foco em:

- cadastro e login de empresas;
- padronização da entrada dos dados;
- upload de arquivos;
- validação das informações;
- tratamento dos dados;
- armazenamento centralizado;
- identificação dos registros por empresa;
- análise histórica das vendas;
- visualização de indicadores;
- apoio à tomada de decisão.

Não fazem parte inicialmente do escopo:

- previsão estatística de demanda;
- machine learning;
- inteligência artificial generativa;
- integração automática com sistemas ERP;
- integração com maquininhas de pagamento;
- utilização automática de dados climáticos;
- previsão automática de estoque;
- dimensionamento automático de equipes.

Essas funcionalidades poderão ser avaliadas como possíveis evoluções futuras da plataforma.

---

## 14. Resultado esperado

Ao final da primeira versão, espera-se disponibilizar uma plataforma simples e intuitiva, capaz de receber dados de vendas de diferentes pequenos negócios, validar e organizar essas informações e transformá-las em indicadores visuais.

O empreendedor deverá conseguir acessar sua própria conta, enviar seus dados de vendas e visualizar um dashboard individual com informações sobre desempenho comercial, produtos, categorias e comportamento das vendas ao longo do tempo.

A proposta busca facilitar a adoção de uma cultura de tomada de decisão baseada em dados entre micro e pequenos empreendedores, oferecendo uma solução acessível e de baixa complexidade de utilização.
