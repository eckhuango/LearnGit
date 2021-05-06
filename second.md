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
