## This can be your internal website page / project page

**Project description:** Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

### 1. Suggest hypotheses about the causes of observed phenomena

<pre style='color:#000000;background:#ffffff;'><span style='color:#696969; '>"""Make a random number generator for D&amp;D statistics that generates 4d6 'take the best 3' results"""</span>
<span style='color:#800000; font-weight:bold; '>import</span> random
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
<!--Created using ToHtml.com on 2020-01-10 23:52:54 UTC -->

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

```javascript
if (isAwesome){
  return true
}
```

### 2. Assess assumptions on which statistical inference will be based

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Provide a basis for further data collection through surveys or experiments

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. 

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
