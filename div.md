<h1># Div in HTML</h1>

<p>The Div element in HTML is a block element which helps group other elements together. A block element takes up an entire line on a page. Here is a basic syntax of a div element</p>

	*html code:

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

	* CSS code:

	.main-div,
	.nested-div-1,
	.nested-div-2 {
	 display: inline-block;
	}

	.main-div {
	  width: 300px;
	}

	.nested-div-1,
	.nested-div-2 {
	  width: 100px;
	}


<p>In your CSS file these divs can be styled either individually or all together. In the example above i have given each a class to better explain how they are nested.</p>

<h2># CSS grid</h2>

<p>The CSS grid is a more efficient and practical way of creating rows and columns in your html file. While individually sizing each div with CSS code, you'll most likely run into spacing and margin inconsistencies within your design. The best way to create well organized, symmetrical and evenly spaced elements is by using the CSS grid method.</p>

	* HTML Code:

	<div style="
	display: grid;
	grid-template-columns: 100px 100px;">

		<div style="background-color: rgb(90, 90, 202)">
		  Div 1
		</div> 
		<div style="background-color: rgb(172, 100, 100)">
		  Div 2
		</div>

	</div>

<p>In the example above we have created "1 row" and "2 columns" and have used the "style" attribute to add CSS styling code within our HTML code. This is generally not recommend as it makes the code much more difficult to read. Let's breakdown the example:</p>

	<div style="	---> The style attribute
	display: grid;	---> We have used the CSS styling "display"
	grid-template-columns: 100px 100px;"> ---> We have added a grid template
					      ---> "100xp" this is the size of the column, for each size counts as one column
	...
	</div>

<p>Here we have used the "display" CSS code to implement the grid template and have passed the size of each column to it.</p>

	<div style="background-color: rgb(90, 90, 202)"> ---> we have added a background color to the div
 	  Div 1		---> Text that will appear in the div
	</div>

<p>In this portion of the code we have stylised the background of the div and have added text to it. In the main div we added the grid template and the size and number of columns that will appear in a row, the nested div are those divs. If we add more nested divs than there are arguments to the grid template, the rest will wrap around and appear on a new line.

So if we have specified 2 columns of 100px but have nested 4 divs into the main div, it will result in having 2 columns but instead of 1 row we will have 2 rows because of the overflow.</p>

<h2># Free remaining space (fr)</h2>

<p>"fr" or "free remaining space" is an argument that is passed when specifying the size of a column in the "grid-template-columns" function. What this does is that it will take cum an free remaining space on the line that has not been given a size. So if we wanted 3 columns but have only specified sizes for two of them, "fr" can be used to create another column that will take up the rest of the space. 

For example, if we have set the first column to 100px and the second to 50px but our row is 250px in width, fr will take up the rest of the 100px.</p>

	* HTML code:

	<div style="
	  display: grid;
	  grid-template-columns: 100px, 50px, 1fr;">
	  ...
	 </div>

<p>You can use "fr" as many times as you'd like. There is also an option to take up double the free space when using "fr". We set one column size, then used "fr" but want another column to take up double the space of the first "fr", we just add the number two in front of it</p>

	* HTML code:

	<div style="
	  display: grid;
	  grid-template-columns: 100px, 1fr, 2fr;">
	  ...
	 </div>

<h2># Column and row gaps</h2>

<p>When creating the display grid you'll notice that there are no natural space between the rows and columns. In order to create the spaces between them you will need to use the "column-gap" and "row-gap" attribute.</p>

	* CSS code

	.class {
	   display: grid;
	   grid-template-columns: 1fr 1fr 1fr;
	   column-gap: 3px;	---> creates spaces between the columns
	   row-gap: 6px;	---> creates spaces between the rows
	}
#end
