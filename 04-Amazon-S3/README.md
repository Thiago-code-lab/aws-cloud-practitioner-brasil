# 4. Amazon Simple Storage Service (S3)

## 4.1. O que é o Amazon S3

- **Definição:** S3 faz parte da camada de infraestrutura da AWS, oferecendo armazenamento escalável sob demanda por meio de APIs, sem que o usuário gerencie hardware, sistemas de arquivos ou servidores.

- **Modelo de Serviço:** IaaS. (às vezes também referido como Storage as a Service)

## 4.2. Conceitos principais

- **Buckets:**
  - **Conceito:**  Um Bucket no S3 é um recipiente onde podem ser armazenados objetos, para armazenar um novo objeto é necessário associá-lo a um bucket.
  - **Nome único global**: Os buckets devem possuir um nome único global entre todas as regiões e todas as contas.
  - **Definição limitada a uma região**: Apesar de o nome do bucket ser único, o S3 não é um serviço global ele deve ser definido em uma região.
  - **Convenção de nomes:**
    - Sem letras maiúsculas, sem o caracter de underscore "_"
    - Tamanho de 3 a 63 caracteres
    - Não pode ser um IP
    - Deve começar com uma letra minúscula ou um número.
    - Não pode começar com o prefixo xn-
    - Não pode terminar com o sufixo -s3alias

- **Objects**
  - **Conceito**: Os objetos são arquivos que são armazenado em um Bucket, eles possuem um chave (**key**) associada a eles que é formada a partir do caminho completo até o objeto.
  - **S3 não trabalha com o conceito de diretórios**: Apesar de comumente utilizar uma estrutura semelhante a de diretórios que utilizamos em nossos computadores, o S3 não utiliza tal conceito, ele apenas possui chaves como nome longos que contém barras.
  - **Upload máximo de 5 TB**: O tamanho máximo de um objeto que pode ser enviado de uma só vez é 5 TB, caso o arquivo seja maior do que isso deve ser utilizado o "multi-part upload".
