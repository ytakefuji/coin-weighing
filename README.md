# coin-weighing
Coin weighing puzzles are intractable for human. They are easily solved by an AI-based system. 
The goal of this repository is to demonstrate the latest approach with AI inference embedded without human intelligence. 
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
