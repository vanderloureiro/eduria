## Eduria

You can use the [editor on GitHub](https://github.com/vanderloureiro/eduria/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Integração

Para integrar com a aplicação principal, o serviço de inteligência deve dispor de um \textit{endpoint} com o verbo POST que receba um JSON e retorne um segundo JSON com \textit{StatusCode} da requisição com código \textit{200 OK}. O caminho para esse \textit{endpoint} deve ser informado no cadastro do curso.

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
