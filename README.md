<div align="center">

## C\+\+ \- Lesson 3 : do, while, \#include, \#define


</div>

### Description

Welcome fellow programmers to our third lesson in a long series on the road to programming C++. This articles explains do, while, #include, and #define. (from http://pa.pulze.com/)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Found on the World Wide Web](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/found-on-the-world-wide-web.md)
**Level**          |Beginner
**User Rating**    |4.4 (35 globes from 8 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/found-on-the-world-wide-web-c-lesson-3-do-while-include-define__3-419/archive/master.zip)





### Source Code

<p><b style="FONT-WEIGHT: bold">Beginners C++ - Lesson 3</b>&nbsp;&nbsp;&nbsp;<br>
<b style="FONT-WEIGHT: bold">Instructor</b>:&nbsp;&nbsp; Paul C. Benedict, Jr. (<u><span style="COLOR: #0000ff">PCC
PaulB</span></u>)&nbsp;&nbsp;&nbsp;<br>
</p>
<h2>Color coded text:</h2>
<p><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp; black&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
New things to Remember</b><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp;
blue&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; C++
keywords (do, while)</b></span><br>
&nbsp;&nbsp;&nbsp; <span style="COLOR: #008800"><b style="FONT-WEIGHT: bold">green&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
C++ preprocessor directives (#include, #define)</b></span></p>
<p><br>
<u><span style="FONT: bold 18pt/21pt Geneva"><b><i>Section 3.1</i></b></span></u>&nbsp;&nbsp;<br>
Welcome fellow programmers to our third lesson in a long series on the road to
programming C++. Just like the real roads we travel on, they are not all big one
straight line. Just imagine how boring driving would be if you were you limited
to one flow of direction. Just imagine how boring programs would be if it
couldn't branch off and make decisions. Every time you ran the program it would
be the same, and that would just depress us all, wouldn't it? :-)&nbsp;&nbsp;&nbsp;</p>
<p>We are going to learn that programs run in one big loop. Every program begins
in a loop, and branches off to smaller loops, and smaller, etc. We will begin
studying what kind of loops C++ support, practice when and when not to use
certain types of loops, and find common mistakes. All that great boolean algebra
we learned will yet appear again as we learn how to control our loops!&nbsp;&nbsp;&nbsp;</p>
<p>C++ supports these types of branching mechanisms:&nbsp;&nbsp;&nbsp;<br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">case</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">default</b></span>&nbsp;&nbsp;&nbsp;</p>
<p>C++ supports these types of loops:&nbsp;&nbsp;&nbsp;<br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">do</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while</b></span>&nbsp;&nbsp;&nbsp;</p>
<p>You can make decisions using these special operators:&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; Less-than&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&lt;&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; Greater-than&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&gt;&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; Less-than or equal to&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&lt;=&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; Greater-than or equal to&nbsp;&nbsp;&nbsp; &gt;=&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; Equal to&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
==&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; Not equal to&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
!=&nbsp;&nbsp;&nbsp;</p>
<p>We will use these operators in making decisions to what the program should do
next. These set of operators are called &quot;Rational and Equality
Operators&quot; and compare the value on the left to the value on the right.
These evaluate to a <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">bool
</b></span>value which is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>or <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>.<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp;</b></span><br>
&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.1.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool equal = (5 &lt; 3);&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
the variable <i>equal </i>gets assigned the value <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false
</b></span>because 5 is defined to be greater than 3 by our math system.&nbsp;&nbsp;&nbsp;</p>
<p><br>
</p>
<h1><u><i>Section 3.2</i></u></h1>
<p>The most simplest form of control loop is the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>
keyword. The syntax for this keyword is as follows:&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
(</b></span> <i>expression</i> <b style="FONT-WEIGHT: bold">)</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement1</i>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else</b></span>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement2</i>&nbsp;&nbsp;&nbsp;</p>
<p>The <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if </b></span>keyword
executes <i>statement1 </i>if expression is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>(nonzero); if <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else
</b></span>is present and <i>expression </i>is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false
</b></span>(zero), it executes <i>statement2</i>. After executing <i>statement1 </i>or
<i>statement2</i>, control passes to the next statement.&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.2.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; if ( i &gt; 0 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = y / i;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 0;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
In this example, the statement <i>x = y / i;</i> is executed if <i>i </i>is
greater than 0. If <i>i </i>is less than or equal to 0, <i>x </i>is assigned the
value of 0. Note that the statement forming the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause does not end with a semicolon. Note that again so you don't
forget.&nbsp;&nbsp;&nbsp;</p>
<p>Let's look at a more complex example where we want to do more than one
statement depending on how if the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause evaluates.&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.2.2</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; if ( i &gt;= 5 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 4 * i;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i++;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 5;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
In this example, the statements <i>x= 4 * i;</i> and<i> i++;</i> are executed if
<i>i </i>is greater than or equal to 5. If <i>i </i>is less than 5, <i>i </i>is
assigned the value 5. Note that how we grouped our statement in braces <b style="FONT-WEIGHT: bold">{
}</b> to indicate two or more statements that need to be executed if the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause evaluates to be <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>(nonzero).&nbsp;&nbsp;&nbsp;</p>
<p>Now the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else </b></span>clause
does not need to be included if you don't have any optional functionality you
need to be performed. It is perfectly legal to do this:&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.2.3</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; if ( i &gt;= 5 )</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 4 * i;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i++;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.2.4</b></span><br>
But what if we wanted to evaluate many cases? We will have to use a nested <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>
statement to accomplish this. Let's say we wanted to perform a separate action
when <i>i </i>is 0, 1, 2, 3, 4, 5. This is how it would be coded:&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; if ( i == 0 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( i == 1 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( i == 2 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 4;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( i == 3 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 8;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( i == 4 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 16;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( i == 5 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 32;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: bold 14pt/17pt Geneva"><b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</b></span><br>
If <i>i </i>is 0, <i>x</i> is assigned 1, then control jumps to the end of our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause.&nbsp;&nbsp;&nbsp;<br>
If <i>i</i> is 1, <i>x</i> is assigned 2, then control jumps to the end of our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause.&nbsp;&nbsp;&nbsp;<br>
If <i>i </i>is 2, <i>x</i> is assigned 4, then control jumps to the end of our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause.&nbsp;&nbsp;&nbsp;<br>
If <i>i </i>is 3, <i>x</i> is assigned 8, then control jumps to the end of our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause.&nbsp;&nbsp;&nbsp;<br>
If <i>i </i>is 4, <i>x</i> is assigned 16, then control jumps to the end of our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause.&nbsp;&nbsp;&nbsp;<br>
If <i>i </i>is 5, <i>x</i> is assigned 32, then control jumps to the end of our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause.&nbsp;&nbsp;&nbsp;</p>
<p>For you math gurus out there, can you see what is happening to <i>x</i>
depending on the value of <i>i </i>in Example 3.2.4? If anyone noticed the
simple pattern, you would see we are calculating the powers of 2, using <i>i </i>as
our exponent. We will go back to this example many times and show you different
methods of doing this.&nbsp;&nbsp;&nbsp;</p>
<p><br>
</p>
<h1><u><i>Section 3.3</i></u></h1>
<p>Now just imagine if we wanted to get the answer of 2 to some variable, which
is <i>i</i>,&nbsp; in C++<i>.</i> C++ does not have an exponent operator, so we
would have to have to have huge and ugly code like Example 4 in Section 3.2.
Fortunately, we can loop to find answers to complex problems like the 2 to the <i>i</i>-th
power. This brings us to our third new keyword in our lesson. The <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
</b></span>keyword has the syntax as follows:&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
(</b></span> <i>init_expr</i><b style="FONT-WEIGHT: bold">;</b> <i>cond_expr</i><b style="FONT-WEIGHT: bold">;</b>
<i>loop_expr </i><b style="FONT-WEIGHT: bold">)</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement</i>&nbsp;&nbsp;&nbsp;</p>
<p>For even a simpler syntax of the for loop, remember this:&nbsp;&nbsp;&nbsp;</p>
<p><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp; for ( </b><i>step1</i><b style="FONT-WEIGHT: bold">;</b>
<i>step2</i><b style="FONT-WEIGHT: bold">;</b> <i>step4</i><b style="FONT-WEIGHT: bold"><i>
)</i></b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>step3</i><b style="FONT-WEIGHT: bold">;</b>&nbsp;&nbsp;&nbsp;</p>
<p>Wow! This is alot to digest, so lets break apart each expression and look at
each one individually:&nbsp;&nbsp;&nbsp;<br>
<i>&nbsp;&nbsp;&nbsp;</i><br>
1. The first thing that happens when a <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
</b></span>loop is encountered is the <i>init_expr </i>expression is evaluated. <i>init_expr
</i>is most commonly used to initialize a variable which will control the loop.&nbsp;&nbsp;&nbsp;<br>
2. Next <i>cond_expr </i>is evaluated. This expression is a conditional
expression, which determines if the loop will continue going or not. If <i>cond_expr
</i>evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true </b></span>(nonzero),
the loop continues. If <i>cond_expr </i>is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false
</b></span>(zero), control passes to the statement following the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
</b></span>loop.&nbsp;&nbsp;&nbsp;<br>
3. <i>statement </i>is executed.&nbsp;&nbsp;&nbsp;<br>
4. <i>loop_exr </i>is than evaluated, and goes back to step 2.&nbsp;&nbsp;&nbsp;</p>
<p>Notice that after <i>loop_expr </i>there is no semicolon!&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.3.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; for ( int i = 1; i &lt;=
10; i++ )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x *= 2;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
Let's go through the steps of this <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
</b></span>loop:&nbsp;&nbsp;&nbsp;<br>
1. First the <i>i </i>variable is created and initialized to 1.&nbsp;&nbsp;&nbsp;<br>
2. Next <i>i &lt;= 10;</i> is evaluated next. Since <i>i </i>is 1 and is less
than 10, it evaluates <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>and we enter the loop and execute <i>x *= 2;</i>.&nbsp;&nbsp;&nbsp;<br>
3. Next we increment i with our loop expression, <i>i++;</i>.&nbsp;&nbsp;&nbsp;<br>
4. Next <i>i &lt;= 10;</i> is evaluated next. Since <i>i </i>is 2 and is less
than 10, it evaulates <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>and we enter the loop and execute <i>x *= 2;</i>.&nbsp;&nbsp;&nbsp;<br>
5. Next we increment i with our loop expression, <i>i++;.</i>&nbsp;&nbsp;&nbsp;<br>
6. We continue this process until our conditional expression, <i>i &lt;= 10;</i>
evaluates for <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
and we exit the loop. This happens when <i>i </i>increments to 11.&nbsp;&nbsp;&nbsp;</p>
<p>Look at what we did! We just compacted that ugly <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>
clauses into a <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for </b></span>loop
and we got the value of 2 to the 10th power, which is 1024! Now that surely
beats the latter.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.3.2</b></span><br>
But say we didn't wanted to calculate 2 to the 10th power, we wanted to
calculate 2 to the <i>n</i>th power? We could go back and modify the example as
follows:&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int n = 5;&nbsp;&nbsp;&nbsp;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; for ( int i = 1; i
&lt;= n; i++ )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x *= 2;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
Remember that when you do programming with integers, the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">int
</b></span>data type can only hold 16-bits or 32-bits (or even 64-bits)
depending on what bit compiler you use. So if we are using a 32-bit compiler, <i>n
</i>being set to 19 would be safe because we have 32-bits (0 through 31) to work
with. If we were working on a 16-bit compiler, 19 would overflow us and <i>x </i>would
be complete junk to us.&nbsp;&nbsp;&nbsp;</p>
<p>Remember our &quot;bug&quot; term from the last lesson? This unexpected
overflow is one type of bug which can make a program spit out junk, even though
the logic and the program is perfectly fine. Watch out for sneaky things like
this.&nbsp;&nbsp;&nbsp;</p>
<p><br>
</p>
<h1><u><i>Section 3.4</i></u></h1>
<p>Usually the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for </b></span>loop
is used when we want to iterate through a list of numbers. In Example 2 of
Section 3.3, we went from 1 to <i>n</i>. Sometimes there is nothing to iterate
and just want to keep on looping while a condition is true. This brings us to
the next kind of loop, called the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while
</b></span>loop. The syntax for <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while
</b></span>loop is as follows:&nbsp;&nbsp;&nbsp;</p>
<p><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp; while (</b> <i>expression </i><b style="FONT-WEIGHT: bold">)</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement</i>&nbsp;&nbsp;&nbsp;</p>
<p>The <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while </b></span>keyword
executes statement while <i>expression </i>is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true
</b></span>(nonzero).&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.4.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool p = false;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 0;&nbsp;&nbsp;&nbsp;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; while ( !p )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x++;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; p = (x
&gt; 20);&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x++;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
This <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while </b></span>loop
does not terminate until <i>p </i>becomes <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.
When<i> p </i>is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>,
the expression <i>!p</i> evaluates to <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">false</b></span>,
terminating the loop, then increments <i>x</i> one last time.&nbsp;&nbsp;&nbsp;</p>
<p>The variable <i>p</i> that controls this loop isn't very good at describing
what it does. Welcome to the world of good variable names! You have became
advanced enough to give good variable names. This has many advantages like not
having to guess at what a variable does. This is a much better example:&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.4.2</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; bool IsXGreaterThan20 =
false;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 0;&nbsp;&nbsp;&nbsp;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; while (
!IsXGreaterThan20 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x++;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
IsXGreaterThan20 = (x &gt; 20);&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; x++;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
Going back to our &quot;2 to the <i>n</i>-th power&quot; example, we can use a <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while
</b></span>loop to do the same thing as the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
</b></span>loop did. (The <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for
</b></span>loop is more appropriate for this kind of situation, so you should
stick with that). Just remember these two simple rules:&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; 1. Use <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for</b></span>
when wanting to iterate a range of values.&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; 2. Use <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while</b></span>
when you want to loop while a condition is <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">true</b></span>.&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.4.3</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int n = 5;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int i = 1;&nbsp;&nbsp;&nbsp;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; while ( i &lt;= n )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x *= 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i++;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;</p>
<h1><u><i>Section 3.5</i></u></h1>
<p>Sometimes, it might not always be appropriate for a loop to test its
condition at the beginning of the loop, like the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while
</b></span>loop. If you want to enter the loop and then check at the end, we use
the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">do</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while
</b></span>loop. The syntax for the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">do</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while</b></span>
loop is as follows:&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">do</b></span>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement</i>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while
(</b></span> <i>expression</i><b style="FONT-WEIGHT: bold"><i> </i>);</b>&nbsp;&nbsp;&nbsp;</p>
<p>This works just like the while loop, except the evaluation of the expression
comes at the end. This kind of loop ensures the statement will be executed at
least one time. Therefore, we do not need to go in-depth on this section.&nbsp;&nbsp;&nbsp;</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.5.1</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int y = 0;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; int x = 10;&nbsp;&nbsp;&nbsp;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; do&nbsp;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
y = x + 5;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x--;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; } while ( x &gt; 0 );&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
The loop is entered. then <i>y </i>gets added <i>x + 5</i>, then <i>x </i>gets
decremented. This loop continues running until <i>x </i>is no longer greater
than 0. So <i>y </i>gets added 15, then 14, 13, 12, ... until 6.&nbsp;&nbsp;&nbsp;</p>
<p><br>
</p>
<h1><u><i>Section 3.6</i></u></h1>
<p>The last and final control statement in C++ is the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">case</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">default</b></span>
trio. This is the syntax:&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch
( </b></span><i>expression </i><b style="FONT-WEIGHT: bold">)</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; <b style="FONT-WEIGHT: bold">{</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">case
</b></span><i>constant_expression</i><b style="FONT-WEIGHT: bold">:</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp; <b style="FONT-WEIGHT: bold">&nbsp; ...</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement</i>&nbsp;&nbsp;&nbsp;<br>
&nbsp; <b style="FONT-WEIGHT: bold">&nbsp; ...</b>&nbsp;&nbsp;&nbsp;<br>
<b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp; default:</b>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <i>statement</i>&nbsp;&nbsp;&nbsp;<br>
&nbsp;&nbsp;&nbsp; <b style="FONT-WEIGHT: bold">}</b>&nbsp;&nbsp;&nbsp;</p>
<p>We use this when we want a more readable form of an <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>statement. <i>constant_expression </i>must be an <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">int
</b></span>value like 2, 3, -6, but not a variable or a floating point number.
It cannot be a variable because as the word implies, it varies. It cannot be a
floating point, because computers can't represent fractions perfectly, which
would mess up the case.&nbsp;&nbsp;&nbsp;</p>
<p>A <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">case </b></span>is
just like if the code read, <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
(</b></span> <i>expression </i><b style="FONT-WEIGHT: bold">==</b> <i>case </i><b style="FONT-WEIGHT: bold">)</b>,
but much more readable. You can think of <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">default:</b></span>
as being the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else </b></span>clause
also.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.6.1</b></span><br>
Watch how we convert the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if
</b></span>clause to the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch
</b></span>clause:<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; if ( x == 2 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( (x == 3) || (x
== 5) || (x == 7) )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else if ( (x == 4) || (x
== 9) )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 3;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; else&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 4;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
can be transformed into<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; switch ( x )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; case 2:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
break;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; case 3, 5, 7:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
break;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; case 4, 9:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 3;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
break;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; default:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 4;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
Now isn't that much easier to understand? Notice the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">break</b></span><i>;
</i>statement. This &quot;breaks&quot; us out of the <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch
</b></span>clause and we continue execution outside of it. If we did not have <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">break</b></span><i>;</i>,
the next statement would keep on executing until it hits the ending right brace <b style="FONT-WEIGHT: bold">}</b>.</p>
<p><span style="FONT: bold 10pt/13pt Geneva"><b>Example 3.6.2</b></span><br>
Here is an example of the problem stated above:<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; switch ( x )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; {&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; case 2:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; case 3, 5, 7:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; default:&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 4;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp; }&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
Oh no! if <i>x </i>is 2, then it will assign <i>i </i>to 1, then 2, then 4! We
don't want this, so we must put our <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">break</b></span><i>;</i>
statement in there to prevent this from happening. This is another peculiar bug
which can creep into your code.&nbsp;&nbsp;&nbsp;</p>
<p><br>
</p>
<h1><u><i>New terms to remember</i></u></h1>
<p>Bug<br>
Clause<br>
Condition<br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">default&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">do&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">for&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>&nbsp;&nbsp;&nbsp;<br>
Loop<br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch&nbsp;&nbsp;&nbsp;</b></span><br>
<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">while</b></span>&nbsp;&nbsp;&nbsp;</p>
<p><br>
</p>
<h1><u><i>Review problems</i></u></h1>
<p>01. Find the bug:&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int x = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
if ( x = 0 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 3;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
else&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 4;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
02. Why doesn't this program ever make y equal to 3 when x is 0?&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int x = 0;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int y = 0;&nbsp;&nbsp;&nbsp;</span></p>
<p><span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
if ( x == 0 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
{</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 1;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
y = 3;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
}&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
else&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
x = 3;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
y = 1;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
03. Write a for loop which will sum all the numbers from 1 to 20.&nbsp;&nbsp;&nbsp;</p>
<p>04. Why doesn't this loop ever end?&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
int n = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
while ( n &lt;= 3 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
{&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
n *= 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
n -= 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
}&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;<br>
05. Convert this <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">else</b></span>..<span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">if</b></span>
clause into an easier reading <span style="COLOR: #0000ff"><b style="FONT-WEIGHT: bold">switch
</b></span>clause:&nbsp;&nbsp;&nbsp;<br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
if ( (x == 0) || (x == 3) )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i++;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
else if ( x == 2 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i *= 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
else if ( (x == 6) || (x == 4) || (x == 5) )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = i + 5 % i;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
else if ( x == 1 )&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = 2;&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
else&nbsp;&nbsp;&nbsp;</span><br>
<span style="FONT: 10pt/13pt Geneva">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
i = x;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>
06. Write a loop that sums every odd number from 1 to 255. There are two
possible ways of doing this, do both.</p>

