## Download

<dl>
<dt>Eduria-core</dt>
<dd>[Clone ou download](https://github.com/vanderloureiro/eduria-core).</dd>
<dt>Eduria-decision-tree</dt>
<dd>[Clone ou download](https://github.com/vanderloureiro/eduria-decision-tree).</dd>
<dt>Eduria-test</dt>
<dd>[Clone ou download](https://github.com/vanderloureiro/eduria-test).</dd>
</dl>

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

### Suporte ou Contato

Em caso de dúvidas, é possível realizar contato por [Linkedin](https://www.linkedin.com/in/vanderloureiro/) ou pelo email vanderloureiro.dev@gmail.com


---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```

