# CSS Questions

<div class="head">

## Explain CSS Selector Specificity

</div>

**Specificity** is the process of determining which caa rule will be applied to an element. 

Specificity determines which rule is applied by the browser - clear understanding of specificity prevents the need to use `!important`.

The **universal selector (*) has low specificity**, while the **ID selectors are *highly* specific**. 
Specificity is a common reason why CSS rules don't apply to some elements like you think they should.

<div class="head">

## What's the difference between "resetting" and "normalizing" CSS?
</div>

**Resetting** strips all default browser styling on elements.
**Normalizing** preserves default styles deemed useful rather than "unstyling" everything.

<div class="head">

## Describe floats and how they work
</div>

`Float` is used for CSS positioning. For example, if you have a block of text and an image, you might try to "float" the image next to the text.
Floats remain a part of the flow of the page, and affect the positioning of the rest of the elements (unlike position: absolute elements).

The `clear` property can be used to position a specified element left/right/both of floated elements!

<div class="head">

## Explain z-index and how stacking context is formed
</div>

`z-index` is the ability to specify the order in which elements can stack on top of each other (overlap), and its value ranges from 1 to 9999.

z-index only effects elements with a position value (that isn't static-aka default)

<div class="head">

## Describe Block Formatting Context (BFC)

</div>

This is part of the visual CSS rendering of a webpage in which "blocks" are laid out: **floats**, **positioning**, **-blocks**, **table-cells**, elements with **overflow**, and others all **establish new block formatting contexts.**

An HTML "box" is defined by one or more of the following conditions:
* The value of **float** is **none** <br/>
* The value of **position** is neither **static** nor **relative**
* The value of **display** is **table-cell**, **table-caption**,  **-block**, **flex**, or **-flex**
* The value of **overflow** is not **visible**

In BFC, each box's left outer edge touches the left edge of the containing block.

<div class="head">

## What are the various clearing techniques?

</div>

* Empty div method: &lt;**`div style="clear both;"`**&gt;
* `Clearfix` method
* `overflow:auto` or `overflow:hidden` - parent will establish a new BFC, and expand to contain its floated children.

<div class="head">

## What are CSS sprites, and how might you implement them?

</div>

Sprites combine multiple images into a single larger image. It's commonly used for **icons**. You can use a **sprite generator** to pack multiple images into one, and generate the appropriate CSS for it.

<div class="head">

## How would you approach fixing browser-specific styling issues?

</div>

This issue really relates to **vendor prefixes**: this can be taken care of for example by a. **CSS/Sass variables**, b. **Using a library like prefix-free (an autoprefixer)**, or c. **Use Reset CSS or Normalize.css**.

<div class="head">

## How do you serve your pages for feature-constrained browser?

</div>

-**Graceful degradation**, or building an application for modern browsers, while still remaining functional for older browsers.
-**Progressive enhancement** - building an application for a base level of user experience, and then adding functional enhancements when a browser supports it.
-perform **feature detection** with **Modernizr**.

<div class="head">

## What ways can you visually hide content and make it available only for screen readers?

</div>

* Using `visibility: hidden`.
* `position: absolute; left: -99999px` - positions outside of the screen

<div class="head">

## What's SVG styling?

</div>

It's the ability to color shapes using either internal CSS, an embedded CSS section, or an external CSS stylesheet. 
Basic coloring can be done by setting two attributes on the **node**: `fill` and `stroke`.

<div class="head">

## Can you give an example of a @media property other than screen?

</div>

There are four total types: 
1. `print` (printers)
2. `speech` (screenreaders)
3. `screen` and 
4. `all`

<div class="head">

## What are some "gotchas" for writing efficient CSS?

</div>

The shorter the length of a selector chain, the faster the browser can determine if that elemenet matches the selector.

**BEM Methodology** - which recommends everything has a single class.

<div class="head">

## What are advantages and disadvantages of using CSS preprocessors?
</div>

CSS is for writing high-level css with special syntax.

#### Advantages:
* Able to use Javascript concepts in CSS
* Able to emphasize **code reuse** and **modularity** with your CSS
* Able to use **mixins** for **generating repeated CSS**

#### Disadvantages:
* Have extra step of compiling - need to 1. **Watch** and 2. **Automate** task with Gulp for example.

<div class="head">

## How would you implement web design that uses non-standard fonts?

</div>

Use `@font-face` to define font-family for different font-weights.


## Describe **pseudo-elements** and what they're used for

* Uses **colon notation** (double for CSS3, single for CSS2 and 1 - fine to use single still)
* Used to **style specific aspects of an element** (i.e. the "hover" of an element) - not unlike "sub-element".



<div class="head">

## What does clip do in CSS?
 
 </div>

Allows you to specify how much of an element is visible, and specify how that element is "clipped".

<div class="head">

## What's the difference between inline and inline-block?
 
 </div>

* block - starts on a **new line**
* inline-block - **flows along** with other content; allows other elements beside it

<div class="head">

## What's the difference between relative, fixed, absolute and statically positioned elements?

</div>

* `Static` is the default position. It flows into the page like it normally would.
* `Relative` means the position is adjusted for an element relative to itself, without changing layout. When the element moves (ex: up: 200px;), no other element in the layout is affected!
* `Absolute` is removed entirely from the flow of the page, and is positioned relative to the nearest positioned parent element (unlike fixed, which is positioned relative to the viewport).
  It allows you to place any page element exactly where you want it, using `top`, `right`, `bottom`, and `left`. These values are **relative to the next parent element that itself has relative or absolute positioning**. If there's no such parent, it defaults all the way up to the &lt;`html`&gt; element (so then it operates similar to `fixed`; however, `absolute` elements still scroll, while fixed elements don't!).
