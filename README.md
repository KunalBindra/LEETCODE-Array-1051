# LEETCODE-Array-1051
Let's go through a dry run of the `heightChecker` method in the `Solution` class. This method is designed to determine how many students are not standing in their correct positions if they were to stand in a line sorted by height.

Here's the step-by-step breakdown of what the method does:

1. **Initialization**:
   - `count` is initialized to 0. This variable will keep track of the number of students standing in the wrong position.
   - `n` is assigned the length of the `heights` array.
   - A new array `correct` is created which is a copy of the `heights` array.
   - The `correct` array is then sorted.

2. **Comparison**:
   - The method iterates through each element of the `heights` array.
   - For each element, it compares the value in the `heights` array with the value at the same index in the `correct` (sorted) array.
   - If the values are different, it increments the `count` by 1.

3. **Return**:
   - After the loop completes, the method returns the `count` which represents the number of students standing in the wrong position.

Let's dry run the method with an example:

```java
int[] heights = {1, 1, 4, 2, 1, 3};
```

1. **Initialization**:
   - `count = 0`
   - `n = 6` (length of `heights`)
   - `correct = {1, 1, 4, 2, 1, 3}` (copy of `heights`)
   - Sort `correct`: `correct = {1, 1, 1, 2, 3, 4}`

2. **Comparison**:
   - Compare `heights[0]` (1) with `correct[0]` (1) -> No increment (count remains 0)
   - Compare `heights[1]` (1) with `correct[1]` (1) -> No increment (count remains 0)
   - Compare `heights[2]` (4) with `correct[2]` (1) -> Increment count (count becomes 1)
   - Compare `heights[3]` (2) with `correct[3]` (2) -> No increment (count remains 1)
   - Compare `heights[4]` (1) with `correct[4]` (3) -> Increment count (count becomes 2)
   - Compare `heights[5]` (3) with `correct[5]` (4) -> Increment count (count becomes 3)

3. **Return**:
   - The method returns `count`, which is `3`.

So, the output for the input `{1, 1, 4, 2, 1, 3}` is `3`, indicating that 3 students are not in the correct positions if they were to stand in a sorted order by height.
