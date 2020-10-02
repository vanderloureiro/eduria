# Download

Projeto Eduria busca auxiliar o desenvolvimento de novos STIs em arquitetura de microsserviços. Realize o download e conheça:

*   [Eduria-core](https://github.com/vanderloureiro/eduria-core)
*   [Eduria-decision-tree](https://github.com/vanderloureiro/eduria-decision-tree)
*   [Eduria-test](https://github.com/vanderloureiro/eduria-test)

### Integração

Para integrar com a aplicação principal, o serviço de inteligência deve dispor de um _endpoint_ com o verbo POST que receba um JSON e retorne um segundo JSON com _StatusCode_ da requisição com código _200 OK_. O caminho para esse _endpoint_ deve ser informado no cadastro do curso.

```
{
    "registerUuid": string,
    "studentId": number,
    "studentAge": number,
    "courseName": string,
    "easyQuestionsAnsweredCorrect": number,
    "mediumQuestionsAnsweredCorrect": number,
    "hardQuestionsAnsweredCorrect": number,
    "qttAllQuestionsAnswered": number,
    "qttAllCourseQuestions": number,
    "score": number,
    "lastQuestionLevel": string,
    "lastQuestionWasAnsweredCorrect": string
}
```

O JSON de resposta é mais simples que o primeiro, tendo apelas dois atributos:

```
{
    "registerUuid": string,
    "selectedLevel": string
}
```

### Motivação

Softwares educacionais podem ser instrumentos transformadores no processo de ensino e aprendizagem, dentre esses softwares existem os Sistemas Tutores Inteligentes, STIs são softwares educacionais aperfeiçoados com técnicas de inteligência artificial para proporcionar um ensino mais adaptável e exclusivo ao aluno. O desenvolvimento de software trás dificuldades arquiteturais à medida que cresce e essas dificuldades levaram ao padrão de microsserviços. Entretanto, ainda não foram encontrados registros de STIs construídos em uma arquitetura de microsserviços. Visto isso, foi buscando realizar um apoio na construção e experimentação de novos STIs por terceiros nessa arquitetura. Foi realizado o desenvolvimento de dois microsserviços em forma de abstrações para módulos de um STI. Os microsserviços desenvolvidos apresentaram o comportamento esperado tanto em termos de integração, como em regras de negócio de ensino e análise de nível de aluno.

### Instalação

Todos são projetos Spring com dependências descritas no arquivo pom.xml

Crie um banco de dados e informe os dados no arquivo aplication-dev.properties em caso de ambiente de desenvolvimento ou application-prod.properties em caso de ambiente de produção.

Execute no terminal dentro da pasta do projeto:
```
mvn clean compile
```

### Como rodar

Execute no terminal dentro da pasta do projeto:
```
mvn spring-boot:run
```

### Portas

| Serviço       | Porta  | Swagger                                |
|:--------------|:-------|:---------------------------------------|
| core          | 3332   | http://localhost:3332/swagger-ui.html  |
| decision-tree | 3334   | http://localhost:3332/swagger-ui.html  |
| test          | 3336   | http://localhost:3332/swagger-ui.html  |


### Entidades do Eduria-core

![Branching](https://guides.github.com/activities/hello-world/branching.png)

### Suporte ou Contato

Em caso de dúvidas, é possível realizar contato por [Linkedin](https://www.linkedin.com/in/vanderloureiro/) ou pelo email vanderloureiro.dev@gmail.com


