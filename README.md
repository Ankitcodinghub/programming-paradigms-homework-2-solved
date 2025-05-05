# programming-paradigms-homework-2-solved
**TO GET THIS SOLUTION VISIT:** [Programming Paradigms Homework 2 Solved](https://www.ankitcodinghub.com/product/programming-paradigms-homework-2-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100196&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Programming Paradigms Homework 2 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
1 Discrete lines and spaces

In this assignment you will need to implement the tools for working with discrete lines and discrete 2D spaces with a focused point. You can think of a discrete line as a tape (e.g., like one used in Turing machine).

1.1 Lines

A discrete line consists of a point (cell) in focus and a (possibly infinite) list of cells to the left and to the right of it:

— | A line with a focus.

— Line xs y zs represents a descrete line:

— * xs represents all elements to the left (below) — * y is the element in focus

— * zs represents all elements after (above)

data Line a = Line [a] a [a]

deriving (Show) — required to enable printing A simplest example of a line is the integer numbers:

<pre>-- | A line of integers with focus at 0.
</pre>
<pre>integers :: Line Integer
integers = Line [-1, -2..] 0 [1, 2..]
</pre>
To be able to print lines, we need to be able to select finite portions: Exercise 1.1 (⋆). Implement the following functions:

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
— | Keep up to a given number of elements in each direction in a line. — cutLine 3 integers = Line [-1,-2,-3] 0 [1,2,3]

cutLine :: Int -&gt; Line a -&gt; Line a

Exercise 1.2 (⋆). Implement the following function:

— | Generate a line by using generating functions.

— (genLine f x g) generates a line with x in its focus,

— then it applies f to x until reaching Nothing to produce — a list of elements to the left of x,

— and, similarly, applies g to x until reaching Nothing to — produce a list of elements to the right of x.

genLine :: (a -&gt; Maybe a) -&gt; a -&gt; (a -&gt; Maybe a) -&gt; Line a

Exercise 1.3 (⋆). Implement the following function:

— | Apply a function to all elements on a line.

— mapLine (^2) integers = Line [1, 4, 9, ..] 0 [1, 4, 9, ..] mapLine :: (a -&gt; b) -&gt; Line a -&gt; Line b

Exercise 1.4 (⋆⋆). Implement the following functions:

— | Zip together two lines.

— zipLines integers integers

— = Line [(-1,-1),(-2,-2),..] (0,0) [(1,1),(2,2),..] zipLines :: Line a -&gt; Line b -&gt; Line (a, b)

— | Zip together two lines with a given combining function. — zipLinesWith (*) integers integers

— = Line [1,4,9,..] 0 [1,4,9,..]

zipLinesWith :: (a -&gt; b -&gt; c) -&gt; Line a -&gt; Line b -&gt; Line c

1.2 Rule 30

In this subsection you need to implement Rule 30 cellular automaton1 using our definition of discrete lines.

When working with a cellular automaton, you need to figure out the next state for each cell simultaneously. However, start by considering only the cell in focus:

Exercise 1.5 (⋆). Implement the following function, computing the next state of the cell in focus, according to Rule 30:

<pre>data Cell = Alive | Dead
  deriving (Show)
</pre>
rule30 :: Line Cell -&gt; Cell

Now, we need tools to allow us to focus on all cells.

Exercise 1.6 (⋆). Implement the following functions, shifting the focus on the line by one position (if possible):

<pre>shiftLeft  :: Line a -&gt; Maybe (Line a)
shiftRight :: Line a -&gt; Maybe (Line a)
</pre>
Now that we can shift by one position, we can shift repeatedly, to reach each cell on the line. In fact, we can get an entire line of different focus shifts:

Exercise 1.7 (⋆⋆). Implement the following function:

lineShifts :: Line a -&gt; Line (Line a) 1see https://en.wikipedia.org/wiki/Rule_30

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Now, we can simply apply rule30 to each cell: applyRule30 :: Line Cell -&gt; Line Cell

applyRule30 line = mapLine rule30 (lineShifts line) Now let’s add some visualization:

Exercise 1.8 (⋆⋆). Implement the following functions: — | Render a line of 1×1 pictures.

<pre>renderLine :: Line Picture -&gt; Picture
</pre>
— | Render the fist N steps of Rule 30,

— applied to a given starting line. renderRule30 :: Int -&gt; Line Cell -&gt; Picture

1.3 Discrete spaces

A discrete 2D space can be represented by a (vertical) line of (horizontal) lines:

— | A descrete 2D space with a focus.

— A 2D space is merely a (vertical) line

— where each element is a (horizontal) line. data Space a = Space (Line (Line a))

Exercise 1.9 (⋆ ⋆ ⋆). Implement the following function, computing the cartesian product of two lines to produce a 2D space:

productOfLines :: Line a -&gt; Line b -&gt; Space (a, b) Exercise 1.10 (⋆⋆). Implement the following utility functions:

<pre>mapSpace :: (a -&gt; b) -&gt; Space a -&gt; Space b
zipSpaces :: Space a -&gt; Space b -&gt; Space (a, b)
zipSpacesWith :: (a -&gt; b -&gt; c) -&gt; Space a -&gt; Space b -&gt; Space c
</pre>
Exercise 1.11 (⋆⋆). Implement the following utility functions:

<pre>mapSpace :: (a -&gt; b) -&gt; Space a -&gt; Space b
zipSpaces :: Space a -&gt; Space b -&gt; Space (a, b)
zipSpacesWith :: (a -&gt; b -&gt; c) -&gt; Space a -&gt; Space b -&gt; Space c
</pre>
1.4 Conway’s Game of Life

Here you need to implement Conway’s Game of Life by using our definition of discrete space. Start by implementing the main rule of the automaton:

Exercise 1.12 (⋆). Implement the following function, computing the next state of the cell in focus, according to the rules of Conway’s Game of Life:

<pre>data Cell = Alive | Dead
  deriving (Show)
</pre>
conwayRule :: Space Cell -&gt; Cell

Since we already can shift focus in lines, we can also shift focus in space. In fact, we can get an

entire space of different focus shifts:

Exercise 1.13 (⋆ ⋆ ⋆). Implement the following function: spaceShifts :: Space a -&gt; Space (Space a)

Now, we can simply apply conwayRule to each cell: 3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<pre>applyConwayRule :: Space Cell -&gt; Space Cell
applyConwayRule space = mapSpace conwayRule (spaceShifts space)
</pre>
Now let’s add some visualization:

Exercise 1.14 (⋆⋆). Implement the following functions:

<pre>-- | Render a space of 1x1 pictures.
</pre>
<pre>renderSpace :: Space Picture -&gt; Picture
</pre>
— | Animate Conway’s Game of Life, — starting with a given space

— and updating it every second. animateConway :: Space Cell -&gt; IO ()

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
