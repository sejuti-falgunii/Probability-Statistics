# Lecture 1
Probability is a mathematical framework for dealing with uncertainty (randomness). 
### What is Sample Space?
---
The set of all possible outcomes in an experiment. 
    
  >**Mutually Exclusive:** One outcome happening means others don't happen.

  >**Collectively Exhaustive:** The set includes all possible outcomes (at least one outcome must occur). 

* There can be numerous details in practical scenarios, what we consider relevant depends on our judgment, making it an art.
### When to choose sequential description?
---
Sequential Description is useful when the experiment has multiple stages (A tree-based).

<a href="https://imgbb.com/"><img src="https://i.ibb.co/68fsKgG/Untitled.png" alt="Untitled" border="0"></a>
* Sample space could be infinite. 

### What is an event?
---
The probability of hitting a specific point in this rectangle to infinite percision will be intuitively 0. (not helpful) So its better to assign probabilities to subsets of the sample space. So we can measure the probability of a event to occur or not. 
<a href="https://imgbb.com/"><img src="https://i.ibb.co/VWTvt8W/geometric-square-shape-black-background-vector-53876-177894.jpg" alt="geometric-square-shape-black-background-vector-53876-177894" border="0"></a>

### AXIOMS
Ground rules that any legitimate probabilistic model should obey
1.  $P(A) \geq 0$ for all $A \subset S$ 
2.  $P(S) = 1$
3.  If $A \cap B = \emptyset$,
    then $P(A \cup B) = P(A) + P(B)$

* Another rule is probability stays between 0 & 1.

$$1^{(2)} = P(\Omega) = P(A \cup A^c)$$
$$^{(3)}P(A) + P(A^c)$$
$$P(A)= 1 - P(A^c)≤ 1$$

### The 3rd axiom for many (finite) sample space
P(AUBUC) = P((AUB)UC)= P(AUB)+P(C) = P(A)+P(B)+P(C)
### Task1
<a href="https://imgbb.com/"><img src="https://i.ibb.co/YWNCNX9/white-concrete-paver-block-500x500.webp" alt="white-concrete-paver-block-500x500" border="0"></a>
We have a sample space and we need to assign a probability law- We let every possible outcome have the probability of 1/16

* P({X=1}) = 4/16
* P(X+Y is odd)= 8/16
* P(min(X,Y)=2)=5/16



### Discrete Uniform Law
If all outcomes be equally likely 
P(A)= $\frac{Number of elements of A}{Total number of sample points}$

Computng probabilities = counting
This defines fair coins, fair dice, well shuffled decks 
### Continuous Uniform Law
<a href="https://imgbb.com/"><img src="https://i.ibb.co/5GZp1V2/Untitled.png" alt="Untitled" border="0"></a>
Probability = Area
* P(X+Y ≤ 1/2) = 1/8
* P((X,Y)=(0.5,0.3))=0

# Lecture 2

### Concept of conditional probability
Info is always partial. 
random experiment → partial info → conditional probability
* The unit square is the union of one element set consisting of all the points. So the unit square is made up by the union of the various point inside the square

1= P(□) = P(U{(x, y)}) = Σ P ({x,y}) = Σ0 = 0

The third expression above isn't valid. It isn't a sequaence of sets; we can't exhaust the whole unit square by taking a sequence of elements inside it and cover the whole unit. Because infinite sets are not all of the same size. Continuous sets like the unit square is a bigger set (uncountable); having more sequence than any sequence could have.

* The 0 probalility means- its highly unlikely by itself. In such continuous probability models 0 probability outcomes are everything that happens. 

