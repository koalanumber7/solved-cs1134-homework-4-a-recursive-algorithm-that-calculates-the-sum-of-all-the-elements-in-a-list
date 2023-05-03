Download Link: https://assignmentchef.com/product/solved-cs1134-homework-4-a-recursive-algorithm-that-calculates-the-sum-of-all-the-elements-in-a-list
<br>



<strong>Homework #4 </strong>

<strong><u>Question 1: </u></strong>

You are given 2 implementations for a recursive algorithm that calculates the sum of

all the elements in a list (of integers):

<strong>def </strong>sum_lst1(lst):

<strong>if </strong>(len(lst) == 1):

<strong>return </strong>lst[0]

<strong>else</strong>:

rest = sum_ lst1(lst [1:]) sum = lst[0] + rest

<strong>return </strong>sum

<strong>def </strong>sum_lst2(lst, low, high):

<strong>if </strong>(low == high):

<strong>return </strong>lst[low]

<strong>else</strong>:

rest = sum_ lst2(lst, low + 1, high) sum = lst[low] + rest

<strong>return </strong>sum

<u>Note:</u> The implementations differ in the parameters we pass to these functions:

<ul>

 <li>In the first version we pass only the list (all the elements in the list have to be taken in to account for the result).</li>

 <li>In the second version, in addition to the list, we pass two indices: low and high (low ≤ high), which indicate the range of indices of the elements that should to b e considered.</li>

</ul>

The initial values (for the first call) passed to low and high would represent the range of the entire list.

1) Make sure you understand the recursive idea of each implementation.

2 ) Analyze the running time of the implementations above. For each version:

<ol>

 <li>Draw the recursion tree that represents the execution process of the function, and the local-cost of each call.</li>

 <li>Conclude the total (asymptotic) running time of the function.</li>

</ol>

3 ) Which version is asymptotically faster?




<strong><u>Question 2: </u></strong>

Analyze the running time of each of the following functions. For each function:

<ol>

 <li>Draw the recursion tree that represents the execution process, and the cost of each call.</li>

 <li>Conclude the total (asymptotic) running time.</li>

</ol>

<u>Note:</u> For the simplicity of the analysis of sections (b) and (c), you may assume that n is a power of 2, therefore it can always be divided evenly by 2.

<ol>

 <li></li>

</ol>

<strong>def </strong>fun1 (n):

<strong>if </strong>(n == 0):

<strong>return </strong>1

<strong>else</strong>:

part1 = fun1(n-1) part2 = fun1(n-1) res = part1 + part2 <strong>return </strong>res

<ol>

 <li></li>

</ol>

<strong>def </strong>fun2(n): <strong>if </strong>(n == 0):

<strong>return </strong>1 <strong>else</strong>:

