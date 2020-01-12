## Word Guessing Game

**Project description:** 
An original word guessing game created without using resources specifically regarding how to make guess word games.

### Program Code:

<pre style='color:#000000;background:#ffffff;'><span style='color:#696969; '>#import module</span>
<span style='color:#800000; font-weight:bold; '>import</span> random

<span style='color:#696969; '>#create a list of words to guessing</span>
words <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#0000e6; '>'ketchup'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'mustard'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'green'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'yellow'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'cordial'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'spaniel'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'worker'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'information'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'jasper'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'science'</span><span style='color:#808030; '>]</span>

<span style='color:#696969; '>#create a list for wrong guess letters</span>
guessed_letters <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#808030; '>]</span>

<span style='color:#696969; '>#create a function to choose a random word from the 'words' list and turn it into a series of blanks (a blank for each letter)</span>
<span style='color:#800000; font-weight:bold; '>def</span> create_guess_word<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    guess_word <span style='color:#808030; '>=</span> random<span style='color:#808030; '>.</span>choice<span style='color:#808030; '>(</span>words<span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span>guess_word<span style='color:#808030; '>)</span>
    x <span style='color:#808030; '>=</span> guess_word
    <span style='color:#800000; font-weight:bold; '>return</span> x

<span style='color:#696969; '>#create a function to turn the guess_word into spaces so the user sees a blank word to start</span>
<span style='color:#800000; font-weight:bold; '>def</span> create_spaced_word<span style='color:#808030; '>(</span>guess_word<span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    count <span style='color:#808030; '>=</span> <span style='color:#008c00; '>0</span>
    <span style='color:#800000; font-weight:bold; '>for</span> letter <span style='color:#800000; font-weight:bold; '>in</span> guess_word<span style='color:#808030; '>:</span>
        count <span style='color:#808030; '>=</span> count <span style='color:#44aadd; '>+</span> <span style='color:#008c00; '>1</span>
        spaced_word <span style='color:#808030; '>=</span> <span style='color:#808030; '>(</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'_'</span><span style='color:#808030; '>)</span> <span style='color:#44aadd; '>*</span> count<span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span>spaced_word<span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>return</span> spaced_word

<span style='color:#696969; '># create a function to prompt user for a guess a letter</span>
<span style='color:#800000; font-weight:bold; '>def</span> prompt_user_guess<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    guess_letter <span style='color:#808030; '>=</span> <span style='color:#400000; '>input</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>"Please guess a letter: "</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>lower<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
    <span style='color:#800000; font-weight:bold; '>return</span> guess_letter

<span style='color:#696969; '># create a function that determines the indices for all places the guess_letter appears in the guess word, convert the guess_word string into a list, use the indices</span>
<span style='color:#696969; '>#to replace correectly guessed letters with those letters in the list [instead of the blanks], change it back into a string, and print out the results to the user</span>
<span style='color:#696969; '>#if a wrong letter is guessed, return a list of wrong guesses and re-prompt the user</span>
<span style='color:#696969; '>#when the word is fully guessed, stop the program and tell the user he/she won</span>
<span style='color:#800000; font-weight:bold; '>def</span> guess_letter_in_guess_word<span style='color:#808030; '>(</span>guess_word<span style='color:#808030; '>,</span> guess_letter<span style='color:#808030; '>,</span> spaced_word<span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    <span style='color:#800000; font-weight:bold; '>while</span> <span style='color:#074726; '>True</span><span style='color:#808030; '>:</span>
        <span style='color:#800000; font-weight:bold; '>if</span> guess_letter <span style='color:#800000; font-weight:bold; '>in</span> guess_word<span style='color:#808030; '>:</span>
            index_finder <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span>n <span style='color:#800000; font-weight:bold; '>for</span> n <span style='color:#800000; font-weight:bold; '>in</span> <span style='color:#400000; '>range</span><span style='color:#808030; '>(</span><span style='color:#400000; '>len</span><span style='color:#808030; '>(</span>guess_word<span style='color:#808030; '>)</span><span style='color:#808030; '>)</span> <span style='color:#800000; font-weight:bold; '>if</span> guess_word<span style='color:#808030; '>.</span>find<span style='color:#808030; '>(</span>guess_letter<span style='color:#808030; '>,</span> n<span style='color:#808030; '>)</span> <span style='color:#44aadd; '>==</span> n<span style='color:#808030; '>]</span>
            <span style='color:#800000; font-weight:bold; '>for</span> index <span style='color:#800000; font-weight:bold; '>in</span> index_finder<span style='color:#808030; '>:</span>
                list_convert <span style='color:#808030; '>=</span> <span style='color:#400000; '>list</span><span style='color:#808030; '>(</span>spaced_word<span style='color:#808030; '>)</span>
                list_convert<span style='color:#808030; '>[</span>index<span style='color:#808030; '>]</span> <span style='color:#808030; '>=</span> guess_letter
                spaced_word <span style='color:#808030; '>=</span> <span style='color:#0000e6; '>""</span><span style='color:#808030; '>.</span>join<span style='color:#808030; '>(</span>list_convert<span style='color:#808030; '>)</span>
            <span style='color:#800000; font-weight:bold; '>if</span> spaced_word <span style='color:#44aadd; '>==</span> guess_word<span style='color:#808030; '>:</span>
                <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'You guessed it. You WIN!!!'</span><span style='color:#808030; '>)</span>
                <span style='color:#074726; '>False</span>
                <span style='color:#800000; font-weight:bold; '>break</span>
            <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span>spaced_word<span style='color:#808030; '>)</span>
        <span style='color:#800000; font-weight:bold; '>if</span> guess_letter <span style='color:#800000; font-weight:bold; '>not</span> <span style='color:#800000; font-weight:bold; '>in</span> guess_word<span style='color:#808030; '>:</span>
            guessed_letters<span style='color:#808030; '>.</span>append<span style='color:#808030; '>(</span>guess_letter<span style='color:#808030; '>)</span>
            <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'That letter is not in the word!'</span><span style='color:#808030; '>)</span>
            <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'Your wrong guesses so far: '</span><span style='color:#808030; '>)</span>
            <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span>guessed_letters<span style='color:#808030; '>)</span>
            guess_letter <span style='color:#808030; '>=</span> <span style='color:#400000; '>input</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>"Please guess a letter: "</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>lower<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
        <span style='color:#800000; font-weight:bold; '>else</span><span style='color:#808030; '>:</span>
            guess_letter <span style='color:#808030; '>=</span> <span style='color:#400000; '>input</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>"Please guess a letter: "</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>lower<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>


<span style='color:#696969; '># use functions and nesting to call the main function</span>
get_word <span style='color:#808030; '>=</span> create_guess_word<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
space <span style='color:#808030; '>=</span> create_spaced_word<span style='color:#808030; '>(</span>get_word<span style='color:#808030; '>)</span>
get_guess <span style='color:#808030; '>=</span> prompt_user_guess<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
guess_letter_in_guess_word<span style='color:#808030; '>(</span>get_word<span style='color:#808030; '>,</span> get_guess<span style='color:#808030; '>,</span> space<span style='color:#808030; '>)</span>
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:39:08 UTC -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
