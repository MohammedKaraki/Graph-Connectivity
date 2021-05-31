# Graph-Connectivity
To compile with gcc:

```g++ -O3 -std=c++20 -o conn.x main.cpp -lfmt```

Compatibility relations should be provided through ```stdin```. For example:

```cat compatibility_relations_samples/p4ncc | ./conn.x```

This should give the following 3 possible band structure connectivities:

```
1: A5 A5 GM8 GM8 GM9 GM9 M5 M5 R3 R3 R4 R4 X3 X3 X4 X4 Z5 Z6 Z7 Z8 

2: A5 GM8 GM8 M5 R3 R4 X3 X4 Z5 Z7 
   A5 GM9 GM9 M5 R3 R4 X3 X4 Z6 Z8 

3: A5 GM8 GM9 M5 R3 R4 X3 X4 Z5 Z8 
   A5 GM8 GM9 M5 R3 R4 X3 X4 Z6 Z7 
```

Each of the latter two graphs contains two disconnected subgraphs. In each of these cases, at least one of the two disconnected components must form a topological band.
