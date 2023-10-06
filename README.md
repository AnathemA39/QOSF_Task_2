# QOSF_Task_2
Task 2: Finding if a negative number exists in a random list


The idea here is to use Grover's Search Algorithm to search our input list for a number.

Our input list may consist of positive and negative integers, and our goal is to determine with the aid of a quantum program whether or not there is a negative number in the list.

To use Grover's algorithm, we have to define a winning element 'w'. However, there are an infinite amount of negative numbers, so we shall do a bit of preprocessing beforehand. By dividing each member of the input list by the absolute value of itself, we obtain a list of positive and negative one's.

Hence, we reduce our number of candidate winning elements to just one. We then define our winning element as -1, so we can perform Grover's Algorithm.

After running, we get a distribution of probablities. We then do a bit of postprocessing on the probability values. 
We take these probabilities into a list, and by analysing the probabilities, we can determine if there was a negative number.


The method used is based on the assumption that the maximum probability will always be much larger than the minimum of the probabilities.

Hence if    max( list_of_probabilities) - min( list_of_probabilities) - 10* min( list_of_probabilities) is a positive number, then there is very likely a negative number in the input list.
If however, max( list_of_probabilities) - min( list_of_probabilities) - 10* min( list_of_probabilities) is a negative number, then there is very likely no negative number in the input list.
