---
layout: post
category : Algorithms
tagline: ""
tags : [algorithms, java, mini-article, interview-question]
---
{% include JB/setup %}


## Problem Statement

### Find occurance of a number in a given array of integers/character?

Similar problem statement in Hackerearth can be found here
https://www.hackerearth.com/practice/data-structures/arrays/1-d/practice-problems/algorithm/memorise-me/

#### Input
An array of numbers/characters, a number/character to find occurance for.

#### Output
Occurance of the number/character.

## Solution

### Solution

 - Create a HashMap<Integer, Integer>
 - `put()` the numbers/characters as key
 - Keep track of occurance as values
 - `get()` occurance for a number/character
 
#### Time Complexity O(n)

 - Create a HashMap<Integer, Integer>
 - `put()` the numbers/characters as key - `O(n)`
 - Keep track of occurance as values
 - `get()` occurance for a number/character - `O(1)`
 
#### Code

    public static int countOccu(int[] array, int a){
				
        HashMap<Integer, Integer> occ = new HashMap<Integer, Integer>();
		
        for(int ar : array){
            if(occ.containsKey(ar)){
                occ.put(ar, (occ.get(ar)+1));
            }else{
                occ.put(ar, 1);
            }
		}		
		return (occ.containsKey(a)) ? occ.get(a) : 0;
	}