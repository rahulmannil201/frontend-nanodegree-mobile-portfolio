## Website Performance Optimization portfolio project

our challenge was to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques i have picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

our aim is to have a PageSpeed Insights score for atleast 90 or above for Desktop and Mobile

instructions
===========

1. url for index.html is https://rahulmannil201.github.io/frontend-nanodegree-mobile-portfolio/

2.copy this url into Google Pagespeed Insight https://developers.google.com/speed/pagespeed/insights/ to check scores

running website locally
====================
1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! 


 
 
 
Optimisations
=============
1. optimized all images using picsresized.com

2.used async word with script tag inodrer to process javascript in the background

3.use media="print" for the css which is meant for printing

4.inlined  css into index.html instead of a external file

intially the score was very low for desktop and mobile.after optimisations it rise up to 95/100 for mobile and 96/100 for desktop
 



####Part 2: Optimize Frames per Second in pizza.html

our aim to optimize views/pizza.html, by modifying views/js/main.js until your frames per second rate is 60 fps or higher

instructions
===========
1.open https://rahulmannil201.github.io/frontend-nanodegree-mobile-portfolio/ in ur browser

2.click on Cam's Pizzeria link and u will be redirected to pizza.html

3.scroll the webpage u will pizza moving

4.take google dev tools and check fps value



Optimizations
=============
1.queryselector is replaced with getelementsbyclassname in order to speed dom scanning(line no 516)


2.queryseector is replaced with Getelementbyid for faster dom processing(line no 409-416, 547)

3.updated updatePositions function var phasetop was taken out of the for loop(line no 518)

4.for addeventlistener created var movpizza and moved it out of the for loop and decreased i value from 200 to 24(atleast there should be 3 full rows)

5.changed changepizzasizes function var pizzasizes was taken out of the for loop and optimized 

6.moved var newwidth outside of the for loop inodrer to avoid calucating dx everytime on iterations(line no 462)

7.moved varpizzasDiv outside of the for loop inodrer to speed dom scanning(line no 483)

8.moved var elam outside of the for loop inodrer to avoid creating that variable every time


