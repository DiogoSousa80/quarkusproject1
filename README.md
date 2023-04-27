código-com-quarkus
Este projeto usa Quarkus, o Supersonic Subatomic Java Framework.

Se quiser saber mais sobre o Quarkus, visite o site: https://quarkus.io/ .

Executando o aplicativo no modo dev
Você pode executar seu aplicativo no modo dev que permite a codificação ao vivo usando:

./mvnw compila quarkus:dev
OBSERVAÇÃO: o Quarkus agora vem com uma IU de desenvolvedor, disponível apenas no modo de desenvolvedor em http://localhost:8080/q/dev/.

Empacotando e executando o aplicativo
O aplicativo pode ser empacotado usando:

./mvnw pacote
Ele produz o arquivo quarkus-run.jar no diretório target/quarkus-app/. Esteja ciente de que não é um über-jar, pois as dependências são copiadas para o diretório target/quarkus-app/lib/.

O aplicativo agora pode ser executado usando java -jar target/quarkus-app/quarkus-run.jar.

Se você deseja construir um über-jar, execute o seguinte comando:

./mvnw pacote -Dquarkus.package.type=uber-jar
O aplicativo, empacotado como um über-jar, agora pode ser executado usando java -jar target/*-runner.jar.

Criando um executável nativo
Você pode criar um executável nativo usando:

./mvnw pacote -Pnative
Ou, se você não tiver o GraalVM instalado, pode executar o build executável nativo em um contêiner usando:

./mvnw pacote -Pnative -Dquarkus.native.container-build=true
Você pode então executar seu executável nativo com: ./target/code-with-quarkus-1.0.0-SNAPSHOT-runner

Se você quiser saber mais sobre a criação de executáveis nativos, consulte https://quarkus.io/guides/maven-tooling.

Guias Relacionados
JDBC Driver - H2 (guia): Conecte-se ao banco de dados H2 via JDBC
Hibernate ORM com Panache (guia): Simplifique seu código de persistência para Hibernate ORM por meio do registro ativo ou do padrão de repositório
Código fornecido
Hibernar ORM
Crie sua primeira entidade JPA

Seção do guia relacionado...

Hibernate relacionado com a seção Panache...

RESTEasy Reativo
Inicie facilmente seus serviços Web RESTful reativos

Seção do guia relacionado...
