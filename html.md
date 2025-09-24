<h1># HTML, CSS and Javascript</h1>

<p>Html, css and javascript are programming languages used to develop/build websites and we applications</p>

<h2>What is the basic web architecture?</h2>

<p>The web architecture is made up of 3 essential elements:

	* Website ---> The front-end of the web application that is visible to the user
	* Serve ---> The back-end of the web application which holds and manages the data
	* IP Address ---> The address assigned to a website where it can be accessed

</p>

<h2># What is a Website?</h2>

<p>Your browser starts by loading the main HTML file, then follows it with the css file and then Javascript. This is what the user interacts with and not the backend of a web application</p>

<h2># What is a serve?</h2>

<p>This is where your website lives on and it usually lives on the cloud, to make it accessible to on the internet. The server and database contains all the data of a website and facilities users interact with.</p>

<h2># What is an IP Address?</h2>

<p>The IP Address is where your website is hosted on and is integrated with a domain name which is easily accessed by anyone with an internet connection.</p>

<h2># What is HTML?</h2>
***HyperText Markup Language***

<p>HTML is a markup language universally used for developing web pages. Its purpose is to define structure of website and formats web pages
	
	* file.html ---> These files always end in .html

</p>

<h2># What is CSS?</h2>
***design language - CSS/ Cascading Style Sheet***

<p>CSS is a design language that is used to style and design your web pages to makke it look good and presentable. It can be added to any HTML element and style it to the developers choice

	* file.css ---> the CSS file/styling sheet always ends in .css

</p>

<h2># What is Javascript?</h2>
***Interpreted Language***

<p>Javascript is an interpreted language used for web development and is used to make your web pages interactive and bringing life to the application. In essence, it animates and creates motion for your web application</p>

<h2># Basic Structure of an HTML file and its Syntax</h2>

<p>This is the basic format for structuring a web page using HTML. There are 5 essential parts to HTML document; "!DOCTYPE HTML", "html", "head", "title" and "body"</p>

	*<!DOCTYPE html>
	<html>
		<head>
			<title></title>
		</head>
		<body>

		</body>

	*</html>

<p>Here is a breakdown of what each part means, what they do and how they are used</p>

**<!DOCTYPE html>***

	* <!DOCTYPE html> ---> When collecting the data from the serve, it's an intruction to let the browser know that this document type is indeed a html file which is being served to the user.
			  ---> This should always be include at the top of the page
***<html></html>***

	* <html> ---> This includes all the html code. It contains and open and closing tag where the latter includes a '/' symbol to indicate the closing tag.
		OR
	* <html lang="eng"> ---> The first tag can also contain attrubutes which can indicate the language which the document will be used.

***<head></head>***

	* <head> ---> This part of the file contains all the information about the web page such as, properties, title, css code ...etc which will be used between the opening and closing tag of the </head>

		---> Bellow is the title tag, but you can also use a link to a stylesheet which can contain css code

***<title></title>***

	*<title>* ---> The title tag defines the title of your web page and usually appears as the browser tab name, in search engine results and browser history/ bookmarks.
		  ---> This is crucial for SEO and user experience

***<body></body>***

	*<body>* ---> This contains all the displayable content of your web page such as; images, pharagraphs, headngs, vidoes, tables, div containers and more

<h2># Useful HTML elements</h2>

<p>The syntax for each element in HTML has an opening and closing tag. It defines the start and the end of the element.</p>

	* <button>TEXT</button> ---> This creates a button in which you can link to another file

	* <p>TEXT</p> ---> Creates a pharagraph

	* <a href="https://WEBSITE.com">Text</a> ---> This is known as an anchor element that directs the user to a link/website
		href="https://WEBSITE.com"	 ---> This part of the element is called an HTML attribute, it modifies how an element should behave.
		href ---> This is the attributes name
		"https://WEBSITE.com" ---> And this is the attributes value
	* <a href="..." target="_blank">TEXT</a> ---> In this example we have added another attribute called target, and this allows the link to be opened in another window.

<h2># CSS structure and Syntax</h2>

	* <style>
		button {	---> "button" is a CSS selector and indicates which element we are targeting
		background-colour: red; ---> background-colour = property, red = value
		}
	  </style>

<p>If you create more than one of the same element in html and want to style them differently, in your html code you'll' need to assign a class to the element. Once you have done that, you can them reference that call in your style sheet. For example:</p>

	* html element

	<button class="button_1">
		TEXT
	</button>

	<button class="button_2">
		TEXT
	</button>


	* CSS code

	.button_1 {	---> Here we are referencing the first button using the class name
		background-color: red;
		color: white;
	}

	.button_2 {	---> The same is being withe second button
		background-color: blue;
		color: white;
	}

<p>In CSS you also have something called a **sudo-class** in which you can add additional styling which is not recognised the general styling function. For example:</p>

	* class

	.button_1 {
		background-color: black;
		color: white;
	}

	* sudo-class
	
	.button_1:hover {	---> "hover" is a functon that allows the button you are hovering over with your cursor to change color depending on the styling you have given it
		background-color: grey;
	}

	* sudo-class

	.button_1:active {	---> This is another sudo-class which allows the opacity to change when you are activily on the button
		opacity: 0.7;
	}

<h2># Different kind of CSS styling</h2>

<p>Here is a list of some basic formatting functions in CSS that you can use to style your elements</p>

	* border: value; ---> styles the border of your element
	* height: valuepx; ---> gives height to your element using pixels
	* width: valuepx; ---> gives width to your element using pixels
	* color: value;	---> changes the color of the text
	* border-radius: valuepx; ---> curves the edges of the border using pixels
	* cursor: pointer; ---> changes the cursors icon when you are on the element
	* margin-direction: valuepx; ---> adds space in the direction you have specified, for the element using pixels
	* font-weight: value; ---> Adds weight to your font, such as bold, italic, etc...
	* font-style: value; ---> changes the font of the element
	* transition: sudo-class value time(sec); ---> this is used to style the sudo class you have created.


	
# end
