
#### HTML Questions:

* What does a `doctype` do?
  - Doctype is required at the top of the page to tell the browser how to render the code and what specifications to use (standards mode vs. quirks mode).

* What's the difference between standards mode and quirks mode?
  - <!DOCTYPE html> indicates that the browser should use full standards mode. Quirks mode emulates the behavior in Netscape navigator and IE 5 for older websites. Full standards mode follows the HTML/CSS standards.

* What's the difference between HTML and XHTML?
  - XHTML is indicated in the Content-Type header as application/xhtml+xml instead of text/html. It can travel over the network in either HTML or an XML format called XHMTL. IE 8 and older browsers show a dialog box to download the page. It must follow the restrictions of XML such as not using double dashes in comments. The main benefits are that the document would be compatible with XML tools, it would    be easy to transform the content for mobile devices. It also allows for XHTML Modularization to support different data types.

* Are there any problems with serving pages as `application/xhtml+xml`?
  - Yes, there are many addional restrictions the contents must follow in order to be properly displayed. Also, IE 8 and older browsers will show a dialog box to download the page.

* How do you serve a page with content in multiple languages?
  - You indicate the language in the element surrounding the content in each language. In the html element, you indicate the most prominant language (ie. <html lang="en">).
  
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
  - 'data-' attributes are good for storing additional metadata about your HTML for which there an other appropriate elements attributes or elements. These attributes are then accessible in JavaScript to alter the way that the content is displayed. For example, when creating a modal you might use a data-target attribute to indicate what contents will be shown in the modal or a data-dismiss attribute to indicate what elements should be hidden when when the modal is closed. 

* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
  - Semantic HTML, JavaScript API, web worker API, video and audio elements, CSS3, SVG, Geolocation API

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
  - A cookie is stored on the client-side. It is protected against Cross-Site Scripting (XSS) and Script Injection by setting an HTML only flag that will prevent access to the cookie through JavaScript. Thus, cookies are sometimes used for authentication purposes to store access tokens. However, session storage is the most secure option. 
  - sessionStorage is saved on the client side, but session data is stored on the server side. Each unique user is given a session id and inf
  - important side notes: HTTP is a stateless protocal. Using sessionStorage allows the server to add a stateful layer to the protocal.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
  - script: HTML parsed until script tag, parsing PAUSED, script downloaded and executed, parsing continues (IN ORDER)
  - async: HTML parsed, script downloaded while parsing continues, parsing PAUSED, script executed, parsing continues (ANY ORDER)
  - defer: HTML parsed, script pdownloaded while parsing continues, parsing ENDS, script executed (IN ORDER of inclusion in HTML file)
  - http://www.growingwiththeweb.com/2014/02/async-vs-defer-attributes.html
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
  - Putting the CSS in the head ensures that the styling is download and parsed before the body of the document so it will be applied before anything is rendered. Otherwise, there might be a gap between when the html is rendered and when the styling is applied
  - Putting the JS script right before the end of the body ensures that the JavaScript does not keep the page from rendering and that any elements referenced in the JS (ie. in jQuery) have already been created when the script executes. 
  
* What is progressive rendering?
  - An image is rendered top-down as the bits are received. This is how an image will traditionally be rendered if you don't make any changes to it (ie.interlacing).
  
* Have you used different HTML templating languages before?
  - Underscore
