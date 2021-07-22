HTML & JAVASCRIPT
How People access the Web ?
 	 
Browsers	People access websites using software called a web browser For example:Firefox, Internet Explorer, Chrome, and Opera
Web Servers	Web Servers When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a web server which hosts the website
Screen reader	Screen readers are programs that read out the contents of a computer screen to a user. They are commonly used by people with visual impairments
 	 
html

In all kinds of documents, structure is very important in helping readers to understand the messages you are trying to convey and to navigate around the document

HTML describesthe Structure of Pages

The HTML code is made up of characters that live inside angled brackets — these are called HTML elements. Elements are usually made up of two tags: an opening tag and a closing tag. (The closing tag has an extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags.
Examples :
< body > : Everything inside this element is shown inside the main browser window .

< head> Before the <body> element you will often see a <head> element. This contains information about the page.
HTML stands for * HyperText Markup Language* . The HyperText part refers to the fact that HTML allows you to create links that allow visitors to move from one page to another quickly and easily. A markup language allows you to annotate text, and these annotations provide additional meaning to the contents of a document. If you think of a web page, we add code around the original text we want to display and the browser then uses the code to display the page correctly. So the tags we add are the markup.

You can Create a Web Page on a PC or on a Mac…

Since the web was first created, there have been several different versions of HTML.

Each new version was designed to be an improvement on the last (with new elements and attributes added and older code removed).

DOCTYPES tell browsers which version of HTML you are using.

If you want to add a comment to your code that will not be visible in the user’s browser, you can add the text between these characters:

** < !– comment goes here → **

Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page.The id attribute is known as a global attribute because it can be used on any element. Every HTML element can also carry a class attribute. Sometimes, rather than uniquely identifying one element within a document, you will want a way to identify several elements as being different from the other elements on the page.

Some elements will always appear to start on a new line in the browser window. These are known as block level elements. Examples of block elements are < h1>, < p>, < ul>, and < li>.

Some elements will always appear to continue on the same line as their neighbouring elements. These are known as inline elements. Examples of inline elements are , , , and .

An iframe is like a little window that has been cut into your page — and in that window you can see another page. The term iframe is an abbreviation of inline frame.

The element	Discribtion
< div>	allows you to group a set of elements together in one block-level box.
< span>	acts like an inline equivalent of the < div> element ,the most common reason why people use < span> elements is so that they can control the appearance of the content of these elements using CSS.
< Meta>	The < meta> element lives inside the < head> element and contains information about that web page. The < meta> element is an empty element so it does not have a closing tag. It uses attributes to carry the information.
< nav>	used to contain the major navigational blocks on the site such as the primary site navigation.
< article>	acts as a container for any section of a page that could stand alone and potentially be syndicated.
< article>	used inside an < article> element, it should contain information that is related to the article but not essential to its overall meaning. When the < aside> element is used outside of an < article> element, it acts as a container for content that is related to the entire page.
< section>	groups related content together, and typically each section would have its own heading.
< hgroub>	group together a set of one or more < h1> through < h6> elements so that they are treated as one single heading.
< figure >	Examples of usage of < figure >include: Images,Videos , Graphs,Diagrams,Code samples,text that supports the main body of an article .The < figure> element shouldalso contain a < figcaption element which provides a text decription for the content of the < figure> element.
< script>	Tell the browsre to load the JavaScript file
< Link>	used to load a CSS file
Older browsers that do not know the new HTML5 elements will automatically treat them as inline elements. Therefore, to help older browsers, you should include the line of CSS on the left which states which new elements should be rendered as block-level elements. header, section, footer, aside, nav, article, figure { display: block;}

To make HTML5 elements work in Internet Explorer 8 X (and older versions of IE), extra JavaScript is needed, .which is available free from Google.

Every website should be designed for the target audience—not just for yourself or the site owner. It is therefore very important to understand who your target audience is.

Your content and design should be influenced by the goals of your users. Site maps allow you to plan the structure of a site.

A wireframe is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require.

Visual hierarchy helps visitors understand what you are trying to tell them.

You can use JavaScript to add elements, attributes, and text to the page, or remove them. A script is a series of instructions that a computer can follow to achieve a goal

Computers use data to create models of things in the real world. The events, methods, and properties of an object all relate to each other:

The document object is just one of a set of objects that all major browsers support. When the browser creates a model of a web page, it not only creates a document object, but it also creates a new object for each element on the page. Together these objects are described in the Document Object model.
