## Choose a Genre - Get a Book Recommendation

**Project description:** 
Turtle are with a lot of randomness resulting in a dizzying array of turtleness.

### Program Code:

<pre style='color:#000000;background:#ffffff;'><span style='color:#800000; font-weight:bold; '>import</span> turtle
<span style='color:#800000; font-weight:bold; '>import</span> random

colors <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#0000e6; '>'blue'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'green'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'orange'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'red'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'cyan'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'purple'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'white'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'yellow'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'pink'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'light blue'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'silver'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'gold'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'darkblue'</span><span style='color:#808030; '>]</span>

<span style='color:#800000; font-weight:bold; '>def</span> random_color<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    <span style='color:#800000; font-weight:bold; '>for</span> i <span style='color:#800000; font-weight:bold; '>in</span> <span style='color:#400000; '>range</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>for</span> color <span style='color:#800000; font-weight:bold; '>in</span> random<span style='color:#808030; '>.</span>sample<span style='color:#808030; '>(</span>colors<span style='color:#808030; '>,</span> <span style='color:#400000; '>len</span><span style='color:#808030; '>(</span>colors<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
            x <span style='color:#808030; '>=</span> color
            <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span>x<span style='color:#808030; '>)</span>
            <span style='color:#800000; font-weight:bold; '>return</span> x

wn <span style='color:#808030; '>=</span> turtle<span style='color:#808030; '>.</span>Screen<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>      <span style='color:#696969; '># creates a graphics window</span>
wn<span style='color:#808030; '>.</span>bgcolor<span style='color:#808030; '>(</span><span style='color:#0000e6; '>"lightgreen"</span><span style='color:#808030; '>)</span>  <span style='color:#696969; '># set the window background colors</span>

arnold <span style='color:#808030; '>=</span> turtle<span style='color:#808030; '>.</span>Turtle<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>  <span style='color:#696969; '># create a turtle named arnold</span>
arnold<span style='color:#808030; '>.</span>hideturtle<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
arnold<span style='color:#808030; '>.</span>speed<span style='color:#808030; '>(</span><span style='color:#008c00; '>0</span><span style='color:#808030; '>)</span>
arnold<span style='color:#808030; '>.</span>pensize<span style='color:#808030; '>(</span><span style='color:#008c00; '>10</span><span style='color:#808030; '>)</span>
arnold<span style='color:#808030; '>.</span>penup<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>

aleena <span style='color:#808030; '>=</span> turtle<span style='color:#808030; '>.</span>Turtle<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
aleena<span style='color:#808030; '>.</span>hideturtle<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
aleena<span style='color:#808030; '>.</span>speed<span style='color:#808030; '>(</span><span style='color:#008c00; '>0</span><span style='color:#808030; '>)</span>
aleena<span style='color:#808030; '>.</span>pensize<span style='color:#808030; '>(</span><span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span>

arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>624</span><span style='color:#808030; '>)</span>         <span style='color:#696969; '># tell arnold to move forward by 150 units</span>
arnold<span style='color:#808030; '>.</span>left<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
arnold<span style='color:#808030; '>.</span>pendown<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>

aleena <span style='color:#808030; '>=</span> turtle<span style='color:#808030; '>.</span>Turtle<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
aleena<span style='color:#808030; '>.</span>hideturtle<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
aleena<span style='color:#808030; '>.</span>pensize<span style='color:#808030; '>(</span><span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span>
aleena<span style='color:#808030; '>.</span>speed<span style='color:#808030; '>(</span><span style='color:#008c00; '>0</span><span style='color:#808030; '>)</span>                 <span style='color:#696969; '># set the width of her pen</span>

gate <span style='color:#808030; '>=</span> <span style='color:#0000e6; '>'open'</span>
x <span style='color:#808030; '>=</span> <span style='color:#008c00; '>1</span>
z <span style='color:#808030; '>=</span> <span style='color:#008c00; '>0</span>
w <span style='color:#808030; '>=</span> <span style='color:#008c00; '>0</span>

<span style='color:#800000; font-weight:bold; '>for</span> i <span style='color:#800000; font-weight:bold; '>in</span> <span style='color:#400000; '>range</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>15</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>  <span style='color:#696969; '>#original = 5</span>
    y <span style='color:#808030; '>=</span> <span style='color:#008c00; '>25</span>
    arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>530</span><span style='color:#44aadd; '>/</span>x<span style='color:#808030; '>)</span>          <span style='color:#696969; '># complete the second side of a rectangle</span>
    arnold<span style='color:#808030; '>.</span>left<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> gate <span style='color:#44aadd; '>==</span><span style='color:#0000e6; '>'closed'</span><span style='color:#808030; '>:</span>
        gate <span style='color:#808030; '>=</span> <span style='color:#0000e6; '>'lap2'</span>
    <span style='color:#800000; font-weight:bold; '>if</span> gate <span style='color:#44aadd; '>==</span> <span style='color:#0000e6; '>'open'</span><span style='color:#808030; '>:</span>
        arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>1258</span><span style='color:#44aadd; '>/</span>x <span style='color:#44aadd; '>-</span> z<span style='color:#808030; '>)</span>
        gate <span style='color:#808030; '>=</span> <span style='color:#0000e6; '>'closed'</span>
    <span style='color:#800000; font-weight:bold; '>if</span> gate <span style='color:#44aadd; '>==</span><span style='color:#0000e6; '>'lap2'</span><span style='color:#808030; '>:</span>
        arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>1260</span><span style='color:#44aadd; '>/</span>x <span style='color:#44aadd; '>-</span> z<span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>left<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>1057</span><span style='color:#44aadd; '>/</span>x<span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>left<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> gate <span style='color:#44aadd; '>==</span> <span style='color:#0000e6; '>'closed'</span><span style='color:#808030; '>:</span>
        arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>1258</span><span style='color:#44aadd; '>/</span>x <span style='color:#44aadd; '>-</span> z<span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> gate <span style='color:#44aadd; '>==</span> <span style='color:#0000e6; '>'lap2'</span><span style='color:#808030; '>:</span>
        arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>1260</span><span style='color:#44aadd; '>/</span>x <span style='color:#44aadd; '>-</span> z<span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>left<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008000; '>528.5</span><span style='color:#44aadd; '>/</span>x<span style='color:#808030; '>)</span>   <span style='color:#696969; '>#528.5</span>
    arnold<span style='color:#808030; '>.</span>left<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>penup<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>forward<span style='color:#808030; '>(</span><span style='color:#008c00; '>25</span><span style='color:#44aadd; '>+</span>y<span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>pendown<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
    arnold<span style='color:#808030; '>.</span>right<span style='color:#808030; '>(</span><span style='color:#008c00; '>90</span><span style='color:#808030; '>)</span>
    y <span style='color:#808030; '>=</span> y <span style='color:#44aadd; '>+</span> <span style='color:#008c00; '>25</span>
    x <span style='color:#808030; '>=</span> x <span style='color:#44aadd; '>+</span> <span style='color:#008000; '>.05</span>
    z <span style='color:#808030; '>=</span> y <span style='color:#44aadd; '>+</span> z
    w <span style='color:#808030; '>=</span> w <span style='color:#44aadd; '>+</span> <span style='color:#008c00; '>25</span>
    arnold<span style='color:#808030; '>.</span>color<span style='color:#808030; '>(</span>random_color<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    aleena<span style='color:#808030; '>.</span>color<span style='color:#808030; '>(</span>random_color<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>for</span> i <span style='color:#800000; font-weight:bold; '>in</span> <span style='color:#400000; '>range</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>15</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span> <span style='color:#696969; '>#original = 5</span>
      aleena<span style='color:#808030; '>.</span>circle<span style='color:#808030; '>(</span><span style='color:#008c00; '>50</span><span style='color:#44aadd; '>*</span>i<span style='color:#808030; '>)</span>
      aleena<span style='color:#808030; '>.</span>up<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
      aleena<span style='color:#808030; '>.</span>sety<span style='color:#808030; '>(</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>50</span><span style='color:#44aadd; '>*</span>i<span style='color:#808030; '>)</span><span style='color:#44aadd; '>*</span><span style='color:#808030; '>(</span><span style='color:#44aadd; '>-</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
      aleena<span style='color:#808030; '>.</span>down<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
    wn<span style='color:#808030; '>.</span>bgcolor<span style='color:#808030; '>(</span>random_color<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>

wn<span style='color:#808030; '>.</span>exitonclick<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:43:42 UTC -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
