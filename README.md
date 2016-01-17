## stellar is a LESS library for easy and fast webapp scaffolding.

**It is good at:**

* vertical align;
* and..centering things;
* arranging in rows (for wide screens) and columns (for small screens);
and of course
* responsive design with just a few lines of code.

**And easy because:**

there is a **parent** (element) and it has **children** (elements)..and the parent says how his children are arranged in terms of x-axis and y-axis.



### How to use:


*First, let's see what the parent can do to children.*


Use ``.row();`` or ``.column();`` on a parent element to arrange its children in a row or a column.

Inside the brackets you can use ``@x:`` and ``@y:`` to specify how the children are positioned on the corresponding axis. 

Use ``@left;``, ``@center;``, ``@right;`` or ``@spread;`` for x-axis positioning.
Use ``@top;``, ``@center;``, ``@bottom;`` or ``@spread;`` for y-axis positioning.


**Default values:**

		.row(@x: @left; @y: @top;);
		.column(@x: @left; @y: @top);
		

If using a default value, the property and its corresponding value can be skipped. 

**Sample:**

Тhis: ``.row(@x: center; @y: @top);`` is the same like ``.row(@x: center;);``.


*And now, what children can do despite their parent's say.*


A child can get a different positioning than the rest of the children.

Use ``.odd(row; @y: value;);`` when the children are arranged in a ``.row;``.
(values ``@top``, ``@center``, ``@bottom``).

Use ``.odd(column; @x: value;);`` when the children are arranged in a ``.column;``.
(values: ``@left``, ``@center``, ``@right``).


**Default values:**

		.odd(row; @y: @top;);
		.odd(column; @x: @left;);



## Sample


**HTML code**

	<div class="container">
		<div class="child"></div>
		<div class="child"></div>
		<div class="child naughty"></div>
		<div class="child"></div>
	</div>


**LESS code**

	.container {
		.row(@x: @center; @y: @top);
		height: 100vh;
		width: 960px;
		.child {
			height: 100px;
			margin: 20px;
			width: 100px;
		}	
		.naughty {
			.odd(row; @y: @center;);
		}
	}



## Install


$ bower install stellar-less

in your .less file:

@import "bower_components/stellar/stellar";



## Browser support





## More samples


For more complex samples in an interactive playground, please visit [http://stellar.stelavit.com](http://www.stellar.stelavit.com/).
