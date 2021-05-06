# **Basic Syntax**

<br>

## **0. Overview**

<br>

아래 내용은 markdown의 기본 문법들을 설명합니다.

<br>
<hr/>

## **1. Headings**
<br>

사용법 1)

Heading을 위해서는, 단어나 구문 앞에 '#'을 삽입하면 됩니다. 이때 '#'의 개수는 Heading level과 동일합니다. 또한, Heading level은 level 6까지만 허용합니다.

<br>

- HTML과의 비교


    | Markdown      | HTML |
    | ----------- | ----------- |
    | # Heading level 1      | \<h1>Heading level 1\</h1>       |
    | ## Heading level 2      | \<h2>Heading level 2\</h2>       |
    | ### Heading level 3      | \<h3>Heading level 3\</h3>       |
    | #### Heading level 4      | \<h4>Heading level 4\</h4>       |
    | ##### Heading level 5      | \<h5>Heading level 5\</h5>       |
    | ###### Heading level 6      | \<h6>Heading level 6\</h6>       |

<br><br>

사용법 2)

글 밑에 선을 긋는 방법으로 대체 가능합니다. 이때 대체의 방법으로는 -과 =의 두 가지 방법이 있습니다.  


<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | Heading level 1<br>===============      | \<h1>Heading level 1\</h1>       |
    | Heading level 2<br>---------------      | \<h2>Heading level 2\</h2>       |

<br><br><hr/>

## **2. Paragraphs**
<br>

사용법) 

문단을 구분하기 위하여, 하나 혹은 하나 이상의 빈 줄을 추가하면 됩니다.

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | I really like using Markdown.<br><br>I think I'll use it to format all of my documents from now on.      |\<p>I really like using Markdown.\</p><br>\<p>I think I'll use it to format all of my documents from now on.\</p>       |

<br><br><hr/>

## **3. Line breaks**
<br>

사용법) 

개행을 위해서는 한 줄을 작성한 후 띄어쓰기 두 개 이상을 사용하고 엔터를 누르면 됩니다.

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | This is the first line. <br>And this is the second line.      | \<h1>Heading level 1\</h1>       |
<br>

- 참고
<br> HTML tag를 이용해서도 개행을 할 수 있습니다.

<br><br><hr/>

## **4. Emphasis**
<br>

### 4-1. Bold 
<br>

사용법)

볼드체 작성을 위해서는 **나 __으로 볼드체가 되길 원하는 텍스트를 감싸주면 됩니다. 이때, 일반적으로 __보다는 **을 많이 사용합니다.

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | I just love \*\*bold text**.      | I just love \<strong>bold text\</strong>.       |
    | I just love \_\_bold text__.      | I just love \<strong>bold text\</strong>.       |
    | Love\*\*is**bold       | Love\<strong>is\</strong>bold
<br>

<br>

### 4-2. Italic
<br>

사용법)

이태릭체 작성을 위해서는 *나 _으로 볼드체가 되길 원하는 텍스트를 감싸주면 됩니다. 이때, 일반적으로 _보다는 *을 많이 사용합니다.

<br>

- HTML과의 비교

    | Markdown      | HTML |
    | ----------- | ----------- |
    | Italicized text is the \*cat's meow*.      | Italicized text is the \<em>cat's meow\</em>.       |
    | Italicized text is the \_cat's meow_.      | Italicized text is the \<em>cat's meow\</em>.       |
    | A\*cat*meow       | A\<em>cat\</em>meow

<br>
- 참고

<br> 1. _ 기호보다는 * 기호를 이용하는 방법이 더 선호됩니다.
<br> 2. Bold와 Italic 두 가지 방법을 동시에 적용하고 싶다면, ***이나 ___을 띄어쓰기 없이 사용하면 됩니다.

<br><br><hr/>
