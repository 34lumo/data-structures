# Data Structures

Solved exercises from the Data Structures course (Estructuras de Datos) of the
Computer Engineering degree at Universidad Complutense de Madrid.

## What it is

Each folder is one exercise from the course problem sheets. Most of them give you
a linked list or a binary tree class and ask you to add one operation to it
(reverse the list, check that a tree is a search tree, rebuild a tree from its
traversals). The code was written in Visual Studio during the course and later
moved here with the IDE files removed.

Every program reads its test cases from a text file in the same folder (the
`#ifndef DOMJUDGE` block at the top of `main`) and prints the answers to the
console or to `datos.out`. The DomJudge define is what the course's online judge
uses to make the program read from standard input instead.

## Exercises

| Folder | Original name | What it does |
| --- | --- | --- |
| `00-11-academia` | 0.11 ACADEMIA | Class that tracks students by level with `unordered_map`, `set` and `list`; no `main`, it was a work in progress |
| `02-1-duplicate` | 2.1 DUPLICAR | Singly linked list: insert a copy of every node right after it |
| `02-2-reverse` | 2.2 INVERTIR | Singly linked list: reverse it in place by relinking nodes |
| `02-3-merge` | 2.3 MEZCLAR | Singly linked lists: merge two sorted lists into one sorted list reusing the nodes |
| `02-4-intersection` | 2.4 INTERSECCION | Singly linked lists: keep only the values present in both sorted lists |
| `02-5-replicate` | 2.5 REPETIR | Singly linked list: repeat or delete each element according to a second list of counts |
| `03-1-add-and-reorder` | 3.1 SUMAR | Doubly linked list: add `m` to the element at position `i` and move it so the list stays sorted |
| `03-2-partition` | 3.2 PARTICION | Doubly linked list: move everything smaller or equal to a pivot in front of the rest |
| `03-3-intersection-double` | 3.3 INTERSECCION2 | Doubly linked lists: intersection of two sorted lists, same idea as 2.4 |
| `03-4-swap-pairs` | 3.4 INTERCAMBIAR2A2 | Doubly linked list: swap the nodes two by two (1 2 3 4 becomes 2 1 4 3) |
| `04-1-balanced-brackets` | 4.1 PARENTESIS | Stack: check that `()`, `[]` and `{}` in a line are balanced |
| `07-1-barrier` | 7.1 BARRERA | Binary tree: find the shallowest multiple of 7 whose path from the root has no prime number |
| `07-1-barrier-v2` | 7.1 BARRERA (2) | Second take on the same exercise, with a different recursion that carries the depth down |
| `07-2-rebuild-from-traversals` | 7.2 RECONSTRUCCION | Binary tree: rebuild it from its preorder and inorder traversals |
| `08-1-is-bst` | 8.1 ESARBOLBINARIODEBUSQUEDA | Binary tree: say whether it is a binary search tree (works for ints and strings) |
| `08-2-is-dense` | 8.2 ESDENSO | Binary tree: check that an inorder walk gives consecutive integers |
| `08-3-rebuild-bst` | 8.3 RECONSTRUCCIONABB | Binary search tree: rebuild it from its preorder traversal |

## Stack

C++14, standard library only. The `list_linked_*.h`, `stack_linkedlist.h` and
`Header.h` files hold the list, stack and `BinTree` classes handed out in class,
plus the method written for each exercise.

## Run it

Every folder with a `main.cpp` compiles on its own:

```
cd 02-1-duplicate
g++ -std=c++14 main.cpp -o main
./main
```

The program reads the test file named in its `main` (`datos.txt`, `datos.in`,
`casos.txt`, ...) and writes to `datos.out` or the console. `00-11-academia` has
no `main`, so only `g++ -std=c++14 -c main.cpp` applies to it.

## Project layout

```
NN-M-name/      one folder per exercise (sheet number, exercise number, name)
  main.cpp      reads the cases and prints the answers
  *.h           the data structure for that exercise
  *.txt, *.in   test cases
```
