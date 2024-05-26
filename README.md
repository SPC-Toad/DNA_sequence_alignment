# DNA Sequence Alignment

This project implements a basic dynamic programming approach to sequence alignment, specifically designed for DNA sequences. The algorithm aligns two sequences and calculates the optimal path with the minimum cost, considering matches, mismatches, and gaps.

## Files

- **Path.java**: This class represents a path in the dynamic programming sequence alignment algorithm. It stores the row, column, cost, and the next node in the optimal path.

- **Match.java**: This class contains the algorithm for matching two sequences using dynamic programming. It initializes the alignment matrix, computes the alignment, and returns the optimal path with the minimum cost.

## Classes

### Path

- **Attributes**:
  - `int row`: The row index this node represents.
  - `int col`: The column index this node represents.
  - `int cost`: The matching cost from this point.
  - `Path next`: The next node in the optimal path.

- **Methods**:
  - `public Path()`: Constructor initializing `next` to `null`.
  - `public int getCost()`: Returns the cost.
  - `public void setCost(int c)`: Sets the cost.
  - `public int getRow()`: Returns the row index.
  - `public void setRow(int r)`: Sets the row index.
  - `public int getCol()`: Returns the column index.
  - `public void setCol(int c)`: Sets the column index.
  - `public Path getNext()`: Returns the next node in the path.
  - `public void setNext(Path p)`: Sets the next node in the path.

### Match

- **Attributes**:
  - `Path[][] opt`: The 2D matrix representing the alignment.
  - `int row_len`: The number of rows in the matrix.
  - `int col_len`: The number of columns in the matrix.
  - `int i, j`: Loop variables.
  - `int col_gap, row_gap, mis_match, min_cost`: Cost variables.

- **Methods**:
  - `public Match()`: Constructor.
  - `public Path match(String a, String b)`: Computes the optimal match between two sequences and returns the last node in the optimal path.
  - `public static void main(String[] args)`: Test case to demonstrate the sequence alignment.

## How to Use

1. **Compile the classes**:
   ```sh
   javac pa3/Path.java pa3/Match.java
   ```

2. **Run the test case**:
   ```sh
   java pa3.Match
   ```

   This will execute the `main` method in the `Match` class, aligning the sequences "AACAGTTACC" and "TAAGGTCA", and printing the costs of the optimal path.

## Example Output

```
4 --> 3 --> 2 --> 2 --> 2 --> 2 --> 2 --> 2 --> 2 --> 1 --> 0 --> 
```

The output represents the costs along the optimal path from the start to the end of the alignment.