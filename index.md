## Eduria

Softwares educacionais podem ser instrumentos transformadores no processo de ensino e aprendizagem, dentre esses softwares existem os Sistemas Tutores Inteligentes, STIs são softwares educacionais aperfeiçoados com técnicas de inteligência artificial para proporcionar um ensino mais adaptável e exclusivo ao aluno. O desenvolvimento de software trás dificuldades arquiteturais à medida que cresce e essas dificuldades levaram ao padrão de microsserviços. Entretanto, ainda não foram encontrados registros de STIs construídos em uma arquitetura de microsserviços. Visto isso, foi buscando realizar um apoio na construção e experimentação de novos STIs por terceiros nessa arquitetura. Foi realizado o desenvolvimento de dois microsserviços em forma de abstrações para módulos de um STI. Os microsserviços desenvolvidos apresentaram o comportamento esperado tanto em termos de integração, como em regras de negócio de ensino e análise de nível de aluno.

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

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/vanderloureiro/eduria/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Suporte ou Contato

Em caso de dúvidas, é possível realizar contato por [Linkedin](https://www.linkedin.com/in/vanderloureiro/) ou pelo email vanderloureiro.dev@gmail.com
