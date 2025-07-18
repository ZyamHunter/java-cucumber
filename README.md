## Projeto java-cucumber

Este projeto demonstra o uso de BDD com Cucumber, Java 11, JUnit e Maven para automação de testes de funcionalidades diversas, incluindo manipulação de arrays, listas, strings, números e dicionários.

### Estrutura do Projeto

- `src/main/java/com/example/App.java`: Classe principal (exemplo).
- `src/test/java/com/example/steps/`: Step definitions para cada feature.
  - `HomeSteps.java`, `ArraySteps.java`, `StringSteps.java`, `NumeroSteps.java`, `DicionarioSteps.java`
- `src/test/resources/features/`: Features Gherkin.
  - `home.feature`, `array.feature`, `string.feature`, `numero.feature`, `dicionario.feature`
- `src/test/java/com/example/runners/RunCucumberTest.java`: Runner do Cucumber.
- `pom.xml`: Configuração do Maven e dependências.

### Dependências Principais

- Java 11
- Maven
- Cucumber (cucumber-java, cucumber-junit)
- JUnit 4

### Como Executar os Testes

1. Instale as dependências:
   ```sh
   mvn clean install
   ```
2. Execute os testes:
   ```sh
   mvn test
   ```

### Funcionalidades Cobrindo

**Home:** Exemplo básico de feature.
**Arrays:** Manipulação, geração aleatória, inversão, ordenação, remoção de duplicados, etc.
**Strings:** Manipulação de strings, concatenação, inversão, busca, etc.
**Números:** Operações matemáticas, fatorial, raiz, máximo/mínimo, primo, etc.
**Dicionários:** Adição, remoção, busca, atualização, listagem de chaves/valores, etc.

### Exemplo de Feature (arrays)

```gherkin
Feature: Manipulação de Arrays
  Scenario: Inverter um array
    Given um array aleatório de tamanho 5
    When inverto o array
    Then o array deve ser invertido corretamente
```

### Observações

- Todos os steps estão implementados em Java, utilizando apenas lógica de negócio (sem Selenium).
- O projeto é facilmente extensível para novas features e cenários.
