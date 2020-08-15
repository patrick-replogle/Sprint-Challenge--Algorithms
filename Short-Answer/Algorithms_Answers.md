#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) The runtime will be o(n) since the while loop will run exactly n times.

b) The runtime will be o(n log n). This is because while the rate of growth is greater than a linear runtime, as n increases the operation increase is still significantly smaller than a quadratic runtime.

c) The runtime will be o(n) since a recursive function with only one recursive call and no extra
looping will generally have a run time of o(n). In this case the function will be called n times + 1 one extra call to reach the base case and return out.

## Exercise II

My algorithm to solve this would be based off of the binary search method and would have a runtime of o(log n).

The steps would be as follows: 1. Because the building floors are already sorted in ascending order, we could simply start by throwing
the egg off of the middle floor. We could calulate the middle floor by adding the first floor and last floor together and then dividing by two.

    2. If the egg does not break, it is safe to assume the floors from the start to the middle of building are not f. Therefore we can weed those floors out as options and move the starting postion to the middle floor + 1 and keep the end pointer at the highest floor and recalculate the middle floor between these two floors and repeat the process of dropping the egg.

    3. Otherwise if the egg does break, we would keep track of that floor as a potential lowest floor that the egg would break, but to be sure, we would now repeat the process by looking at the middle floor between first floor and floor right below our initial middle floor. This is because the egg will break at floor f and all floors above. Therefore we can't be sure yet that this is the lowest floor the egg will break on.

    4. We would repeat these steps until our left pointer is greater than our right pointer, while keeping track of the lowest floor the egg breaks from along the way.

    5. At the end we will not only have the lowest floor the egg will break from, but we will have cut the amount of items we must search thru in half at each iteration, making this algorithm logarithmic in nature.
