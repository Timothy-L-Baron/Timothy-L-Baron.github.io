## Roll 4d6 - Take Best 3 - Repeat 6 Times

**Project description:** 
Make a random number generator that generates 4d6 'take the best 3' results and repeats 6 times

### Program Code:

<pre style='color:#000000;background:#ffffff;'><span style='color:#800000; font-weight:bold; '>import</span> random
count <span style='color:#808030; '>=</span> <span style='color:#008c00; '>0</span>

<span style='color:#696969; '>#function to find the minimum roll</span>
<span style='color:#800000; font-weight:bold; '>def</span> find_min<span style='color:#808030; '>(</span>v1<span style='color:#808030; '>,</span> v2<span style='color:#808030; '>,</span> v3<span style='color:#808030; '>,</span> v4<span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    scores <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#808030; '>]</span>
    scores<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>v1<span style='color:#808030; '>)</span>
    scores<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>v2<span style='color:#808030; '>)</span>
    scores<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>v3<span style='color:#808030; '>)</span>
    scores<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>v4<span style='color:#808030; '>)</span>
    min_roll <span style='color:#808030; '>=</span> <span style='color:#400000; '>min</span><span style='color:#808030; '>(</span>scores<span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>return</span> min_roll

<span style='color:#800000; font-weight:bold; '>for</span> score <span style='color:#800000; font-weight:bold; '>in</span> <span style='color:#400000; '>range</span><span style='color:#808030; '>(</span><span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    value1 <span style='color:#808030; '>=</span> random<span style='color:#808030; '>.</span>randint<span style='color:#808030; '>(</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>,</span> <span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span>
    value2 <span style='color:#808030; '>=</span> random<span style='color:#808030; '>.</span>randint<span style='color:#808030; '>(</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>,</span> <span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span>
    value3 <span style='color:#808030; '>=</span> random<span style='color:#808030; '>.</span>randint<span style='color:#808030; '>(</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>,</span> <span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span>
    value4 <span style='color:#808030; '>=</span> random<span style='color:#808030; '>.</span>randint<span style='color:#808030; '>(</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>,</span> <span style='color:#008c00; '>6</span><span style='color:#808030; '>)</span>
    min_roll <span style='color:#808030; '>=</span> find_min<span style='color:#808030; '>(</span>value1<span style='color:#808030; '>,</span> value2<span style='color:#808030; '>,</span> value3<span style='color:#808030; '>,</span> value4<span style='color:#808030; '>)</span>
    roll_total <span style='color:#808030; '>=</span> value1 <span style='color:#44aadd; '>+</span> value2 <span style='color:#44aadd; '>+</span> value3 <span style='color:#44aadd; '>+</span> value4 <span style='color:#44aadd; '>-</span> min_roll
    <span style='color:#800000; font-weight:bold; '>if</span> count <span style='color:#44aadd; '>==</span> <span style='color:#008c00; '>0</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'S: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>roll_total<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> count <span style='color:#44aadd; '>==</span> <span style='color:#008c00; '>1</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'D: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>roll_total<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> count <span style='color:#44aadd; '>==</span> <span style='color:#008c00; '>2</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'C: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>roll_total<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> count <span style='color:#44aadd; '>==</span> <span style='color:#008c00; '>3</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'I: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>roll_total<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> count <span style='color:#44aadd; '>==</span> <span style='color:#008c00; '>4</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'W: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>roll_total<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>if</span> count <span style='color:#44aadd; '>==</span> <span style='color:#008c00; '>5</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'C: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>roll_total<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
    count <span style='color:#808030; '>=</span> count <span style='color:#44aadd; '>+</span> <span style='color:#008c00; '>1</span>
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:50:02 UTC -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
