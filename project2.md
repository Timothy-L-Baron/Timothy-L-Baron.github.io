## Choose a Genre - Get a Book Recommendation

**Project description:** 
This program takes user input (asking for book genre) and returns a book suggestion (title and author). The data
used for book selection is stored in a spreadsheet called book_data.csv. The program case insensitive to user input.
and returns an error message if they do not pick one of the available genres.

### Program Code:

<pre style='color:#000000;background:#ffffff;'><span style='color:#696969; '>#import module</span>
<span style='color:#800000; font-weight:bold; '>import</span> string

<span style='color:#696969; '>#create a list of valid genres</span>
genres <span style='color:#808030; '>=</span> <span style='color:#808030; '>[</span><span style='color:#0000e6; '>'horror'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'mystery'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'classics'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'fantasy'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'science fiction'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'romance'</span><span style='color:#808030; '>,</span><span style='color:#0000e6; '>'plays'</span><span style='color:#808030; '>]</span>

<span style='color:#696969; '>#open up the .csv file for reading</span>
open_file <span style='color:#808030; '>=</span> <span style='color:#400000; '>open</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'book_data.csv'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'r'</span><span style='color:#808030; '>)</span>

<span style='color:#696969; '>#get a list of strings, each of which is a single line[row] of the spreadsheet</span>
get_lines <span style='color:#808030; '>=</span> open_file<span style='color:#808030; '>.</span>readlines<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>

<span style='color:#696969; '># get user input to obtain which genre they would like and make case insensitive</span>
user_input <span style='color:#808030; '>=</span> <span style='color:#400000; '>input</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>"Please choose a genre (Classics, Fantasy, Horror, Mystery, Plays, Romance, or Science Fiction) </span><span style='color:#0f69ff; '>\n</span><span style='color:#0000e6; '>to receive a book suggestion:"</span><span style='color:#808030; '>)</span>

<span style='color:#696969; '>#write a function that will search the spreadsheet and match up the user input genre with an author and title from the ss and print this out as a suggestion</span>
<span style='color:#800000; font-weight:bold; '>def</span> get_book_title<span style='color:#808030; '>(</span><span style='color:#400000; '>str</span><span style='color:#808030; '>,</span>u_in<span style='color:#808030; '>)</span><span style='color:#808030; '>:</span>
    <span style='color:#696969; '>#loop through each line [row] of the ss, each line is currently a string of title, author, genre</span>
    <span style='color:#800000; font-weight:bold; '>for</span> line <span style='color:#800000; font-weight:bold; '>in</span> get_lines<span style='color:#808030; '>[</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>:</span><span style='color:#808030; '>]</span><span style='color:#808030; '>:</span>
        <span style='color:#696969; '>#make everything in the line [row] of the ss lowercase, so that user input is case insensitive</span>
        line <span style='color:#808030; '>=</span> line<span style='color:#808030; '>.</span>lower<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
        <span style='color:#696969; '>#strip any \n's from the line</span>
        line <span style='color:#808030; '>=</span> line<span style='color:#808030; '>.</span>strip<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>
        <span style='color:#696969; '>#change the string into a list of strings where the 3 elements are title, author, genre</span>
        new_lst <span style='color:#808030; '>=</span> line<span style='color:#808030; '>.</span>split<span style='color:#808030; '>(</span><span style='color:#0000e6; '>','</span><span style='color:#808030; '>)</span>
        <span style='color:#800000; font-weight:bold; '>if</span> u_in <span style='color:#800000; font-weight:bold; '>in</span> new_lst<span style='color:#808030; '>:</span>
            <span style='color:#696969; '>#x = print('You should check out "{}" by {}.'.format(string.capwords(new_lst[0], sep = None), string.capwords(new_lst[1], sep = None)))</span>
            <span style='color:#800000; font-weight:bold; '>break</span>
    <span style='color:#800000; font-weight:bold; '>return</span> <span style='color:#800000; font-weight:bold; '>print</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>'You should check out "{}" by {}.'</span><span style='color:#808030; '>.</span>format<span style='color:#808030; '>(</span>string<span style='color:#808030; '>.</span>capwords<span style='color:#808030; '>(</span>new_lst<span style='color:#808030; '>[</span><span style='color:#008c00; '>0</span><span style='color:#808030; '>]</span><span style='color:#808030; '>,</span> sep <span style='color:#808030; '>=</span> <span style='color:#074726; '>None</span><span style='color:#808030; '>)</span><span style='color:#808030; '>,</span> string<span style='color:#808030; '>.</span>capwords<span style='color:#808030; '>(</span>new_lst<span style='color:#808030; '>[</span><span style='color:#008c00; '>1</span><span style='color:#808030; '>]</span><span style='color:#808030; '>,</span> sep <span style='color:#808030; '>=</span> <span style='color:#074726; '>None</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>

<span style='color:#696969; '>#if the user input is not a valid genre, prompt them again</span>
<span style='color:#800000; font-weight:bold; '>while</span> user_input <span style='color:#800000; font-weight:bold; '>not</span> <span style='color:#800000; font-weight:bold; '>in</span> genres<span style='color:#808030; '>:</span>
    user_input <span style='color:#808030; '>=</span> <span style='color:#400000; '>input</span><span style='color:#808030; '>(</span><span style='color:#0000e6; '>"Please choose a valid genre ---</span><span style='color:#0f69ff; '>\n</span><span style='color:#0000e6; '>(Classics, Fantasy, Horror, Mystery, Plays, Romance, or Science Fiction)</span><span style='color:#0f69ff; '>\n</span><span style='color:#0000e6; '>genre:"</span><span style='color:#808030; '>)</span><span style='color:#808030; '>.</span>lower<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span>

get_book_title<span style='color:#808030; '>(</span>get_lines<span style='color:#808030; '>,</span> user_input<span style='color:#808030; '>.</span>lower<span style='color:#808030; '>(</span><span style='color:#808030; '>)</span><span style='color:#808030; '>)</span>
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:34:38 UTC -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
