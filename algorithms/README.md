# Algorithms

## Bubble Sort

## Selection Sort

## Insertion Sort

## Merge Sort
- Divide the array in the middle.
- Sort the two halves (recursively).
- Merge the resulting sorted halves together to produce the sorted result.

```
                  mergesort(0,3)
		┌───┬───┬───┬───┐
		| 5 | 3 | 4 | 1 |
		└───┴───┼───┴───┘
		        |
	    ┌───────────┴───────────┐
	    | mergesort(0,1)        | mergesort(2,3)
	┌───┼───┐               ┌───┼───┐
        | 5 | 3 |               | 4 | 1 |
        └───┼───┘               └───┼───┘
            |                       | 
     ┌──────┴──────┐         ┌──────┴──────┐
     | ms(0,0)     | ms(1,1) | ms(2,2)     | mergesort(3,3)
   ┌─┴─┐         ┌─┴─┐     ┌─┴─┐         ┌─┴─┐
   | 5 |         | 3 |     | 4 |         | 1 |
   └─┬─┘         └─┬─┘     └─┬─┘         └─┬─┘
     |             |         |             |
     └──────┬──────┘         └──────┬──────┘
            | merge(0,0,1)          | merge(2,2,3)
        ┌───┼───┐               ┌───┼───┐
        | 3 | 5 |               | 1 | 4 |
        └───┼───┘               └───┼───┘
            |                       | 
	    └───────────┬───────────┘
		        | merge(0,1,3)
		┌───┬───┼───┬───┐
		| 1 | 3 | 4 | 5 |
		└───┴───┴───┴───┘
```

Trace
```
[5, 3, 4, 1]
mergeSort( [5, 3, 4, 1], 0, 3)
mergeSort( [5, 3, 4, 1], 0, 1)
mergeSort( [5, 3, 4, 1], 0, 0)
mergeSort( [5, 3, 4, 1], 1, 1)
merge( [5, 3, 4, 1], 0, 0, 1)
mergeSort( [3, 5, 4, 1], 2, 3)
mergeSort( [3, 5, 4, 1], 2, 2)
mergeSort( [3, 5, 4, 1], 3, 3)
merge( [3, 5, 4, 1], 2, 2, 3)
merge( [3, 5, 1, 4], 0, 1, 3)
[1, 3, 4, 5]
```

## Quick Sort

## Head Sort
