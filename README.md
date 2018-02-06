## Website Performance Optimization portfolio project

This is the sixth project of the [Udacity Front-End Web Developer Nanodegree](https://www.udacity.com/course/front-end-web-developer-nanodegree--nd001). The main goal is to optimize the provided portfolio, in a purpose of getting more efficiency in the website performance.

To get started, check out the repository and inspect the code.

### Getting started

You can find the initial project commit [here](https://github.com/udacity/frontend-nanodegree-mobile-portfolio)

#### Part 1: Check Optimization in PageSpeed Insights score for index.html

##### Some useful tips to help you get started:
##### If you would like to run it in a local server:
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

1. Copy the public URL ngrok gives you and try running it through [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/).

##### If you would like to run it by your own server:
1. Check out the repository.
1. Upload all files in your server.
1. Open the **index.html** file in any browser.
1. Copy this live link.
1. To check the **optimization**, paste the link in [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/).

#### Part 2: Inspect Optimization of the Frames per Second in pizza.html

1. Check the same steps as in Part 1.
1. To inspect the **frame rate at 60fps or higher** and the **computational efficiency of resizing the pizza is less than 5ms**, open the console and performance tabs in DevTools in the browser.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization that has made
The optimization that has made in this project includes:

#### General HTML files include index.html
* Extra font has removed.
* `print.css` has merged with `style.css` to reduce file requests.
* Image file sizes have reduced.
* Added the text description `alt` in `<img>`.
* added `</div>` to solve the error of missing closing tag.
#### perfmatters.js
* File minified.
#### view/main.js
* `switch` statement in `changePizzaSizes` function to simplify which width has been chosen every case, and a `for loop` to set the width for every element to resize the pizza in less than 5ms.
* The line of `document.documentElement.scrollTop` has been deleted, and the usage of scrollTop has been changed with `i` in the `for` loop to generate some consistent pizzas across the screen with frame-rate at 60ps.

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