res = fun2(n//2)

res += n <strong>return </strong>res

<ol>

 <li></li>

</ol>

<strong>def </strong>fun3 (n): <strong>if </strong>(n == 0):

<strong>return </strong>1 <strong>else</strong>:

res = fun3(n//2)

<strong>for </strong>i <strong>in </strong>range(1, n+1):

res += i

<strong>return </strong>res




<strong><u>Question 3 : </u></strong>

Give a <strong>recursive </strong>implement to the following functions:

a . <strong>def </strong>print_triangle(n)

This function is given a positive integer n, and prints a textual image of a right triangle (aligned to the left) made of <em>n </em>lines with asterisks.

For example, print_triangle (4), should print: *

**

***

****

b . <strong>def </strong>print_oposite_triangles( n )

This function i s given a positive integer n, and prints a textual image of a two opposite right triangles (aligned to the left) with asterisks, each containing <em>n </em>lines.

For example, print_ oposite_triangles (4), should print:

* * * *

***

**

*

*

**

***

****

<ol>

 <li><strong>def </strong>print_ruler(n)</li>

</ol>

This function is given a positive integer n, and prints a vertical ruler of 2 − 1 lines. Each line contains ‘-‘ marks as follows:

<ul>

 <li>The line in the middle ( ~)</li>

</ul>

~of the ruler contains <em>n </em>‘-‘ marks

<table>

 <tbody>

  <tr>

   <td width="50">•••</td>

   <td width="527">The lines at the middle of each half( and ~) of the ruler contains (<em>n </em>– 1 ) ‘- ‘~marks~The lines at the ~, <sup>3</sup><sub>8</sub>, *and ~ of the ruler contains (<em>n</em>-2) ‘-‘ marks~And so on …</td>

  </tr>

 </tbody>

</table>




For example, print_ruler(4), should print (only the blue marks):




<table>

 <tbody>

  <tr>

   <td width="583">

    <table width="100%">

     <tbody>

      <tr>

       <td> </td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="345">

    <table width="100%">

     <tbody>

      <tr>

       <td>

        <table>

         <tbody>

          <tr>

           <td width="73"><strong>1/16</strong><strong>=</strong></td>

           <td width="40"><strong>1/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>2/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"><strong>1/8</strong></td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>3/16</strong><strong>=</strong></td>

           <td width="40"><strong>3/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>4/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"> </td>

           <td width="34"><strong>1/4</strong></td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>5/16</strong><strong>=</strong></td>

           <td width="40"><strong>5/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>6/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"><strong>3/8</strong></td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>7/16</strong><strong>=</strong></td>

           <td width="40"><strong>7/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>8/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"><strong>1/2</strong></td>

          </tr>

          <tr>

           <td width="73"><strong>9/16</strong><strong>=</strong></td>

           <td width="40"><strong>9/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>10/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"><strong>5/8</strong></td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>11/16</strong><strong>=</strong></td>

           <td width="40"><strong>11/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>12/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"> </td>

           <td width="34"><strong>3/4</strong></td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>13/16</strong><strong>=</strong></td>

           <td width="40"><strong>13/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>14/16</strong><strong>=</strong></td>

           <td width="40"> </td>

           <td width="24"><strong>7/8</strong></td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

          <tr>

           <td width="73"><strong>15/16</strong><strong>=</strong></td>

           <td width="40"><strong>15/16</strong></td>

           <td width="24"> </td>

           <td width="34"> </td>

           <td width="81"> </td>

          </tr>

         </tbody>

        </table> </td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<table>

 <tbody>

  <tr>

   <td width="80">

    <table width="100%">

     <tbody>

      <tr>

       <td><strong>–</strong><strong>– –</strong><strong>–</strong><strong>– – –</strong><strong>–</strong><strong>– –</strong><strong>–</strong><strong>– – – –</strong><strong>–</strong><strong>– –</strong><strong>–</strong><strong>– – –</strong><strong>–</strong><strong>– –</strong><strong>–</strong></td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>




<u>Hints:</u>

1 . Take for n=4: when finding print_ruler(4) , try to think first what print_ruler(3) does, and how you can use it to print a ruler of size 4. Then, generally identify what print_ruler(n-1) is <strong>supposed </strong>to print, and use that in order to define how to print the ruler of size n.

2 . You may want to have more than one recursive call

3 . It looks much scarier than it actually is

<strong><u>Question 4 : </u></strong>

Give a <strong>recursive </strong>implement to the following function:

<strong>de f </strong>list min(lst, low, high)

The function i s given lst, a list of integers, and two indices: low and high ( low ≤ high), which indicate the range of indices that need to be considered.

The function should find and return the minimum value out of all the elements at the position <em>low, low+1, …, high </em>in l s t .




<strong><u>Question 5 : </u></strong>

Give a <strong>recursive </strong>implement to the following functions:

<ol>

 <li><strong>def </strong>count_lowercase(s, low, high):</li>

</ol>

The function i s given a string s, and two indices: low and high (low ≤ high), which indicate the range of indices that need to be considered.

The function should return the number of lowercase letters at the positions <em>low, low+1, …, high </em>in s .

<ol>

 <li><strong>def </strong>is_number _of_lowercase_even(s, low, high):</li>

</ol>

The function i s given a string s, and two indices: low and high (low ≤ high), which indicate the range of indices that need to be considered.

The function should return True if there are even number of lowercase letters at the positions <em>low, low+1, …, high </em>in s, or False otherwise.

<strong><u>Question 6 : </u></strong>

Give a <strong>recursive </strong>implement to the following function:

<strong>de f </strong>appearances(s, low, high)

The function is given a string s, and two indices: low and high (low ≤ high), which indicate the range of indices that need to be considered.

The function should return a dictionary that stores a mapping of characters to the number of times they each appear in s. That is, the keys of the dictionary should be the different characters in s, and their associated values should be the number of times each of them appears in s .

For example, the call appearances (”Hello world”, 0, 10) could return: {’e’:1, ’o’:2, ’H’:1, ’l’:3, ’r’:1, ’ ’:1, ’d’:1, ’w’:1}.

<u>Note:</u> A dictionary is a mutable object. Use that property to <strong>update </strong>the dictionary, returned from your recursive call.

<strong><u>Question 7: </u></strong>

Give a <strong>recursive </strong>implement to the following function:

<strong>de f </strong>split_by_sign(lst, low, high)

The function is given a list lst of non-zero integers, and two indices: low and high ( low ≤ high), which indicate the range of indices that need to be considered.

The function should reorder the elements in lst, so that all the negative numbers would come before all the positive numbers.

<u>Note:</u> The order in which the negative elements are at the end, and the order in which the positive are at the end, doesn’t matter, as long as all he negative are before all the positive.




<strong><u>Question 8: </u></strong>

A <strong><em>nested list of integers </em></strong>is a list that stores integers in some hierarchy. That is, its elements are integers and/or other nested lists of integers.

For example nested_lst=[[1, 2], 3, [4, [5, 6, [7], 8]]] is a nested list of integers.

Give a <strong>recursive </strong>implement to the following function: <strong>de f </strong>flat_list (nested_lst, low, high)

The function is given a nested list of integers nested_list, and two indices: low and high (low ≤ high), which indicate the range of indices that need to be

considered.

The function should flatten the sub-list at the positions <em>low, low+1, …, high </em>of

n e s t e d_l i s t, and return this flattened list. That is, the function should create a new 1-level (non hierarchical) list that contains all the integers from the <em>low…high</em>

range in the input list.

For example, when calling flat_ list to flatten the list nested_lst

demonstrated above (the initial call passes low=0 and high=2), it should create and return [1, 2, 3, 4, 5, 6, 7, 8] .

<strong><u>Question 9: </u></strong>

Given an ordered list <em>L</em>. A <strong><em>permutation </em></strong>of <em>L </em>is a rearrangement of its elements in

some order. For example <em>(1, 3, 2) </em>and <em>(3, 2, 1) </em>are two different permutations of <em>L=(1, 2, 3)</em>.

Implement the following function:

<strong>de f </strong>permutations(lst, low, high)

The function is given a list lst of integers, and two indices: low and high ( low ≤ high), which indicate the range of indices that need to be considered.

The function should return a list containing all the different permutations of the elements in lst. Each such permutation should be represented as a list.

For example, if lst=[1, 2, 3], the call permutations(lst, 0, 2) could

return [[1, 2, 3], [2, 1, 3], [1, 3, 2], [3, 2, 1], [3, 1, 2], [2, 3, 1]]

<u>Hint:</u> Think recursion!!!

Take for example lst=[1, 2, 3, 4]: to compute the permutation list of l s t, try to first write down the list containing all permutations of [1, 2, 3], then, think how to modify it, so you get the permutation list of [1, 2, 3, 4].