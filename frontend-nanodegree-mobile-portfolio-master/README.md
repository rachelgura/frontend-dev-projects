## Website Performance Optimization portfolio project


To open the application please open html.index in your browser.

Getting started



Part 1: Optimize PageSpeed Insights score for index.html



1. Minimized and inlined the whole style.css stylesheet.
2. Make print.css async and place at the end of index.html file
3. Make google font, analytics.js and perfmatters.js all async and place at the end of index.html file
4. Move Google analytics object function to the end of index.html file
5. Reduced pizzeria.jpg size and compressed
6. Compressed profilepic.jpg

Scores 95 Mobile and 96 Desktop

1. Made the same adjustments to project-2048.html, project-webperf.html and project-mobile.html They all came in over 90

Part 2: Optimize Frames per Second in pizza.html

1. On pizza.html, I inlined the elements that showed up above the fold then placed style.css at the end of the file as async.
2. On main.js I finally figured out that the for loop inside the updatePositions() function was only calculating five numbers and repeating that 40 times for every scroll event. So I created an array to calculate and store the five numbers outside of the for loop and then assign them inside the loop. That brought the fps up to 60.
3. The changePizzaSizes() function had the same problem since all pizzas are resized to the exact size. So I declared the two variables outside of the for loop using the first pizza's size as the model. Then assigned the new size inside the loop.
4. Changed  the behavior of the pizza number in the background.