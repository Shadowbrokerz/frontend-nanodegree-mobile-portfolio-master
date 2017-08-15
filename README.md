## How to run this application

* * *
* #### Cloning the repository
    ```
    $ git clone https://github.com/Shadowbrokerz/frontend-nanodegree-mobile-portfolio-master.git
    ```
* #### Go to the online hosted version
    https://shadowbrokerz.github.io/frontend-nanodegree-mobile-portfolio-master


## Optimisations

* * *
### Index.html
* Js files, Google fonts, Google analytics will load async so it won't interfere with page load.
* Images are compressed a bit to reduce the loading time.
* Inlined the CSS to avoid render-blocking problems.

I've got 93/100 on mobile and 95/100 on desktop

### Pizza page
* ##### Optimisations for Pizza resizing
    * I made so that when the slider get's moved it would apply a class according to the size of the pizza. That being **small**, **medium** and **large**. that way, I managed to gain a lot of frames and at the same time, use less resources.used getElementsById for faster calls.
    * Also added **will-change** on the elements that were turning green when scrolling or changing the slider, it has given me more frames as well.
Resizing time went down to 1.5~ ms
* ##### Optimisations for Pizza Scrolling
    * In ***updatePositions(e)*** I firstly changed the for loop with the length of the elements. Then instead of the *left* CSS property I used *transform* so I can get rid of the repainting problem. I also added a timeStamp so it could refresh less frequently.Declared some variables outside the loop to avoid extra declaration. Used getElementsByClassName for faster calls.
    * Going down to the bottom of the script where the background pizzas are being generated I changed the amount of pizzas down to 35, there were too many and I thought it was unnecessary. Applied so that in the for loop I would use the screen size, so I could reduce the amount of pizzas for space in the screen.




