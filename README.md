In clf->Array.py, I created a temp variable named 's' that stores all string
concatenations while the routines 'for' loop is iterated. Once the 'for' loop is
finished, I set the xml element's text to the variable 's'. Previously the element's text
attribute was successively appended to. This resulted in a massive allocaion of
memory and an ever growing slowdown.

I created a new function called xmlWrite in ProcessList.py. This function does
not prettify the document string (as it is very close to being prettified). This process was taking 10 minutes on a Mac i7
laptop. I will want to check, but I can't imagine prettified xml being
operationally critical.