P((x, y) ≠ (0,0) = 1
* Probability of 1 means essential certainty it still allows the possibility that the outcome might be outside that set.
### Concept of conditional probability (Cont.)
Based on my knowledge of the world, we set up the probability model and we write down probabilities for the different outcomes.
New info → Changes belief (revising beliefs) → Conditional probabilities

<style>
.square {
  position: relative;
  width: 200px;
  height: 200px;
  background-color: yellow;
  border: 2px solid red;
  display: flex;
  align-items: center;
  justify-content: center;
}
.ellipse-x {
  position: absolute;
  width: 120px;
  height: 60px;
  background-color: orange;
  border: 2px solid black;
  border-radius: 50%;
  top: 70%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  align-items: center;
  justify-content: center;
  color: black;
}
.ellipse-y {
  position: absolute;
  width: 60px;
  height: 120px;
  background-color: coral;
  border: 2px solid black;
  border-radius: 50%;
  top: 50%;
  left: 30%;
  transform: translate(-50%, -50%);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 10px 0;
  color: black;
}
</style>
<div class="square">
  <div class="ellipse-x">
    <span>1/6</span>
  </div>
  <div class="ellipse-y">
    <span>3/6</span>
    <span>2/6</span>
  </div>
</div>

P(A|B) = probability of A, given B occurred
### Definition of Conditional Probability
P(B) = 0
P(A|B) = $\frac{P(A∩B)}{P(B)}$
P(A|B) undefined if P(B) = 0
#### Interpretetion in terms of frequency
P(A∩B) = P(B) P(A|B)

When the experment is done over and over again, what fraction of time it is going to be the case that both A and B occurs?
You only look at those experiments at which B happens to occur & what fractions of those experments where B already occurred, event A also occurs.

### Additivity Law
A∩B = ∅
P(A∩B|C) = P(A|C)+P(B|C)

<style>
.big-square {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: repeat(4, 1fr);
  width: 200px;
  height: 200px;
  gap: 2px; /* Optional: adds space between the small squares */
}

.small-square {
  background-color: lightblue;
  border: 1px solid gray;
}
</style>

<div class="big-square">
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>  
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
  <div class="small-square"></div>
</div>
X First roll
(By the Y axis, Y first roll)

* Let B be the event : min(X,Y)=2
* Let M = max(X, Y)
* P(M=1 | B) = 0
* P(M=2 | B) = $\frac{P(M=2 ∩ B)}{P(B)}$

Whenever w ehave a uiform distribution on out initial smaple space, when we condition a new event, our new distributon is still going to be uniform- but the smaller event of that we considered. 
### The model in terms of conditional probabilities
P((A∩B) P(C|A∩B)) = P(A∩B) P(C|A∩B) = P(A) P(B|A) P(C|A∩B)

### Total Probability Theorem
* divide & conquer
Partition of sample sapce into A<sub>1</sub>, A<sub>2</sub>, A<sub>3</sub>


<style>
.square {
  position: relative;
  width: 200px;
  height: 200px;
  background-color: yellow;
  border: 2px solid red;
}

.circle {
  width: 100px;
  height: 100px;
  background-color: #ccff33; /* Lemon green color */
  border-radius: 50%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.curve {
  position: absolute;
  width: 200px;
  height: 100px;
  border-top: 2px solid black;
  border-radius: 100px;
}

.curve1 {
  top: 60px;
  left: 0;
}

.curve2 {
  bottom: 20px;
  left: 0;
  transform: rotate(60deg);
}
</style>

<div class="square">
  <div class="circle"></div>
  <div class="curve curve1"></div>
  <div class="curve curve2"></div>
  
</div>
we imagine 3 areas here A<sub>1</sub>, A<sub>2</sub>, A<sub>3</sub>

## Bayes' Theorem Statement

Let $E_1, E_2, ..., E_n$ be a set of events associated with a sample space $S$, where all the events $E_1, E_2, ..., E_n$ have nonzero probability of occurrence and they form a partition of S. Let A be any event associated with S, then according to Bayes theorem,
for any $k = 1, 2, 3,...., n$

## Venn Diagram Representation

$$P(E_i | A) = \frac{P(E_i)P(A | E_i)}{\sum_{k=1}^{n} P(E_k)P(A | E_k)}$$

# Lecture 3
Bayes' rule is the trivial half line calculation. 
### Inference
A situation on which there's a bunch or lots of different hypotheses about the environment. Given any parrticular setting in the environment, I may have a measuring device that may produce many different outcomes. I can observe the final outcome with my measuring device, trying to guess which particular branch occurred. Trying to guess the state of the world with paricular measurement.

### Property Independence
Two events are independent if and only if their probability of happening simultaneously is the equal of the product of their two individual probabilities.

* Independer is something we can check formally using these definition, but also we can check intuitivelyby if, in some casesyou can reason that whatever happens, that determines A is going to occur, or not, has absolitely nothing to do with whatever happens that determines whether B is going to happen or not.

* What events happen in one experiment aren't going to change our beliefs about what might be happeningin the other, because the sources of noise in these two experiments are completely unrelevant.
### Extreme dependence disjointness
<style>
.square {
  position: relative;
  width: 200px;
  height: 200px;
  background-color: yellow;
  border: 2px solid red;
}
.circle1 {
  width: 100px;
  height: 100px;
  background-color: #ccff33; /* Lemon green color */
  border-radius: 50%;
  position: absolute;
  top: 50%;
  left: 25%;
  transform: translate(-50%, -50%);
}
.circle2 {
  width: 100px;
  height: 100px;
  background-color: orange;
  border-radius: 50%;
  position: absolute;
  top: 50%;
  left: 75%;
  transform: translate(-50%, -50%);
}
.circle1, .circle2 {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
    color: black;
}
</style>

<div class="square">
    <div class="circle1">A</div>
    <div class="circle2">B</div>
</div>
These two circles as events, are seemingly different, as they are seperate, but aren't. Info about the occurrance of A in the sample space definitely affects our beliefs on possible occurance/non-occurance of B.
If A=1/3 & B=1/4
& P(A⋂B)=0
P(A) P(B)= 1/12
& P(A|B) = 0
P(A)=1/3
### Conditional Independence
Independence defined 
P(A⋂B)=P(A) P(B)
In conditional independence
P(A⋂B|C)=P(A|C) P(B|C)
This is the definition of conditional independence.

* In a particular experiment, where A & B are independent (A⋂B≠0), and C occurred, such that C has both some parts of A & B both included. 
Here A & B both are independent and disjoint. But the info that C occurrs biases the conception in such a way that in the new model, A and B are dependent.
"Having independence in the original model doesn't imply independence in conditional model"
# Lecture 4
Counting method apply in the situations in which we have probabilistic experiments with a fintie number of outcomes- where every possible outcome of the same possibility of occurring.



![Square with Circle](figure/sqcircle.svg)













