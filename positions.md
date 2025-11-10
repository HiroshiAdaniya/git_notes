<h1># Positions in CSS</h1>

<p>The position property in CSS tell an element where to sit in on the page and how it should behave in the browser when scrolling. There are 5 values that come with the Position property; fixed, static, relative, absolute and sticky.<p>

<h3>NB: It's important to note that when writing your code, the flow of the code will determine if an element is placed in front or behind another element. To combat this, you can use the "z-index" property, but we will get into that a little later</h3>
<h2># Fixed</h2>

<p>"fixed" allows you to position an element relative to the browser window and not the page. This fixes the element to the side, bottom or top of the browser window and does not move when you're scrolling the page, it remains visible.</p>

	* HTML & CSS code:

	<div style="
	background-color: green;
	position: fixed;		---> Fixes the div element to the browser window
	bottom: 20px;			---> positions it 20px to the bottom
	right: 20px;">			---> positions it 20px to the right
		Hello World!
	</div>

<p>"static" is the default setting of all elements. This means if you attempt to position it with a direction such as "top: 5px;" or "bottom: 10px", it will have no affect on the element. Since static is the default you don't need to add it to your code but I've still added an example below.</p>

	* HTML & CSS Code:
	
	<div style="
	postion: static;	---> remains static to the page (do not need to code this)
	bottom: 10px;">		---> has no affect on the element
		Hello World!
	</div>

<h2># Absolute</h2>

<p>"absolute" works similarly to "fixed" however, the key difference between the two is that the absolute property fixes the element to the page. This means, when you are scrolling the items move with the page.</p>

	*HTML & CSS code:

	<div style="
	position: absolute;"		---> Fixes the element to the page
	bottom: 20px;			---> Positions the element to the bottom
	right: 20px;>			---> Positions the element to the right

		Hello World!
	</div>

<p>"absolute" is usually used within another div that has a position of its own. When nesting an absolute element in another element the values that were given to it will then affect how it appears within the nested div. The div now becomes the page.</p>

	* HTML & CSS code:

	<div style="
	background-color: purple;
	position: fixed;		---> This will be fixed to the browser window
	left: 0px;
	right: 0px;
	top: 0px;
	hight: 50px">
		<div style"
		position: absolute;	---> position within the div
		top: 5px;		---> position 5px from the top within the div
		right: 5px;">		---> position 5px from the right within the div
			hello!!
		</div>
	</div>

<h2># Relative</h2>

<p>"relative" does not affect the div itself but rather the nest div that appears within it. So by default the element is static and is fixed to the page but when you use an absolute within it, it appears relative to the div element and not the actual page.

The previous example we used a fixed div with an absolute div nested within it. This code would allow you to scroll the page without either of the element moving and they always remain visible. However with a relative div that has a nested absolute div, they will scroll with the page but the absolute will remain relative to the element it is in and not the page itself.</p>

	* HTML & CSS code:

	<div style="
	background-color: red;
	position: relative;
	width 50px;
	hight: 50px;">
		<div style="
		position: absolute;
		right: 0px;
		top: 0px;">
			hello!
		</div>
	</div>

<h2># Negative position value</h2>

<p>When positioning an element within another element, we are limited to the borders of that element unless you use negative number. This will allow you to position it outside of the element but relative to where it is</p>

	* HTML & CSS code:

	<div style="
	position: realtive;
	width 50px;
	height: 50px;">
		<div style="
		position: absolute;
		top: -5px;			---> This lets the element apepar outside of the border of the main div
		right: 0px;">
			hello world!
	</div>
<h2># z-index</h2>

<p>"z-index" allows you to number an element which will dictate how forward or how backward an element is placed. The flow of code is important because an element that comes after another element will always appear in front of it unless coded otherwise. Generally you would give an element a index of 100 so that you can account for all other possible elements that would be used. The higher value, the more in front an element will appear and the lower index value the more behind it will be placed.

All elements have a default of zero and will appear at the back because of "position: static" so that is why its important to note where you code an element as that will determine where it will be placed, unless you use "z-index".</p>

	* HTML & CSS code:

	<div style="
	position: fixed;
	background-color: green;
	top: 0px;
	left: 0px;
	right; 0px;
	z-index: 1;">		---> this will be placed behind the next div
		hello!
	</div>

	<div syle="
	position: absolute;
	left: 10px;
	top; 0px;
	z-index: 2;">		---> This will be placed infront of the previous div

		world!
	</div>

# END
