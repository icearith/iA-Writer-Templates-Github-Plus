author: Arith Xu
data-title: 123
project_home: https://arithxu.com
- - -

@(Guide)[iA Writer|Manual|Markdown|🎩]

{{TOC}}

## Note Tags
This theme adds `@(Note Title)[tag1|tag2|tag3]` syntax to implement tag function. However, only put this statement at the **“start”** of the document can it be rendered. This is a trade off with performance.

@(Guide)[iA Writer|Manual|Markdown|🎩]

As you can see, if you put the statement above, it will not be rendered.

## Quote blocks
> **Note:** this is a quotation block, you can use nested markdown markup here. For example, **bold** text, *italic* text, even images:
>
> ![](https://ia.net/wp-content/themes/ia5/assets/img/logo-ia-writer-basic.gif)


## LaTeX Math Expressions
### Normal mode

This is a normal math equation in normal mode. $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ , use `$…$` as delimiter.

### Display mode
$${
J(\theta_0, \theta_1) =  \frac{1}{2m} \sum_{i=1}^{m} \big( h_{\theta}(x^{(i)}) - y^{(i)}   \big)^2
}$$

$${
    h_{\theta}(x) = \begin{bmatrix}
                        \theta_0 & \theta_1 & \cdots & \theta_n \\
                    \end{bmatrix}
                    \begin{bmatrix}
                        x_0 \\
                        x_1 \\
                        \vdots \\
                        x_n \\
                    \end{bmatrix} = {\theta}^{T}x
}$$  

## Code Blocks

> **Tips:** Code highlight support most popular programming languages and configuration files.

> Please check [highlight.js][1] for more information.  

### C
```c
#include <stdio.h>

int main(){
	/* this is a print statement */
	printf("Hello, World!");
}
```

### Go
```go
// You can edit this code!
// Click here and start typing.
package main

import "fmt"

func main() {
	fmt.Println("Hello, 世界")
}
```

### HTML
```html
<html>
	<p style="color:red;">
		Mozilla, we’re a global community of
	</p>
	<ul>
	  <li>technologists</li>
	  <li>thinkers</li>
	  <li>builders</li>
	</ul>
</html>
```

### Python
```python
@requires_authorization
def somefunc(param1='', param2=0):
    '''A docstring'''
    if param1 > param2: # interesting
        print 'Greater'
    return (param2 - param1 + 1) or None
class SomeClass:
    pass
>>> message = '''interpreter
... prompt'''
```

## Table
### Markdown table
|              | Grouping                    ||  
| First Header | Second Header | Third Header |  
| ------------ | :-----------: | -----------: |  
| Content      | *Long Cell*                 ||  
| Content      | **Cell**      | Cell         |  
| New section  | More          | Data         |

### CSV table
/example.csv

## Checkbox

- [x] Flow chart
- [x] Sequence chart
- [x] Note tags
- [ ] Mathematical chart
- [ ] Data visualization chart

## Charts
> **Note:** You can find more information:

> - Check **Sequence diagrams** syntax [here][3],
> - Check **Flow charts** syntax [here][4].


### Flow Chart
```flow
st=>start: Start|past:>http://www.google.com[blank]
e=>end: End:>http://www.google.com
op1=>operation: My Operation|past
op2=>operation: Stuff|current
sub1=>subroutine: My Subroutine|invalid
cond=>condition: Yes
or No?|approved:>http://www.google.com
c2=>condition: Good idea|rejected
io=>inputoutput: catch something...|request

st->op1(bottom)->cond
cond(yes, right)->c2
cond(no)->sub1(left)->op1
c2(yes)->io->e
c2(no)->op2->e
```

### Sequence Chart

#### Sequence chart with simple theme
```sequence
A->B: Does something
```

#### Sequence chart with handwriting theme
```sequence_hand
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D->>D: Self 
D-->>A: Dashed open arrow
```

### Links
#### Audio Links 

A audio link is a markdown link with a specific link parameters `?ml_type=audio`. Here is an example:

```markdown 
[link](https://www.arithxu.com/test.mp3?ml_type=audio)
```

| Punctuation | Pronunciation |
|:--:|:--:|
| `!` | [link](https://www.oxfordlearnersdictionaries.com/media/english/uk_pron/e/exc/excla/exclamation_mark_1_gb_1.mp3?ml_type=audio) |

> ![](markdown.png)


[image3]: markdown.png "This is where the title goes" height=22px width=60px
This is the same image ![image3][] but with the attributes placed later on in the document.

Here is some text containing a footnote[^somesamplefootnote]. You can then continue your thought...

This is a {==test==}.

background-color: transparent;
background-image: linear-gradient(to bottom, rgba(39, 243, 106, .1), rgba(39, 243, 106, .1));



[1]: http://highlightjs.org
[2]: https://chrome.google.com/webstore/detail/kidnkfckhbdkfgbicccmdggmpgogehop
[3]: http://bramp.github.io/js-sequence-diagrams/
[4]: http://flowchart.js.org

