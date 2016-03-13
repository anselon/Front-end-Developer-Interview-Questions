#### CSS Questions:

* What is the difference between classes and ID's in CSS?
  - ID's are used as unique identifiers. ID's take precedence of classes in CSS. It is best practice to only use classes when applying styling to your HTML.
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
  - Resetting removes all the automatic styling that a browser applies, so that you can ensure your styling will look the same in every browser. 
  - Normalizing changes the automatic styling applied by the browser to be the same in every browser. 
  - Normalizing is generally more mantainable and doesn't require as much additional code because you would end up reapplying a lot fo the automatic styling that gets taken away in resetting. 
  
* Describe Floats and how they work.
  - Floating an element changes the flow of elements inside of another given element. You can designate whether the inner element will align to the left or right of its outer div. The parent element's size will no longer depend on it's children's size when float is used. 
  
* Describe z-index and how stacking context is formed.
  - z-index allows you to determine in what order the elements will be displayed on the z-axis (front to back).
  - a stacking context is formed by any element:
      - with opactiy < 1
      - the root element (HTMl)
      - a z-index value that is not "auto" is assigned to a flex item with parent display:flex
      - position: fixed
      - other cases: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context
  
* Describe BFC(Block Formatting Context) and how it works.
 - the region in which the layout of block boxes occurs ans in which floats interact with eachother
 - floats only effect the layout of their own BFC.
 - https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context
  
* What are the various clearing techniques and which is appropriate for what context?
 - add an element to the bottom of the container or floats with .clear{ clear:both}
 - change the container to have overflow:hidden (froces container to take on height of child (floated) divs
 - change .container to have min-height:conatain-floats;
 - add class .clearfix to .container with css .clearfix:after { display:table;content:"";clear:both}
    - this creates another element like the first solution
    
* Explain CSS sprites, and how you would implement them on a page or site.
  - sprites are concatenated images used to reduce the bandwidth required to load a page because all the images are received with one request instead of in separate requests. 
* What are your favourite image replacement techniques and which do you use when?
- SVG 
- 
* How would you approach fixing browser-specific styling issues?
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
* Describe pseudo-elements and discuss what they are used for. 
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
* Have you played around with the new CSS Flexbox or Grid specs?
* How is responsive design different from adaptive design?
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?
