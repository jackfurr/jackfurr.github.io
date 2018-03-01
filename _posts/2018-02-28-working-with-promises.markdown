---
layout:     post
title:      "Working with Promises"
subtitle:   "Simple things to remember when working with Promises"
date:       2018-02-28 13:00:00
author:     "Jack Furr"
header-img: "img/post-bg-01.jpg"
categories: [Javascript, Node.js, Promises]
comments: true
---

<div class="row">

	<div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
    <h2>Promise Contructor</h2>
		<p>
    Over the past few months I've started embracing Promises and async/await in my daily coding sessions.
    </p>

    <p>I find that the only time I need to use a Promise contructor is when I need to call a function that uses callbacks. If you are calling a function the returns a Promise, there's no need to use a Promise contructor.
    </p>

    <p data-height="582" data-theme-id="0" data-slug-hash="yvZvbx" data-default-tab="js" data-user="jackfurr" data-embed-version="2" data-pen-title="yvZvbx" class="codepen">See the Pen <a href="https://codepen.io/jackfurr/pen/yvZvbx/">yvZvbx</a> by Jack Furr (<a href="https://codepen.io/jackfurr">@jackfurr</a>) on <a href="https://codepen.io">CodePen</a>.</p>
    <script async src="https://static.codepen.io/assets/embed/ei.js"></script>

	</div>

  <div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
    <h2>Converting Callback Functions</h2>
    <p>In some cases it's just not possible to make complete changes to your codebase to use Promises everywhere. To help with the migration from callbacks to Promises, I've found that wrapping the function in a Promise constructor and returning a callback (if supplied) or the Promise if the callback is not supplied, works well. </p>

    <p>Callback style</p>
    <p data-height="261" data-theme-id="0" data-slug-hash="gvqvaL" data-default-tab="js" data-user="jackfurr" data-embed-version="2" data-pen-title="gvqvaL" class="codepen">See the Pen <a href="https://codepen.io/jackfurr/pen/gvqvaL/">gvqvaL</a> by Jack Furr (<a href="https://codepen.io/jackfurr">@jackfurr</a>) on <a href="https://codepen.io">CodePen</a>.</p>
    <script async src="https://static.codepen.io/assets/embed/ei.js"></script>

    <p>Hybrid style (Promise/Callback)</p>
    <p data-height="270" data-theme-id="0" data-slug-hash="KQJQzo" data-default-tab="js" data-user="jackfurr" data-embed-version="2" data-pen-title="KQJQzo" class="codepen">See the Pen <a href="https://codepen.io/jackfurr/pen/KQJQzo/">KQJQzo</a> by Jack Furr (<a href="https://codepen.io/jackfurr">@jackfurr</a>) on <a href="https://codepen.io">CodePen</a>.</p>
    <script async src="https://static.codepen.io/assets/embed/ei.js"></script>

  <p>Now I can call the code and pass in a callback and it will still work as before. But for the new code that I am writing where I am using Promises, I can call the same function but not pass in a callback and the function will return a Promise.</p>

  <p>At some point you should remove the Hybrid-style code and just use Promises.</p>

  </div>

  <div class="col-lg-8 col-lg-offset-2 col-md-10 col-md-offset-1">
		<p>Thanks for checking out this short code review, and good luck!</p>
	</div>

</div>
