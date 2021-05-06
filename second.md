## **5. Blockquotes**
<br>

사용법)

블럭 인용을 위해서는 문단 앞에 >을 붙이면 됩니다. 이 때 문단 사이에 빈 줄에도 >을 추가함으로서 여러 개의 문단을 포함할 수도 있고, >>를 사용하여 블럭 인용 내에 또다른 블럭 인용을 추가할 수도 있습니다. 뿐만 아니라, 다른 마크다운 요소을 블럭 내에서 인용하는 것도 가능합니다. 

<br>

- 예시

    \> ## The quarterly results look great!<br>
    \><br>
    \>\> - Revenue was off the chart.<br>
    \>\> - Profits were higher than ever.<br>
    \><br>
    \>  \*Everything\* is going according to \*\*plan\*\*.<br>

<br>

- 실제로 나타나는 모양

    >  ## The quarterly results look great!
    >
    >> - Revenue was off the chart.
    >> - Profits were higher than ever.
    >
    >  *Everything* is going according to **plan**.

<br><br><hr/>

## **6. Lists**
<br>

### 6-1. Ordered Lists 
<br>

사용법)

순서를 갖춘 목록 작성을 위해서는 1. , 2. 과 같이 순서를 매길 수 있습니다. 이때 주의할 점은, 1부터 시작해야 한다는 것입니다. 또한 순서 리스트가 1부터 시작했다면, 그 후에 이어지는 리스트의 번호는 자동으로 순차적으로 작성됩니다. 또한, Blockquotes에서 블럭 인용 내에 또 다른 블럭을 인용했듯, 순서 리스트 내에 순서 리스트를 포함시킬 수도 있습니다.

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | 1. First item<br>2. Second item<br>3. Third item<br>4. Fourth item      | \<ol><br>\<li>First item\</li><br>\<li>Second item\</li><br>\<li>Third item\</li><br>\<li>Fourth item\</li><br>\</ol>       |
<br>

<br>

### 6-2. Unordered Lists
<br>

사용법)

순서없는 목록 작성을 위해서는, Ordered list에서 사용한 1.,2. 와 같이 숫자 대신 -,+,*,와 같은 기호를 이용하여 목록을 표시할 수 있습니다. 또한 Ordered List의 경우처럼, 리스트 내에 또 다른 리스트를 포함시킬 수도 있습니다. 

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | \- First item<br>- Second item<br>- Third item<br>- Fourth item      | \<ul><br>\<li>First item\</li><br>\<li>Second item\</li><br>\<li>Third item\</li><br>\<li>Fourth item\</li><br>\</ul>       |

<br>
- 참고

<br> 1. Unordered List의 경우 +,-,* 중 하나만 사용하도록 합니다. (혼용하지 맙시다)
<br> 2. List 내에 마크다운 요소를 포함하고 싶다면, 4개의 빈칸이나 tab 1개를 입력한 후 입력하면 됩니다.

<br><br><hr/>

## **7. Code**
<br>

사용법)

