# Big-O explained in plain English

**Source:** https://stackoverflow.com/a/487278/472433
**Section:** Technologies

---

## Key Insights

- **Big O measures worst-case scaling**: O(n) means doubling input roughly doubles time; O(n²) means 100x input = 10,000x time
- **Only the dominant term matters**: O(n² + 2n) simplifies to O(n²) because n² dwarfs 2n at scale
- **Common complexities ranked by performance**:
  - O(1): Constant - same time regardless of input size
  - O(log n): Logarithmic - 1M items takes ~20 operations (binary search)
  - O(n): Linear - time scales 1:1 with input
  - O(n log n): Common for good sorting algorithms
  - O(n²): Quadratic - nested loops, bubble sort
  - O(2^n): Exponential - becomes unusable quickly
  - O(n!): Factorial - traveling salesman brute force

- **Practical scaling examples**:
  - Phone book lookup: O(log n) via binary search vs O(n) for reverse lookup
  - Multiplication: O(n²) operations for n-digit numbers
  - Hash table lookup: O(1) average case enables O(n) solutions instead of O(n²)

- **Data structures enable better complexity**: Preprocessing with hash tables/trees trades O(n) setup cost for O(1) or O(log n) queries
- **Constant factors ignored**: 2n² and 100n² are both O(n²) - focus is on growth pattern, not absolute speed
- **Multiple variables matter**: String search is O(text_length + query_length), not just O(n)

## Bottom Line
Big O describes how algorithm performance scales with input size, helping you choose approaches that remain viable as data grows rather than becoming impossibly slow.