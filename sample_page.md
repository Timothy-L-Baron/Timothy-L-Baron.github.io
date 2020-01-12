## Consonant and Vowel Counter

**Project description:** 
An original program that will take as input somebody's name and output the number of vowels and consonants. It will also output 
a magic word created by randomly shuffling the letters of the person's name

### Program Code:

<pre style='color:#000000;background:#ffffff;'><span style='color:#800000; font-weight:bold; '>import</span> random

<span style='color:#696969; '>#Need lists of vowels and consonants</span>
vows <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#0000e6; '>'a'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'e'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'i'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'o'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'u'</span><span style='color:#808030; '>]</span>
cons <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#0000e6; '>'b'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'c'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'d'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'f'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'g'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'h'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'j'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'k'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'l'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'m'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'n'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'p'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'q'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'r'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'s'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'t'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'v'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'w'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'x'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'y'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'z'</span><span style='color:#808030; '>]</span>

<span style='color:#696969; '>#prompt user for input</span>
user_input <span style='color:#808030; '>=</span> <span style='color:#400000; '>input</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>"please input your name:"</span><span style='color:#808030; '>)</span>

<span style='color:#696969; '># function that counts the numer of vowels and consonants</span>
<span style='color:#800000; font-weight:bold; '>def</span> cons_vow_counter<span style='color:#808030; '>(</span><span style='color:#400000; '>str</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    count_c <span style='color:#808030; '>=</span> <span style='color:#008c00; '>0</span>
    count_v <span style='color:#808030; '>=</span> <span style='color:#008c00; '>0</span>
    magic_letters_lst <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#808030; '>]</span>
    <span style='color:#800000; font-weight:bold; '>for</span> letter <span style='color:#800000; font-weight:bold; '>in</span> <span style='color:#400000; '>str</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>if</span> letter <span style='color:#800000; font-weight:bold; '>in</span> vows<span style='color:#808030; '>:</span>
            count_v <span style='color:#808030; '>=</span> count_v <span style='color:#44aadd; '>+</span> <span style='color:#008c00; '>1</span>
            magic_letters_lst<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>letter<span style='color:#808030; '>)</span>
        <span style='color:#800000; font-weight:bold; '>if</span> letter <span style='color:#800000; font-weight:bold; '>in</span> cons<span style='color:#808030; '>:</span>
            count_c <span style='color:#808030; '>=</span> count_c <span style='color:#44aadd; '>+</span> <span style='color:#008c00; '>1</span>
            magic_letters_lst<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>letter<span style='color:#808030; '>)</span>
    random<span style='color:#808030; '>.</span>shuffle<span style='color:#808030; '>(</span>magic_letters_lst<span style='color:#808030; '>)</span>
    magic_letters <span style='color:#808030; '>=</span> <span style='color:#0000e6; '>""</span>
    <span style='color:#800000; font-weight:bold; '>for</span> letter <span style='color:#800000; font-weight:bold; '>in</span> magic_letters_lst<span style='color:#808030; '>:</span>
        magic_letters <span style='color:#808030; '>=</span> magic_letters <span style='color:#44aadd; '>+</span> letter
    <span style='color:#800000; font-weight:bold; '>return</span> <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'Your name has {} consonant(s) and {} vowel(s). </span><span style='color:#0f69ff; '>\n</span><span style='color:#0000e6; '>Your name forms the magic word: {}'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>count_c<span style='color:#808030; '>,</span> count_v<span style='color:#808030; '>,</span> magic_letters<span style='color:#808030; '>.</span>upper<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>


cons_vow_counter<span style='color:#808030; '>(</span>user_input<span style='color:#808030; '>)</span>
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:09:47 UTC -->


cons_vow_counter<span style='color:#808030; '>(</span>user_input<span style='color:#808030; '>)</span>
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:05:05 UTC -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
