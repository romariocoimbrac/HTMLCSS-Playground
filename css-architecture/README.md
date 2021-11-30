# CSS Architecture

Just knowing and using the basic principles does not guarantee flexible, reusable, and maintainable development. Design patterns represent solutions that try to fill these needs.

Some patterns are organization basics regardless of which methodology you want to use.
Adding classes to your css instead of using the tags themselves, organizing the attributes of each class in alphabetical order so you can more easily find an item and discern when images should be used by the img tag or as a background in another tag are examples of tricks for a good css.
We'll look at how to apply a modular, organized, and more meaningful approach through three basic principles:

1. Divide and conquer
   Break the code into smaller pieces and separate them by scope.
2. Consistency
   Encode components independently and encapsulated.
3. Standardization
   Name CSS selectors according to their purpose and relationship to each other.

## Atomic Design

This model come from the comparison that internet pages are like systems, that is, sets of elements that, connected as a whole, form an organism.
[Brad Frost](https://bradfrost.com/blog/post/atomic-web-design/), creator of this methodology, was the one who realized that the components of a website behave similarly to atoms, molecules and organisms.
Web pages are basically composed of a finite group of elements (HTML tags) and can be grouped together in different ways to create complex systems.

**Atoms** <br>
Atoms are the smallest possible elements, something that by itself does not completely define something. These are for example single HTML tags, a title \<h1>, a list \<ul> or a paragraph \<p> with no connections.
They are the basis for creating molecules.

**Molecules** <br>
Molecules are groups of atoms. For example a title tag and a paragraph within an \<article> form a movie synopsis.

**Organisms** <br>
The union of atoms creates molecules which then interconnected create an organism. For example a \<section> with a list of movie titles, containing the synopsis on each item.

**Template** <br>
The template can already be considered the final part of the design evolution, but in a simpler and more abstract way. The template is a union of more generalist tags, such as the union of several \<section> creating an outline of a page.

**Page** <br>
The page is when the template is instantiated and becomes real, with all the details and information. This is the last stage of the design and the final version.

## BEM Methodology

BEM (Bloc Element Model) is based on the idea of ​​dividing the page into blocks. It's a CSS class naming methodology that helps you create reusable and maintainable code.

**Block** <br>
Block is a logically independent component that encapsulates styles, behavior, or implementation technologies. This independence makes the blocks easily reusable.
Blocks can also coexist in other blocks and will work the same as if repeated out of position or reused in other projects.

**Element** <br>
An element is a kind of block part. The block works like a box and the elements are the items placed in it that perform specific functions.
The element is a part of a block that cannot be used for it. For example, items within the menu block or entries in a form.

**Modifier** <br>
The modifier is optional. It is responsible for defining the state, a form and behavior of blocks or elements. Identical blocks may look different because of a modifier.

The idea behind many BEM naming conventions is to make them as informative and easy to understand as possible.
In this style, blocks must be separated by two underscores (\_\_), and modifiers must be separated by two dashes (--). Each of the blocks, elements and modifiers can be separated by a hyphen (-).

```
.block {}
.block__element {}
.block--modifier {}
.block__element--modifier {}
```

I created [this website](https://romariocoimbrac.github.io/HTMLCSS-Playground/css-architecture/example/) so that you can have an example of how these patterns work in practice.
