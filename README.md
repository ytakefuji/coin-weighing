# coin-weighing
Coin weighing puzzles are intractable for human. 
According to Wikipedia, a balance puzzle or weighing puzzle is a logic puzzle about balancing items—often coins or balls—to determine which holds a different value, by using a balance scale a limited number of times. In 12-coin-3-weighing puzzle, twelve coins are given where eleven of which are identical. If one is different, we don't know whether it is heavier or lighter than the others. The balance may be used three times to determine if there is a unique (counterfeit or fake) coin to isolate it and determine its weight relative to the others. Therefore, in 12-coin-3-weighing puzzle, we have to isolate a single counterfeit coin by three weighings using the balance.

They are easily solved by an AI-based system. 
The goal of this repository is to demonstrate the latest approach with AI inference embedded without human intelligence. 
The Prolog program and Z3 programs are based on deductive method. prolog.pl and misc.pl are Prolog program. 12coins_z3.py and 24coins_z3.py are based on Z3 library.

To run prolog.pl, execute the following command:
<pre>
$ swipl -s prolog.pl -g go -t halt
</pre>
To run 12coins_z3.py, 
<pre>
$ python 12coins_z3.py
</pre>

To run Perl program odd.pl:
<pre>
$ odd.pl 12 3
or
$ odd.pl 24 4
</pre>

12coins.py is a simple program with 37 lines. 
The program is composed of three parts: generating states, generating experiments using pseudorandom number, and verifying the satisfactory conditions. 
Human intelligence can be replaced by the proposed AI system.

In orde to run the program, type the following:
<pre>
$ python 12coins.py
</pre>
One of 5 solutions in 1000 trials is generated as follows:
<pre>
[6, 5, 10, 7, 9, 2, 3, 1] [10, 4, 3, 8, 12, 7, 9, 1] [12, 2, 6, 8, 11, 10, 3, 9]
　   1      2      3      4      5      6      7      8      9      10     11     12    
L:['>>=', '>=<', '><>', '=<=', '<==', '<=<', '<>=', '=<<', '>>>', '<<>', '==>', '=><', 
H: '<<=', '<=>', '<><', '=>=', '>==', '>=>', '><=', '=>>', '<<<', '>><', '==<', '=<>']
</pre>
Access to the following web service:
https://nrich.maths.org/5796

Play with the web page. The first experiment is to use 4 coins (6, 5, 10, 7) on the left side and 4 coins (9, 2, 3, 1) on the right side.
The result of weighing coins in a balance scale shows three states: <, =, or > where < indicates that the right side is heavier, = for balanced, > the left side is heavier.
In the second experiment, use 4 coins (10, 4, 3, 8) on the left and 4 coins (12, 7, 9, 1) on the right side.
In the third experiment, use 4 coins (12, 2, 6, 8) and 4 coins (11, 10, 3, 9).
For example, if the result of three experiments is '>=<', then it shows that coin#2 is lighter.

For 13-coin weighing puzzle, you can use the following solution generated by 13balls.py
<pre>
[3, 2, 8, 9, 7, 12, 5, 1] [11, 4, 12, 3, 2, 10, 7, 5] [4, 8, 12, 1, 11, 6, 5, 3]
　   1      2      3      4      5      6      7      8      9      10     11     12     13
L:['>=<', '<>=', '<<>', '=<<', '>>>', '==>', '>>=', '<=<', '<==', '=>=', '=<>', '><<', '===', 
H: '<=>', '><=', '>><', '=>>', '<<<', '==<', '<<=', '>=>', '>==', '=<=', '=><', '<>>', '===']
</pre>

In 13-coin weighing puzzle, 12 coins can be detected whether it is lighter or heavier, but one coin can be only detected without information of lighter or heavier.


For 24 coins by 4 weighing, the solution is the following:
<pre>
[19, 22, 11, 21, 12, 7, 3, 13, 5, 14, 8, 4, 24, 2, 6, 23]
[24, 16, 8, 4, 1, 21, 20, 15, 7, 5, 13, 18, 17, 2, 14, 11]
[19, 6, 9, 14, 18, 12, 24, 5, 20, 4, 13, 1, 3, 10, 23, 8]
[16, 10, 2, 24, 8, 9, 14, 19, 12, 5, 1, 15, 22, 18, 6, 13]

   1        2       3       4       5       6       7       8       9       10      11      12      13      14      15      16
H:['=><<', '<<=>', '>=<=', '<><=', '<<=<', '<=><', '><==', '<>=>', '==>>', '==<>', '>===', '>=><', '=<<=', '<<>>', '===<', '=>=>', 
   17       18     19      20     21      22       23      24
 '=<==', '=<><', '>=>=', '=><=', '>>==', '>==<', '==<=', '<>>>']
    1        2       3       4       5       6       7       8       9       10      11      12      13      14      15      16
L:['=<>>', '>>=<', '<=>=', '><>=', '>>=>', '>=<>', '<>==', '><=<', '==<<', '==><', '<===', '<=<>', '=>>=', '>><<', '===>', '=<=<', 
   17       18     19      20     21      22       23      24
 '=>==', '=><>', '<=<=', '=<>=', '<<==', '<==>', '==>=', '><<<']
 
 </pre>
