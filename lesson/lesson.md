# Methods 2 Lesson: Algorithms

## [Slides](lesson.pdf)

## Context
* **Javascript Programming course, 11th grade**
* **AIM:** How do we create and implement an algorithm?
* **Prior knowledge:** Students should have experience with:
  * JS fundamentals: strings, arrays, functions, conditionals, loops
* **Standard(s):** 
  * 9-12.CT.8: Develop a program that effectively uses control structures in order to create a computer program for practical intent, personal expression, or to address a societal issue.
  * 9-12.CT.5 Modify a function or procedure in a program to perform its computation in a different way over the same inputs, while preserving the result of the overall program.

---

## Warmup
Discussion question: what is the difference between "algorithm" and "code"? Or are they the same? Or is there overlap?

---

## Mini-lesson
Transition: "algorithm" and "code" aren't exactly the same thing, but they are certainly related! In this lesson, we will unpack how they overlap.

Let's consider the following task:

> [TwoTwo](https://the-winter.github.io/codingjs/exercise.html?name=twoTwo&title=Array-2): given an array of ints, return true if every 2 that appears in the array is next to another 2.

Here is a general template for approaching a task such as this:
* Understand the problem
* Write pseudocode for an algorithm to solve the problem
* Turn the pseudocode into actual code
* Revise as necessary
  * Errors --> debug
  * No errors --> refactor for efficiency

Now let's unpack this with the TwoTwo example:

### Understand the problem

Let's consider both examples and non-examples:

`twoTwo([4, 2, 2, 3])` returns `true` because both `2`s are next to each other

`twoTwo([2, 2, 4])` returns `true` because both `2`s are next to each other

`twoTwo([2, 2, 4, 2])` returns `false` because the `2` at the end does not have a `2` next to it

### Write pseudocode for an algorithm to solve the problem

* Let's lok for "scenarios" that would return `false`, otherwise assume all good (return `true`)
* Only look for `2`s, then look at neighbors of `2`s
  * Check first and last since those are special cases (only one neighbor)
  * Check inside (everything with two neighbors)

### Turn the pseudocode into actual code

```js
function twotwo(nums) {
    // first is 2, second isn't 2
    if(nums[0] == 2 && nums[1] != 2) {
        return false;
    }
    // last is 2, second-to-last isn't 2
    if(nums[nums.length-1] == 2 && nums[nums.length-2] != 2) {
        return false;
    }

    // check each inside (and the one after it)
    for(var i = 1; i < nums.length-1; i++) {
        if(nums[i] == 2 && nums[i+1] != 2) {
            return false;
        }
    }

    return true;
}
```

### Revise as necessary

#### Error
`twoTwo([4, 2, 2, 3])` _should_ return `true` but my code returns `false`. Why?

```js
if(nums[i] == 2 && nums[i+1] != 2)
```

only checks the number to the _right_ of the current number. But we only want to return `false` if the left **and** right neighbors of a `2` are non-`2`s. So we revise by adding another condition to our boolean expression:

```js
if(nums[i] == 2 && nums[i+1] != 2 && nums[i-1] != 2)
```

#### Refactor

The scenarios where:
* There is a 2 at the beginning
* There is a 2 at the end

can be combined with an `or` statement, although the expression is quite lengthy:

```js
if((nums[0] == 2 && nums[1] != 2) || (nums[nums.length-1] == 2 && nums[nums.length-2] != 2))
```


---

## Activity
In pairs, decide on which task to try. 
* [Tough: swapEnds](https://the-winter.github.io/codingjs/exercise.html?name=swapEnds&title=Array-1)
* [Tougher: caughtSpeeding](https://the-winter.github.io/codingjs/exercise.html?name=caughtSpeeding&title=Logic-1)
* [Toughest: tripleUp](https://the-winter.github.io/codingjs/exercise.html?name=tripleUp&title=Array-2)


Then follow the procedure:

> * Understand the problem
> * Write pseudocode for an algorithm to solve the problem
> * Turn the pseudocode into actual code
> * Revise as necessary
>   * Errors --> debug
>   * No errors --> refactor for efficiency

Ways to support students during activity:
* Ask "what concepts do you know that might apply here?"
* Provide paper where they can make sense of the problem via a diagram, table, etc.
* Provide real-world examples, i.e. swapping coffee/water
* Be ready to provide the first lines of code for each exercise:

```js
// tough
var temp = nums[0];

// tougher
if(birthday) {

// toughest
if(nums.length < 2) {
```

---

## Summary

Reflection questions:
* Did you have to change your original algorithm?
* Finished?
  * How close was your code to your algorithm?
  * Did you under/over-plan?
* Not finished?
  * Is there anything in your algorithm that you don't know how to turn into code?
