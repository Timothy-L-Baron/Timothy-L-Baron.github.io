## Unit Converter

**Project description:** 
This program that calculates unit equivalencies such as feet to meters,
inches to centimeters, kg to pounds, grams to pounds, etc. It gives error messages for bad input. When the number is 1 is used,
singular units are displayed in the output (ex. inch instead of inches).

### Program Code:

<pre style='color:#000000;background:#ffffff;'><span style='color:#696969; '>#create a list of aceptabl eunit values</span>
unit_vals <span style='color:#808030; '>=</span> [<span style='color:#0000e6; '>'inches'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'feet'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'centimeters'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'meters'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'pounds'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'grams'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'kilograms'</span>]

<span style='color:#696969; '>#create a dictionary of unit conversion values</span>
unit_dic <span style='color:#808030; '>=</span> {<span style='color:#0000e6; '>'inches_to_centimeters'</span> : <span style='color:#008c00; '>2</span>.<span style='color:#008c00; '>54</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'centimeters_to_inches'</span> : <span style='color:#008c00; '>1</span>/<span style='color:#008c00; '>2</span>.<span style='color:#008c00; '>54</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'feet_to_inches'</span> : <span style='color:#008c00; '>12</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'inches_to_feet'</span> : <span style='color:#008c00; '>1</span>/<span style='color:#008c00; '>12</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'meters_to_inches'</span> : <span style='color:#008c00; '>39</span>.<span style='color:#008c00; '>9071</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'inches_to_meters'</span> : <span style='color:#008c00; '>1</span>/<span style='color:#008c00; '>39</span>.<span style='color:#008c00; '>9071</span><span style='color:#808030; '>,</span>
<span style='color:#0000e6; '>'feet_to_centimeters'</span> : 30.48<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'centimeters_to_feet'</span> : 1/30.48<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'meters_to_centimeters'</span> : 100<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'centimeters_to_meters'</span> : 1/100<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'meters_to_feet'</span> : 3.28084<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'feet_to_meters'</span> : 1/3.28084<span style='color:#808030; '>,</span>
<span style='color:#0000e6; '>'pounds_to_grams'</span> : 453.592<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'grams_to_pounds'</span> : 1/453.592<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'kilograms_to_pounds'</span> : 2.20462<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'pounds_to_kilograms'</span> : 1/2.20462<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'kilograms_to_grams'</span> : 1000<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'gram_to_kilograms'</span> : 1/1000<span style='color:#808030; '>,</span>
<span style='color:#0000e6; '>'feet_to_feet'</span> : 1<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'inches_to_inches'</span> : 1<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'centimeters_to_centimeters'</span> : 1<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'meters_to_meters'</span> : 1<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'pound_to_pound'</span> : 1<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'grams_to_grams'</span> : 1<span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'kilograms_to_kilograms'</span> : 1}

<span style='color:#696969; '>#create dictionary of single unit values</span>
single_unit_dic <span style='color:#808030; '>=</span> {<span style='color:#0000e6; '>'inches'</span> : <span style='color:#0000e6; '>'inch'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'feet'</span> : <span style='color:#0000e6; '>'foot'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'centimeters'</span> : <span style='color:#0000e6; '>'centimeter'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'meters'</span> : <span style='color:#0000e6; '>'meter'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'pounds'</span> : <span style='color:#0000e6; '>'pound'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'grams'</span> : <span style='color:#0000e6; '>'gram'</span><span style='color:#808030; '>,</span> <span style='color:#0000e6; '>'kilograms'</span> : <span style='color:#0000e6; '>'kilogram'</span>}

<span style='color:#696969; '>#create a function to do unit conversion that takes three parameters (n_in, u_in, u_out)</span>
def unit_converter(n_in<span style='color:#808030; '>,</span> u_in<span style='color:#808030; '>,</span> u_out):
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;#convert n_in to a float</span>
    n_in <span style='color:#808030; '>=</span> float(n_in)
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;#create an input phrase so that the proper conversion value can be obtained from the unit_dic</span>
    input_phrase <span style='color:#808030; '>=</span> u_in + <span style='color:#0000e6; '>'_to_'</span> + u_out
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;#calculate fin_out using the input number and conversion value</span>
    fin_out <span style='color:#808030; '>=</span> n_in * unit_dic.get(input_phrase)
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;#change units to singular string for output if number in front of unit is 1</span>
    if n_in <span style='color:#808030; '>=</span>= <span style='color:#008c00; '>1</span>.<span style='color:#008c00; '>0</span>:
        u_in <span style='color:#808030; '>=</span> single_unit_dic.get(u_in)
    if fin_out <span style='color:#808030; '>=</span>= <span style='color:#008c00; '>1</span>.<span style='color:#008c00; '>0</span>:
        u_out <span style='color:#808030; '>=</span> single_unit_dic.get(u_out)
<span style='color:#696969; '>&#xa0;&#xa0;&#xa0;&#xa0;#return the conversion</span>
    return print(<span style='color:#0000e6; '>'{} {} is approximately {} {}'</span>.format(n_in<span style='color:#808030; '>,</span> u_in<span style='color:#808030; '>,</span> fin_out<span style='color:#808030; '>,</span> u_out))

<span style='color:#696969; '>#prompt the user for user_input - a number, original unit(s) and outputs, give error message for bad inputs and re-prompt, make sure the same unit type can't be entered for unit_in and unit_out</span>
<span style='color:#696969; '>#prompt for the number of starting units, return an error if it is not a number</span>
num_in <span style='color:#808030; '>=</span> input(<span style='color:#0000e6; '>'This program handles the following units: inches, feet, centimeters, meters, pounds, grams, and kilograms)\nPlease enter the NUMBER of units for the unit you are converting from:\n'</span>)
while True:
    try:
        num_in <span style='color:#808030; '>=</span> float(num_in)
        <span style='color:#800000; font-weight:bold; '>break</span>
    except ValueError:
        num_in <span style='color:#808030; '>=</span> input(<span style='color:#0000e6; '>'You must input a NUMBER:'</span>)

<span style='color:#696969; '>#prompt for the unit type the user wants to convert from. If it is not a valid unit, re-prompt</span>
unit_in <span style='color:#808030; '>=</span> input(<span style='color:#0000e6; '>'Please input the UNIT TYPE that you want to convert FROM:\n'</span>).lower()
while unit_in not <span style='color:#800000; font-weight:bold; '>in</span> unit_vals:
    unit_in <span style='color:#808030; '>=</span> input(<span style='color:#0000e6; '>"Please choose a valid unit ---\n(inches, feet, centimeters, meters, pounds, grams, kilograms)\nunit:"</span>).lower()

<span style='color:#696969; '>#prompt for the uit type the user wants to convert to. If it is not a valid unit or the same unit as the unit_in, re-prompt the user</span>
unit_out <span style='color:#808030; '>=</span> input(<span style='color:#0000e6; '>'Please input the UNIT TYPE you want to convert TO:'</span>).lower()
while unit_out not <span style='color:#800000; font-weight:bold; '>in</span> unit_vals:
        unit_out <span style='color:#808030; '>=</span> input(<span style='color:#0000e6; '>"Please choose a valid unit ---\n(inches, feet, centimeters, meters, pounds, grams, kilograms)\nunit:"</span>).lower()
        


<span style='color:#696969; '>#call the function</span>
unit_converter(num_in<span style='color:#808030; '>,</span> unit_in<span style='color:#808030; '>,</span> unit_out)
</pre>
<!--Created using ToHtml.com on 2020-01-12 17:27:26 UTC -->

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
