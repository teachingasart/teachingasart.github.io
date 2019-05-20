---
title: "Generative Random Art"
layout: post

# To set teaching:image:
# image: ...
---
A workshop presented by Teaching as Art Student [Jiwon Shin](http://jiwonshin.com/) 
<!DOCTYPE html>
<html>
<head>
    <meta name="author" content="Jiwon Shin">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css?family=Lato:100,100i,300,300i,400,400i,700,700i,900,900i" rel="stylesheet">
    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    <link rel="stylesheet" href="https://code.getmdl.io/1.3.0/material.indigo-pink.min.css">
    <link rel="stylesheet" href="../css/style.css">
    <script defer src="https://code.getmdl.io/1.3.0/material.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.16/p5.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.16/addons/p5.dom.min.js"></script>
    <script src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>
    <title>WORKSHOP | Generative Random Art</title>
    <!-- Global site tag (gtag.js) - Google Analytics -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=UA-110518171-1"></script>
    <script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', 'UA-110518171-1');
    </script>
</head>
<body>
<div class="mdl-layout mdl-js-layout mdl-layout--fixed-header">
    <main class="mdl-layout__content">
        <div class="page-content">
            <div class="full-page-content">
                <h3><b>Generative Random Art</b></h3>
                <p>In this workshop, we ask the fundamental question of what randomness is and what it looks like. By asking students to express what they think random is, and by looking at what can constitute as randomness in nature, the workshop attempts at defining random. We ask the question of whether complete randomness is useful in creating visuals and explore ways to tame the randomness to create a desired controlled randomized visuals in <a target="_blank" href="https://p5js.org/">p5.js</a>, a javascript library for creating visuals.</p>
                <p>Students will approach the concept of random first with pen and paper, to reflect on what their idea of random is. Then they will examine whether their idea of random is truly random and compare it with p5's idea of randomness. We will also compare two functions that can be used to generate random values in p5.js: random() and noise(). We will attempt at gaining a deeper knowledge of these functions by applying different visuals using these functions and go further into controlling it with other functions such as modulus(%) and map().
                </p>
                <p>This workshop is presented as a final project for <a target="_blank" href="https://teachingasart.github.io/posts/teachingasartday/">Teaching as Art</a> class at NYU ITP.</p>
                <hr>
                <h4>What is <b>RANDOM</b>?</h4>
                <p>We first begin by asking the question of what random is. What is random? Can you draw something that is random?</p>
                <img class="p-img" src="img/random-walk-with-seed.jpg">
                <p>Here is a video explaining what random is, and whether something is truly random. If you roll a dice, or flip a coin, is the result you get a *random* result?</p>
                <div class="video-wrap">
                    <iframe width="560" height="315" src="https://www.youtube.com/embed/9rIy0xY99a0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </div>
                <br>
                <p>If nothing is random, or at least, finding something that is truly random is hard, then how are we generating *random* numbers computationally?</p>
                <div class="video-wrap">
                    <iframe width="560" height="315" src="https://www.youtube.com/embed/GtOt7EBNEwQ" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </div>
                <p>For details about how Javascript generates the pseudo random numbers, check out this <a target="_blank" href="https://www.ecma-international.org/ecma-262/6.0/#sec-math.random">ECMA Script documentation on Javascript's Math.random() function</a> and this <a target="_blank" href="https://hackernoon.com/how-does-javascripts-math-random-generate-random-numbers-ef0de6a20131">Hackernoon article</a>.</p>
                <h4>Using random() in p5</h4>
                <p>We will first start off simple. Here is what you get if you use a random number to generate the x position of the ellipse.</p>
                <iframe src="https://editor.p5js.org/js6450/embed/bXJ7Gr9jq"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/bXJ7Gr9jq">Link to Code</a></p>
                <h4>Graphing random()</h4>
                <p>What are the properties of this graph? What's the width and height of this graph? What is the mid horizontal point of this graph? What is the maximum value and the minimum value?</p>
                <iframe src="https://editor.p5js.org/js6450/embed/sNZEDmYuN"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/sNZEDmYuN">Link to Code</a></p>
                <h4>Random Walks</h4>
                <p>As explained in the videos above, there is a concept of a random walk, which draws continuous lines of randomly generated x and y coordinates. Using the parameters of random we've discovered, how would be "control" this random walk?</p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/pd0lXqU_V"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/pd0lXqU_V">Link to Code</a></p>
                <p>The random() function that we use is PSEUDO random. How do we generate SAME random numbers for everyone? Click on the below sketch and press any keys to progress the "random" walk.</p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/vhMUr7Bj9"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/vhMUr7Bj9">Link to Code</a></p>
                <h4>What is <b>NOISE</b>?</h4>
                <p>What comes to your mind when you think of a noisy drawing / image? How would you draw it on a piece of paper? How is this different from the random drawing that you did previously?</p>
                <img class="p-img" src="img/noisy-img.gif">
                <img class="p-img" src="img/noise-2d.jpg">
                <img class="p-img" src="img/noise-walk.jpg">
                <p>In this workshop, we are going to talk specifically about Perlin noise. For more details about Perlin noise, read this <a target="_blank" href="https://flafla2.github.io/2014/08/09/perlinnoise.html">blog post</a>.</p>
                <p>We will start simple with this one too. Here is what the horizontal movement of an ellipse looks like using noise() function.</p>
                <iframe src="https://editor.p5js.org/js6450/embed/z5Dbv9tO5"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/z5Dbv9tO5">Link to Code</a></p>
                <h4>Graphing noise()</h4>
                <p>What are the properties of this graph? What's the width and height of this graph? What is the mid horizontal point of this graph? What is the maximum value and the minimum value?</p>
                <iframe src="https://editor.p5js.org/js6450/embed/mVEA_QnM1"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/mVEA_QnM1">Link to Code</a></p>
                <h4>Noise Walks</h4>
                <p>Here is an adaptation of the random walk that we saw using the noise() function. What are the differences? What are the similarities?</p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/aeykVYLr4"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/aeykVYLr4">Link to Code</a></p>
                <h4>Random vs Noise</h4>
                <p>Now lets look at how we can create different emotions to generate lines and shapes using random() and noise().</p>
                <p>Below are two simple drawing tools, using random() and noise().</p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/zokbnRFbM"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/zokbnRFbM">Link to Code</a></p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/odzvPMSWh"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/odzvPMSWh">Link to Code</a></p>
                <p>This is how we could animate a circular edged shape, to create a blob like movement, using random() and noise().</p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/UICJ8O9ul"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/UICJ8O9ul">Link to Code</a></p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/OHHeLDUo7"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/OHHeLDUo7">Link to Code</a></p>
                <h4>Code Example: Starry Ocean</h4>
                <p>Using the different characteristics of random() and noise(), this is an example of how the two different functions could be used to create a complete generated scene.</p>
                <iframe height="500px" src="https://editor.p5js.org/js6450/embed/922I-uQ4P"></iframe>
                <p><a target="_blank" href="https://editor.p5js.org/js6450/sketches/922I-uQ4P">Link to Code</a></p>
                <h4>References:</h4>
                <p>Here are some references and inspirations for the content of this workshop.</p>
                <p><a href="https://github.com/mimiyin/choreographic-interventions-s19/">Choreographic Interventions</a>, Mimi Yin</p>
                <p>Chapter 3: The Wrong Way to Draw A Line, <a href="https://www.manning.com/books/generative-art">Generative Art</a>, Matt Pearson</p>
                <p><a href="https://natureofcode.com/book/introduction/">Random Walks</a>, Nature of Code, Daniel Shiffman</p>
                <p><a href="https://www.youtube.com/watch?v=nfmV2kuQKwA">The random() Function</a>, Coding Train, Daniel Shiffman</p>
                <p><a href="https://www.youtube.com/watch?v=Qf4dIN99e2w">Perlin Noise</a>, Coding Train, Daniel Shiffman</p>
            </div>
            <footer class="mdl-mini-footer">
                <div class="mdl-mini-footer__left-section">
                    <ul class="mdl-mini-footer__link-list">
                        <li><u><a class="p-link" href="index.html" target="_self">BACK TO MAIN</a></u></li>
                    </ul>
                </div>
                <div class="mdl-mini-footer__right-section">
                    <ul class="mdl-mini-footer__link-list">
                        <li>Workshops By <u><a class="p-link" href="http://jiwonshin.com" target="_blank">Jiwon Shin</a></u></li>
                    </ul>
                </div>
            </footer>
        </div>
    </main>

</div>
</body>
<script src="../js/background.js"></script>
</html>
 
