<!-- Output copied to clipboard! -->

<!-----

You have some errors, warnings, or alerts. If you are using reckless mode, turn it off to see inline alerts.
* ERRORs: 0
* WARNINGs: 0
* ALERTS: 9

Conversion time: 1.433 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β34
* Wed Apr 19 2023 12:05:51 GMT-0700 (PDT)
* Source doc: Greedy Algorithm
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!


WARNING:
You have 4 H1 headings. You may want to use the "H1 -> H2" option to demote all headings by one level.

----->


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 1; ALERTS: 9.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>
<a href="#gdcalert5">alert5</a>
<a href="#gdcalert6">alert6</a>
<a href="#gdcalert7">alert7</a>
<a href="#gdcalert8">alert8</a>
<a href="#gdcalert9">alert9</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>



# Greedy Algorithm


# Theory

The greedy algorithm is a problem-solving approach that works by making the locally optimal choice at each step in the hope of finding a global optimum. In other words, the algorithm makes the best possible decision at each stage without considering the overall impact of the decisions. The idea behind the greedy algorithm is that if we always choose the option that appears to be the best at the moment, we will eventually reach an optimal solution.

The greedy algorithm is often used for optimization problems, where the goal is to find the best possible solution from a set of available choices. However, the greedy algorithm is not always guaranteed to produce the optimal solution and may produce suboptimal results in some cases. Examples are below:

The image below depicts the result of a greedy algorithm that needed to find the largest possible sum, starting from the root. It focused on choosing the maximum value at each step, leading to a solution that wasn't globally optimal.



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


The image below depicts the globally optimal solution (in green). The image below depicts the globally optimal solution (in green).



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


_Pros of Greedy Algorithms:_



* simple
* easy to implement
* reasonable complexity

_Cons of Greedy Algorithms:_



* may not result in a globally optimal solution for any given problem may not result in a globally optimal solution for any given problem

_Where do we use Greedy Algorithms? _

Problems that can be solved using Greedy Algorithms satisfy the following properties:

**_Greedy choice property_**: from a local optimum we can reach a global optimum, without having to reconsider the decisions already taken

**_Optimal Substructure_**: an optimal solution can be constructed efficiently from the optimal solutions of its subproblems

**A Greedy Algorithm never reconsiders its choices!**

_Some common problems solved using the greedy approach include:_



* the Activity Selection problem
* Fractional Knapsack Problem
* Minimum Number of Coins
* Huffman Coding
* Job Sequencing problem
* Kruskal's Minimum Spanning Tree
* Prim's Minimum Spanning Tree
* Dijkstra's Shortest Path problem


# Coin Change Problem

The coin change problem is a classic example of an optimization problem that can be solved using the greedy algorithm. The problem is as follows: Given a set of coin denominations and a target amount of money, the goal is to find the minimum number of coins needed to make up the target amount.

For example, if the available coin denominations are [1, 5, 10, 25] and the target amount is 47 cents, we can use two 25-cent coins, one 10-cent coin, and two 1-cent coins to make up the target amount with a total of 5 coins.


# Greedy Algorithm for Coin Change

The greedy algorithm can be used to solve the coin change problem by always choosing the largest coin denomination that is less than or equal to the remaining amount at each step. The algorithm works as follows:



1. Sort the available coin denominations in descending order.
2. Initialize an empty dictionary to keep track of the number of coins used for each denomination.
3. Starting with the largest coin denomination, repeatedly check how many coins of that denomination can be used to make up the remaining target amount.
4. If the number of coins used is greater than zero, add the denomination and the corresponding count to the dictionary, and subtract the value of the coins from the remaining target amount.
5. Repeat steps 3 and 4 for the next largest coin denomination until the remaining target amount is zero.
6. At the end of the algorithm, the dictionary will contain the minimum number of coins needed to make up the target amount for each denomination.

_Code Example_

Here's an implementation of the greedy algorithm in Python:



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")


_Overall explanation:_

The coin_change function takes two arguments: coins, which is a list of available coin denominations, and target_amount, which is the amount of money we want to make up using the fewest number of coins possible.

Inside the function, we first initialize an empty dictionary coin_counts to keep track of the number of coins used for each denomination.

Next, we sort the available coin denominations in descending order using the sorted function with the reverse=True argument.

Then, we loop through the sorted coin denominations, starting with the largest denomination. For each denomination, we calculate the maximum number of coins that can be used to make up the remaining target amount using the // operator to perform integer division. If the number of coins is greater than zero, we add the denomination and the corresponding count to the coin_counts dictionary and subtract the value.

_Detail of the code:_



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")




* We define the function coin_change which takes two arguments: coins and target_amount. The coins argument is a list of available coin denominations, and target_amount is the amount of money we want to make up using the fewest number of coins possible. We initialize an empty dictionary coin_counts to keep track of the number of coins used for each denomination.



<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")




* We start a loop that iterates over the coin denominations in descending order. We use the sorted function with the reverse=True argument to sort the coin denominations in descending order.

    

<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")


* For each coin denomination, we calculate the maximum number of coins that can be used to make up the remaining target amount using the // operator to perform integer division. This gives us the largest number of coins we can use for the current denomination without exceeding the target amount.

    

<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image7.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image7.png "image_tooltip")


* If the number of coins is greater than zero, we add the denomination and the corresponding count to the coin_counts dictionary using coin_counts[coin] = count. We also subtract the value of the coins from the remaining target amount by multiplying the denomination by the count, i.e., target_amount -= coin * count. This ensures that we don't use more coins than necessary to make up the target amount.

    

<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image8.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image8.png "image_tooltip")


* If the target amount becomes zero after subtracting the coins, we break out of the loop, since we have found the minimum number of coins needed to make up the target amount.

    

<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image9.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image9.png "image_tooltip")


* Finally, we return the coin_counts dictionary, which contains the minimum number of coins needed to make up the target amount for each denomination.

    Overall, this code implements the greedy algorithm for the coin change problem, by choosing the largest coin denomination that is less than or equal to the remaining amount at each step. It is a simple and efficient algorithm that can solve the coin change problem in O(n log n) time, where n is the number of available coin denominations.


# 
    Reference:


    _Vikram Bajaj. "CS-GY 6033: Design and Analysis of Algorithms." GitBook, n.d., vikram-bajaj.gitbook.io/cs-gy-6033-i-design-and-analysis-of-algorithms-1/chapter1._
