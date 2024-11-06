# css-drills
CSS Drills Project

The purpose of this lab is to deepen your understanding of CSS fundamentals, specifically focusing on positioning properties and the order of specificity. Let's do this!!

Project Setup
Create a new project folder and connect it to a github repository. Copy the text from this README.md file into it.
Create an index.html file and a styles.css file.
Use the ! emmet shortcut to stub out the page.
In the <head>, link the the CSS file to the HTML page.
Build the HTML Structure
In the <body> element, create a <main> with an id of "container".
Inside #container, add four <div> elements with a class name of "box" and a unique id (box1, box2, etc.). Each added div will be a child of the #container and a sibling to each other.
Within each "box", include an <h2> for the title, a <p> for the description, and an <a> with the text "Read More".
h2: Add a story title in each header
p: Add a story description within each paragraph
a: Add a link that says "Read More"
Text and Body Styling
Assign a global font family
Here is a list of some Web Safe Fonts: https://www.w3schools.com/cssref/css_websafe_fonts.php
You could also play around with Google Fonts: https://fonts.google.com/
Hint: use the body selector.
Change the background color for the body element to a light grey color.
Use a multiple selector rule set to center the text for all h2, p, and a elements.
So you notice that the link is not centered like the h2 and p elements. This is because text-align will center the element based on the width assigned to it. If you apply a border to the link tag, you'll see that the link is centered inside the anchor element. The best way to center the link, relative to its parent element, is to enclose it inside of a div element.
This is a common technique you should be aware of!
Wrap the anchor element inside of a <div> and give the <div> a class name of "readme-wrapper".
Replace the a in the multiple selector rule with .readme-wrapper instead.
Now refresh and you'll see the link is centered as we expected it. Huzzah!
Use an element selector to remove the default underline styles for anchor tags and change the font color.
Add a CSS :hover selector so that when the link is moused over the cursor changes to a pointer, the font is bold, and text color changes.
Wrap a single word in each <p> element inside of a <span> element and assign it a new font color and font weight.
You can do the first word of each description inside each of your <p> elements, for example.
Box Styling
Use a class selector to target the .box class:
Add margin.
Add padding.
Add a solid border with a custom color.
Add a border radius to round the edges of the border.
Add a width of 30rem.
Use an ID selector to add a unique background color to each div.
Your lab at this point should resemble something like this, with the colors and margin/padding sizes being different for you, of course! Boxes before being re-positioned

Note: The backgrounds are different in the screenshot, they are just darker shades of the same color from #box1 :P
Position, How Does It Work?!
Change the display to inline-block in your .box class selector.
Notice how the .box <div>'s will now sit next to each other because of this rule.
inline-block will make block level elements flow next to each other based on their size, instead of taking up the entire block!
Change the display to block in your .box class selector.
Notice how it goes back to the previous flow without any display change? That's because by default <div> elements follow block rules by default! Cool. You should remember that.
We're gonna leave it on block for now to do the next steps ...
Change the position of the second box div (#box2) to be relative to its parent.
Changing that didn't seem to do anything to the flow of the page, right?
Now position the second box div (#box2) to be next to the right side of the first box.
Hint: try using bottom and left properties on the second box div with various values. We're "nudging" this div from where it should be in the flow of elements.
It won't be perfect, but it should resemble something like this, and take notice that the element flow acts as if that div is still in its original spot!
We've moved this element relative to where it's supposed to be, without breaking the original flow of html elements.
Now change the second box div to position absolute
Madness!! Notice how it moved somewhere strange, and now the other box divs act as if the second one isn't in the flow anymore.
Like we learned from the lectures, relative has our HTML keep the element in the flow whereas absolute removes it from the flow.
Also remember that without a parent element having position: relative; added to it, then that means the absolute positioned box will be relative to the document itself.
Adjust your position using any of the top, bottom, left, right properties to get it back to being next to the first div.
It should look something like this, and notice that the other divs flow as if the "absolute" div isn't included anymore!
Remove the position styling (including all the top/bottom/left/right) from the second box div (#box2). This should make it return to what it looked like before being re-positioned.
Add a new new <div> element in your HTML above the <h2> elements in each box. These will not wrap anything, but rather be stand alone, like this: <div></div>.
These <div>'s will be representing "images" for each box.
Give all four of these <div>'s a custom class name they all share.
Select that class in your CSS, and add the following properties:
Add a height and width property with a value of 50px.
Add a border radius property of 50px.
Add a custom background color.
You should have something close to this with those divs added and styled, with your own color, of course!
Use your new knowledge of positioning to get that circle <div> next to the <h2> element! Shoot for a goal looking similar to this screenshot.
It probably won't be perfect and it might scale strangely if you change your browser size, but that's okay! Raw CSS is tricky. We'll learn better ways to handle these issues later. :)
Styling Specificity
The following HTML code will be below the .container element, but still within your </body>. So under all the box business you've been writing so far.

Insert 3 <h1> tags into the html document, give each text for your favorite TV shows.
Apply styling so that all <h1>'s have a font color of your choice.
Add 2 more <h1>'s with 2 other TV shows. What immediately happens to their font color when you refresh the html document?
Give all the original 3 <h1>'s the class name "original".
Give the newer additional 2 <h1>'s the class name "additional".
Apply styling by class name, have the first 3 <h1>'s get a new font color (don't delete or comment out the original styling). Once you apply a new font color by class, refresh the page and see what it does.
Do the same thing for the additional 2 <h1>'s, give them a different font color by class name.
Take note at what which font color rule is in effect. Class is a more specific rule than element in CSS selectors! So it'll override the element selector styling and use the class selector styling.
Rank each TV show you have (so all 5 <h1>'s), a rank of show1 would be the best. Have the rank be the id of each <h1>. At this point every <h1> should have a class AND an id attribute.
Apply styling using the id of each <h1>, give each a different color. Refresh the document and see how this type of styling changes what was already applied.
Take note that your class selectors are now overridden by the id selectors! They are more specific and will use those styles instead of the class or element selectors on these <h1>'s.
Below the <h1>'s, create 3 unordered lists (<ul>), each with 5 items (<li>), have the first list be 5 friend's names, have the next be 5 places you want to travel, and have the last list be your 5 favorite restaurants.
Apply styling to all the <ul>'s using an element selector changing their font color.
Add the class "star" to the second and third <ul>.
Apply styling to the class "star" changing the font color.
Add the id "wars" to the third unordered list.
Apply styling to the id "wars" changing the font color.
Take note again on the order of specificity between element, class, and id selectors.
TL;DR element selector styling is less specific than class selector styling is less specific than id selector styling.
Wrap each <ul> in a <div>, give the <div> a border that is 2 pixels thick, have it be solid and the color be black.
It'll look like a multi color fiasco, but the purpose here was to learn how specificity works!

But isn't styling fun? We know it can be tricky and tedious, but the more you practice, the better you'll get at it. After a while, you won't even think about it anymore :)

Closing Remarks
Congratulations on completing the CSS Drills lab! Through this lab, you've practiced essential CSS skills, exploring how positioning, specificity, and various styling techniques can be applied to enhance your web development projects. Remember, the key to mastering CSS is consistent practice and experimentation. Each element and property you've learned to manipulate serves as a building block for more complex designs.

As you move forward, keep challenging yourself with new CSS features and scenarios. Experiment with different layouts, explore new properties, and always keep in mind the importance of responsive and accessible design. The skills you've honed here form the foundation for creating beautiful, functional, and user-friendly websites.

Keep coding, keep learning, and remember to have fun with your CSS adventures!
