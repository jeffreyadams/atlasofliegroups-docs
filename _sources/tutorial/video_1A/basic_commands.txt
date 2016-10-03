Basic Commands
===============

Helpful unix tools
-------------------


One useful tool you can use is hitting the ``TAB`` key twice. Hitting it once does command completion which helps you finish a command if you don't remember how it ends. Hitting it twice does command completion on the empty string and it will tell you all possible completions::

        atlas> {TAB,TAB}
        Display all 204 possibilities? (y or n)

Here the curly brackets mean a comment. In this case it means that you
hit the key in question instead of typing the word. Now, when you type
``y`` it will display all the 204 commands in the software using more,
so you can scroll through them to find the command you need. 

You can also use ``TAB`` to find more than one possible command completions. For
example, typing ``nu`` and then ``TAB`` completes to null. Typing
``TAB`` again gives the possible commands that start with null::

   atlas> nu{TAB}
   atlas> null
   {TAB}
   null         null_module
   atlas> null

If this does not work on your version of ``atlas`` it may be that the appropriate ``readline`` library is not installed on your computer: command completion is implemented by ``readline``. Addressing this problem is worth the effort!

Another useful unix command is ``ctrl-p`` which helps you find the previous command you typed. For example::

   atlas> set y=2
   Identifier y: int
   atlas> {ctrl-p}
   atlas> set y=2

So, you can easily scroll back to the previous commands that you have typed by repeating this step. This is also useful for editing the commands without having to type them all again, as we could do in the above example by changing ``y=2`` to ``y=3`` after recalling our previous command.

The same result can be obtained by hitting the up/down arrow keys. This also lets you scroll forward as well as backward.

The commands ``ctrl-a`` and ``ctrl-e`` move you to the start and end of a line respectively and the command ``option-left/right-arrow`` move you left or right to the start/end of the next word. 

Basic ``atlas`` Operations
---------------------------


``atlas`` also performs operations on non-integers and outputs integers or integer tuples. For example you could ask the software to round down to the the largest integer less than a number, to compute the remainder, or to exppress a rational as a pair:: 

	  atlas> x:=13
	  Value: 13
	  atlas> x\5
	  Value: 2
	  atlas> x%5
	  Value: 3
	  atlas> z:=x/5
	  Value: 13/5	
	  atlas> %z
	  Value: (13,5)

We can also work with each part of the pair separately::

   atlas> set s=%z
   Identifier s: (int,int)
   atlas> set (num,denom)=s
   Identifiers num: int, denom: int
   atlas> num
   Value: 13
   atlas> denom
   Value: 5
   atlas> 


n-tuples
---------

The above pair of integers belongs to the more general data type,
tuples, which could consist of integers, rationals, vectors, strings
or a combination of a variety of data types. A string can be any
string of characters in quotes such as::

    atlas> set x="hello world"
    Identifier x: string
    atlas> x
    Value: "hello world"
    atlas> print(x)
    "hello world"
    Value: "hello world"
    atlas> prints(x)
    hello world
  

Here we use the command ``prints`` which means print string, to print
without quotes. 

Now we can form the 3-tuple of different data types::

   set z=(1,2/3,x)
   Identifier z: (int,rat,string)
   atlas> z
   Value: (1,2/3,"hello world")


