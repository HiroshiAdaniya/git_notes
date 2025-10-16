<h1># Div in HTML</h1>

<p>The Div element in HTML is a block element which helps group other elements together. A block element takes up an entire line on a page. Here is a basic syntax of a div element</p>

	* HTML code:

	<div>
	  code goes here
	</div>

<p>Although a div is a block element, we can actual change it's default property into an inline-block element using a CSS code called "display". An inline-block element only takes up the space that is specified.</p>

	* CSS code:

	div {				---> No class was given so all divs will be affected
	  display: inline-block;	---> This changes the div/divs to inline-block elements. 
	}

<h2># Nested Div</h2>

<p>The main advantage of the div element is that they can be nested which can help create columns and rows on your web page. This can further divide and group your code into sections which can be styled independently from the rest of the code in the main div element.</p>

	* HTML code:

	<div class="main-div">		---> This is the main div that groups all the elements within in
	  <div class="nested-div-1">	---> A nested div
	    code goes here
	  </div>
	  <div class="nested-div-2">	---> Another nested div
	    <div class="nested-div-2-a">  ---> Nested within a nested div
	      code goes here
	    </div>
	  </div>
	</div>

<p>In the CSS file these divs can be styled either individually or all together. In the example above i have given them each a class to better explain how they are nested.</p>
