# complete

Simple IPython dict keys autocompleter

###Installation

Just copy `comp.ipy` file wherever you want to.

###Dependency

- Python 2 or 3 (tested with 2.7 and 3.4)
- IPython 3.0.0

###Usage

#####Briefly:

$ `ipython`

In [1]: `%run comp.ipy`

In [2]: `compl(locals())`

Then just type variable name (dict), [' (bracket and apostrophe), press tab and have fun :)

#####Step-by-step guide (tl;dr):

$ `ipython`

In [1]: `%run comp.ipy`

In [2]: `compl(locals())`

In [3]: `my_magnificent_dict = {'a': 1, 'bc': {'x': 0, 'y': ['t']}}`

In [4]: `my_magnificent_dict['` < TAB-key > *# we have to type [' (bracket and apostrophe)* and then we press TAB key

`a bc` *# we can see available keys*

In [4]: `my_magnificent_dict['a` < TAB-key > *# so we type a and press TAB*

In [4]: `my_magnificent_dict['a'` < TAB-key >

In [4]: `my_magnificent_dict['a']` < TAB-key > *# and auto-completer closes apostrophe and bracket*

In [4]: `my_magnificent_dict['a']` < TAB-key > *# completer says there is no deeper dict*

`Scalar value: 1` *# just scalar value - no further completion needed*

In [4]: `my_magnificent_dict['a']` < ALT + Backspace-key > *alt with backspace clears one word left*

In [4]: `my_magnificent_dict['` < TAB-key > *# completion once again*

`a bc` *# we can see available keys*

In [4]: `my_magnificent_dict['` < TAB-key > *# completion once again*

`a b` *# we can see available keys*

In [4]: `my_magnificent_dict['b` < TAB-key > *# now we type b and press TAB*

In [4]: `my_magnificent_dict['bc'` *# auto-completer adds c and '*

In [4]: `my_magnificent_dict['bc'` < TAB-key > *# TAB again*

In [4]: `my_magnificent_dict['bc']` *# and bracked closed*

In [4]: `my_magnificent_dict['bc']` < TAB-key > *# we inspect what is under 'bc' key*

In [4]: `my_magnificent_dict['bc']['` < TAB-key >  *# TAB again*

`x y` *# and further keys appear*

In [4]: `my_magnificent_dict['bc']['y` < TAB-key > < TAB-key > *# we choose one of them and press TAB twice*

In [4]: `my_magnificent_dict['bc']['y']` *# and everything works as expected*

In [4]: `my_magnificent_dict['bc']['y']` < TAB-key >  *# TAB once again*

`Value <class 'list'>`  *# and we see there is a list*

Simple, isn't it ? :)

###Key features

- Completion for lines starting not from variable name (eg. `new_dict = my_magnificent_dict['` < TAB-key >)
- Auto-closing brackets and apostrophes
- Brackets and apostrophes auto-suggest once dict found
- Colorized scalar value printing once found
- Colorized value type printing for non-scalars other than dict
- Suppressing junk completion default for IPython (for empty dicts either)
- Python 2 and 3 version support

###License

BSD / License
