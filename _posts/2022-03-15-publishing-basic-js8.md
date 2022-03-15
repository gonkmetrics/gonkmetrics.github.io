## Introduction to JS ES6

JS's ECMAScript 6 revision has additional features over earlier revisions of JS to bring it in line with other programming languages.

* var Keyword in JS
* let Keyword
* const Keyword
* Declaring Functions

---
<br>
# var Keyword in JS

The standard keyword for declaring variables in JS *var* has three quirks: it has global scope, is hoisted on runtime, and can be re-declared ("duplicated") outside of it's local block.

A JS variable declared with keyword var can be declared again:
<pre><code class="language-javascript">var x=1;

var x = 100;

console.log(x);
</code></pre>

>Output:
>>100

All variables declared with var have global scope:
<pre><code class="language-javascript">var x = 1;
console.log(x);
if (true) {
var x = 10;
console.log(x);
}
console.log(x);
</code></pre>

>Output:
>>1
>>10
>>10

The same behavior persists with different types of code blocks (for(){}, blank curly brackets {}, etc.)

Lastly, any variables declared with the var keyword are hoisted **and initialized**, other declarations are only hoisted until initialized.
<pre><code class="language-javascript">console.log(x);
x = 1;
var x = 1;
</code></pre>

>Output:
>>1

---
<br>
# let Keyword

ES6 introduces the *let* keyword, of which variables declared with *let* behave like variables in other C-family languages.

Unlike var:
<ul>
<li>*let* cannot be re-declared</li>
<li>*let* has local scope, within its own block</li>
<li>*let* is hoisted but not initialized until it is directly done so in code</li>
</ul>

Syntax:
<pre><code class="language-javascript">let bar = 123;
</code></pre>

---
<br>
# const Keyword

ES6 introduces the *const* keyword, which has the same behavior as *let*, but declares constants. This is similar to the behavior of the *final* keyword in Java.

Syntax:
<pre><code class="language-javascript">const foo = 1;
</code></pre>

Constants may not be declared empty in JS.

---
<br>
# Declaring Functions

As observed previously, functions can be saved to variables, which can then be used in constructors or as methods:

<pre><code class="language-javascript">        var foo = function(){
                return 1;
        }

        //constructor
        new foo(); // => foo {}

        //method
        var obj = {ddd:foo};
        obj.ddd();
        console.log(obj);
</code></pre>

Another feature of JS are arrow functions, which act as shorthand for the *function* keyword.

They are written in the syntax:
> VARIABLE = (INPUTS) => [FUNCTION;]

E.x. 1:
<pre><code class="language-javascript">        const plus = (x,y) => {return x+y};
        *is shorthand for*
        const plus = function (x,y) {return x+y;}
</code></pre>

E.x. 2: Note the function receives *null*.
<pre><code class="language-javascript">        const hello = () => {return "hello";}
        *is shorthand for*
        var hello = function(){return "hello";}
</code></pre>


-gonkgonk