* `Fixed` doesn't move on scroll - **its position is relative to the viewport**.

<div class="head">

## What existing CSS frameworks have you used, either locally or in production?

</div>

Bootstrap.

<div class="head">

## Can you explain the difference between coding a website for responsiveness, versus a mobile-first design?

</div>

Mobile-first means you are designing a webpage literally for mobile devices in mind, and then implementing it for desktop screens - it means defining all styles specifically for mobile devices, and only adding specific responsive rules to other devices later.

Responsiveness is adjusting certain elements depending on screen (typically **viewport width**).

So responsiveness is media queries, mobile-first is already assuming a mobile device and then implementing "larger-size" features after.

<div class="head">

## How is responsive design different from adaptive design?

</div>

Responsive design is about flexibility, where you have a single fluid website that looks good on any device. **Adaptive design** is similar to **progressive enhancement**, where instead of one flexible design, you detect the device and provide appropriate features and layout based on a predefined set of viewport sizes and other characteristics.

<div class="head">

## Can you explain object-oriented CSS?

</div>

The idea of **OOCSS** is to treat page elements as objects, giving all of these objects classes, and treating the single entities in style sheets.

<div class="head">

## What retina techniques are you familiar with?

</div>

Retina just means **higher-resolution** screens (a **pixel ratio larger than 1**). 

Browser by default render all DOM elements according to device resolution, except for images.
So you need to use high-resolution images for retina, and use `srcset` (and optionally sizes) to let the browser determine which image is best!

<div class="head">

## Is there any reason you'd need to use translate() instead of absolute positioning or vice-versa?

</div>

`translate()` is a value of `transform` - it doesn't trigger browser **reflow** or **repaint** but does trigger **compositions**, while `absolute` positioning does trigger these things.

<div class="head">

## What are the differences between visibility hidden and display none?

</div>

`Visibility:hidden` elements take the space in the normal flow, but aren't shown.
`Display: none` completely removes the element from the normal flow and other elements fill it in.

<div class="head">

## How would you optimize CSS selectors?

</div>

* **DRY** 
* **Avoid universal (*) selectors**
* Get rid of **edundant selectors**
* Be as **specific** as possible
* Follow **BEM Methodologies**

<div class="head">

## Can you explain CSS grid?

</div>

CSS Grid is a 2-dimensional system, meaning it handles columns and rows. Flexbox by contrast is largely 1-dimensional, meaning it just addresses rows.

With Grid, you apply CSS rules to a parent "Container" and its child elements or "items".


