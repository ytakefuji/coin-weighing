# coin-weighing
Coin weighing puzzles are intractable for human. They are easily solved by an AI-based system. The goal of this repository is to demonstrate the latest approach with AI inference embedded without human intelligence. 12balls-v2.py is a simple program with 50 lines. The program is composed of three parts: generating states, generating experiments using pseudorandom number, and verifying the satisfactory conditions. Human intelligence can be replaced by the proposed system.

In orde to run the program, type
$ python 12balls-v2.py

One of solutions in 1000 trials is:
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
