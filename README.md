# CSA09 Assignment 2 (CO2): Strings, Collections, Hashing, Generics and Ranking

- **Name:** Bala Ashwin R
- **Register number:** 1921260102
- **Java version:** OpenJDK 21 (replace with the output of `java -version` on your machine)

## How to compile and run
Open a terminal inside a task folder, then `javac *.java` and `java <MainClass>` (main classes are listed in each `notes.md`).
The benchmark programs (Q1, Q2, Q4, Q7 and parts of Q3, Q5, Q6) print raw data lines starting with `ROW,`; the files `raw_data_*.txt` are the outputs used in the report.

| Task | Folder | Result |
|---|---|---|
| Building Text Under Load: String, StringBuilder or StringBuffer | Q1 | + is 1.5x/4.1x/49x slower than StringBuilder on workloads A/B/C and allocates up to 163x more; StringBuilder loses data when shared between threads (800,000 of 1,600,000 in one trial, an exception in another); StringBuffer was always correct. |
| When Is ArrayList an Appropriate Engineering Choice | Q2 | ArrayList: O(1) get and fast end add, but front edits cost 7.6 microseconds at 100,000 elements; LinkedList get(k) is about 520x slower; ArrayDeque is best for Up Next (0.96 ms vs 75.5 ms for 100,000 operations). |
| Engineer the hashCode-equals Contract | Q3 | Without hashCode the program prints 3 unique students; with the fix it prints 2. All 10 predictions in HashContractTests matched. |
| Choosing a Map for a Pharmacy Inventory | Q4 | Hash-based maps look up in tens of ns, TreeMap in hundreds of ns, binarySearch in about 1 microsecond; LinkedHashMap chosen; every report order verified. |
| Derive a Generic Ranking Component from a Principle | Q5 | Output matches expected: [Eagles(9,6), Bisons(9,4), Panthers(9,4), Cobras(6,1)]; subtraction comparator and missing tie-break break the principle as designed. |
| Priority, Order and Fairness in a Queue | Q6 | Output matches expected; 8-patient hand check matches; starvation shown and fixed with virtual deadlines; 5,000 patients take about 1.3 ms. |
| Diagnose, Redesign and Validate | Q7 | RingList: 0 mismatches against ArrayList in 300,000 random operations; about 10x fewer element moves and 4x to 17x faster than ArrayList on the mixed Up Next workload. |

The full report (predictions, designs, tables, complexity analysis, Q7 design challenge) is `CSA09-1921260102-Assignment2-Report.pdf`.
