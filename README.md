
# Project Title

Brief description of your project.

## Getting Started

Instructions on setting up your project locally.

### Prerequisites

What things you need to install the software and how to install them.

### Installing

A step-by-step series of examples that tell you how to get a development environment running.

## Python Command Examples

<details>
  <summary><b>List Comprehension</b></summary>

  ```python
  # Example-1: list comprehension - for loop
  >>> mylist=["alice", "bob"]
  >>> [ name.upper() for name in mylist] #[ <LOOP_ACTION> for <VARS> in <LOOP_ITER> ]
  ['ALICE', 'BOB']

  # Example-2: from list comprehension can be exposed to other python object - like tuple 
  >>> names = ["Alice", "Max", "Rose", "Jimmy"]
  >>> mylist = [ ("length", len(name) * 2) for name in names ]
  >>> print(mylist)
  [('length', 10), ('length', 6), ('length', 8), ('length', 10)]
  >>> print(type(mylist))
  <class 'list'>
  >>> print(type(mylist[0]))
  <class 'tuple'>

  # Example-3: from list comprehension can be exposed to other python object - like dictionary
  >>> names = ["Alice", "Max", "Rose", "Jimmy"]
  >>> mylist = [ {name:len(name)} for name in names ]
  >>> print(mylist)
  [{'Alice': 5}, {'Max': 3}, {'Rose': 4}, {'Jimmy': 5}]
  >>> print(type(mylist))
  <class 'list'>
  >>> print(type(mylist[0]))
  <class 'dict'>

  # Example-4: Adding conditionals statement 
  >>> numbers=[2,4,3,5,4,6,9,3,4]
  >>> [print(f"Even {i}") if i % 2 == 0 else print(f"Not even {i}") for i in set(numbers)] 
  Even 2
  Not even 3
  Even 4
  Not even 5
  Even 6
  Not even 9