단어나 문장을 코드라고 명시하고 싶다면, \` 기호로 감싸면 됩니다. 또한, 코드라고 명시하고 싶은데 그 속에 \`기호가 이미 존재할 때는 \``기호를 이용하여 감싸면 됩니다. 마지막으로 코드 블럭을 생성하고 싶다면, 그 코드 블럭의 모든 라인을 space 4개나 1개의 tab으로 들여 쓰면 됩니다.

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | At the command prompt, type \`nano\`.      | At the command prompt, type \<code>nano\</code>.       |
    | \`\`Use \`code\` in your Markdown file.\`\`       | \<code>Use \`code\` in your Markdown file.\</code>      |


<br><br><hr/>

## **8. Horizontal Rules**
<br>

사용법)

수평줄의 입력을 위해서는, *, -, _ 중 한 개를 3번 이상 입력하면 됩니다. 이때 Heading의 표현 방법과 구분하기 위하여, 반드시 빈 줄을 위아래에 삽입해주도록 합시다.


<br><br><hr/>

## **9. Links**
<br>

사용법)

만약 당신이 ARS1이라는 링크 제목을 통해 www.URL1.com이라는 주소로 연결하고 싶다면, 다음과 같이 사용하면 됩니다.

    My favorite search engine is [ARS1](www.URL1.com).

> My favorite search engine is [ARS1](www.URL1.com).

<br>

이때 사용자의 편의를 위해 주소 위에 설명을 추가해줄 수도 있습니다. 이 설명은 커서를 올릴 때 나타납니다.

     My favorite search engine is [ARS1](www.URL1.com "Most Interesting Site Ever").

> My favorite search engine is [ARS1](www.URL1.com "Most Interesting Site Ever").

<br>

또 다른 방법으로, URL이나 이메일을 바로 링크로 변환하고 싶다면, <> 기호를 이용할 수도 있습니다.

    <https://www.naver.com/>

> <https://www.naver.com/>

<br>

링크를 강조하기 위해서는, 위 Emphasis 문서에서 했듯이, * 기호로 링크 코드 전체를 감싸주면 됩니다.

    I love supporting the **[EFF](https://eff.org)**.  
    This is the *[Markdown Guide](https://www.markdownguide.org)*.  
    See the section on [`code`](#code).  

> I love supporting the **[EFF](https://eff.org)**.  
    This is the *[Markdown Guide](https://www.markdownguide.org)*.  
    See the section on [`code`](#code).  

<br>

또한, 소스 문서의 가독성을 높이기 위해서 참조형 링크를 생성하여 코드를 작성할 수도 있습니다. 참조형 링크는 글 내에 참조 링크를 삽입하고, 파일 다른 곳에 링크 정의와 참조되는 링크의 주소를 써놓을 수 있습니다.  
먼저, 참조번호를 삽입해 봅시다.

     [링크][1]

그리고 다음과 같은 방법을 통해 참조되는 링크를 표기해놓을 수 있습니다. 

     [1]: https://www.markdownguide.org/ "Markdown"

참조번호와 참조되는 링크를 사용하면 [이런 식으로][1] 나타납니다.

[1]: https://www.markdownguide.org/ "Markdown"

우리는 이러한 방법을 통해 소스코드의 가독성을 높이고, 수정을 용이하게 만들 수 있습니다.

<br><br><hr/>

## **9. Images**
<br>

사용법)

이미지 추가를 위해서는, 느낌표를 이용하여 다음과 같이 사용합니다. 미리보기 설명을 추가하고 싶다면, 파일 경로 뒤에 큰따옴표를 이용하여 표기해주면 됩니다.

    형태)
    ![텍스트](이미지파일경로.jpg)
    ![텍스트](이미지파일URL)
    [![텍스트](이미지URL이나 경로)](링크URL) // 이미지에 링크기능 추가

    사용 예)  
    ![Whether it's a dream or a real life](Starrain-typeA.jpg)


예시)

>![IMAGINE](Starrain-typeA.jpg "Whether it's a dream or a real life")






<br><br><hr/>

## **10. Escaping Characters**
<br>

사용법)

때로는 마크다운 문서에서 문자 수정을 위해 사용되는 리터럴 문자를 있는 그대로 나타내기 위해서는 탈출 문자 '\\'를 이용해야 합니다. 마크다운에서 탈출 문자를 다음과 같은 문자들 앞에 삽입한다면 이 문자들을 결과화면에 나타낼 수 있습니다.


| Character      | Name |
| ----------- | ----------- |
| \      | backslash       |
| `      | backtick (see also escaping backticks in code)       |
| *      | asterisk       |
| _      | underscore       |
| { }      | curly braces       |
| [ ]      | brackets       |
| < >      | angle brackets       |
| ( )      | parentheses       |
| #      | pound sign       |
| +      | plus sign       |
| -      | minus sign (hyphen)       |
| .      | dot       |
| !      | exclamation mark       |
| |      | pipe (see also escaping pipe in tables)       |

<br><hr/><br>

추가) 마크다운은 마크다운 문서 내에서 HTML 문법을 사용하는 것을 허용합니다. 만약 당신이 HTML 문법을 사용하고 싶다면, 그렇게 하면 됩니다.

GFM) <https://github.com/eckhuango/start_github/blob/main/README.md>