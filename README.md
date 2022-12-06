# Gfetch_init

## Abstract
 This repo contains the most simple initial setup to start using the Gfetch.js module in a static website.
 
 I created this module with the desire to have a tool as simple as possible to be able to create an online site quickly and visually, with all the advantages of dynamic content management and the immediacy of an app like Google Docs which we are all used to working with.
 
 Check the following links to discover more on that:
 <br>
 https://medium.com/@danilo_fiumi/gfetch-your-next-cms-for-static-websites-59dcaabde377 <br>
 https://danilofiumi.github.io/blog-gfetch.html <br>
 https://observablehq.com/@danilofiumi/html-rendering-gfetch-module <br>
 https://youtu.be/eHjYMJSfSjc <br>

![1_PbDMLpOG4LBCWeyYXs8DTw](https://user-images.githubusercontent.com/76904889/205452996-c22aaa72-aa56-467e-9a28-3cab07996f2d.jpeg)


## How to use it?
Let’s clone the repo on github with the following command:

```git clone https://github.com/danilofiumi/Gfetch_init```
You will get 3 files:
NB: This file arrangement is absolutely prototypical and is intentionally simplified to give as many people as possible a chance to understand how it works and how to use it. For possible improvement proposals, take a look at section 6.

Gfetch.js: The main module described in the following [Notebook](https://observablehq.com/@danilofiumi/html-rendering-gfetch-module) and exported in JavaScript
index.full.js: A reworked setup file that enables the Observable runtime. This to have continuity with what has been described previously.
index.html: Main HTML file in which the Google docs code will be injected.

Let’s open the index.html file.
The only elements that allow the module to work are the 5 below:
![image](https://user-images.githubusercontent.com/76904889/205995153-1a6aec84-99a8-4323-8f43-e79701345ba9.png)


NB: All the other elements are classes from Bulma, a CSS framework, which are used to give a minimum of positioning and style within the page, (for more details check https://bulma.io/).

Let’s go through them one by one.

The first two are <script> elements and are used to import the JavaScript codes described above.

The div with the id equal to “link” is an element that contains the url from which we want to retrieve the information (in the repo is the sample link linked to the same demo document shown in the observable notebook). Note that in this plain vanilla version the style is on “display:none”, so it will not be displayed on the page but will only serve as a configuration element.

The div with the id attribute equal to “placeholder” will be the element inside which we are finally going to render the html code exported from Google sheet.

The <img> tag with id equal to “image-src” will be the element in which the src value will be replaced with that of the image source in the Google document.


To customize it with your own content, simply follow the steps below:

- Create a new Google document
- Create your own content with the respective keys
- Click on share at the top right of the document
- Enable access to anyone with the link
- Copy the link
- Paste the link into the div with id=”link”
- Update the HTML elements in index.html so that “id” attributes match the keys

for the detailed guide on how to configure document rights so that it communicates with index.html I refer to this viedo or to the guide on my (personal website)[https://danilofiumi.github.io/blog-gfetch] (ITA only):

<iframe width="560" height="315" src="https://www.youtube.com/embed/eHjYMJSfSjc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
