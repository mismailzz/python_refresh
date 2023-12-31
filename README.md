
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

  # Example-5: List to string concatenation 
  >>> my_list = [0, 1, 2, 3, 4]
  >>> my_string = ",".join([str(i) for i in my_list])
  >>> print(my_string)
  0,1,2,3,4

  # Example-6: MAX, MIN, SUM
  >>> min([ num for num in range(0,100) if num % 3 == 0 ])
  0
  >>> max([ num for num in range(0,100) if num % 3 == 0 ])
  99
  >>> sum([ num for num in range(0,100) if num % 3 == 0 ])
  1683
  ```

  <details>
    <summary><b>Other Comprehension</b></summary>

    ```python
    #Example-1: Dict. comprehension
    >>> { f"player-{num}":num for num in range(0,5) }
    {'player-0': 0, 'player-1': 1, 'player-2': 2, 'player-3': 3, 'player-4': 4}

    #Example-2: list comprehension to create a list of tuples, then turn the tuples into dict keys and values:
    >>> list_tuples= [ (f"player-{num}",num) for num in range(0,5) ]
    >>> print(list_tuples)
    [('player-0', 0), ('player-1', 1), ('player-2', 2), ('player-3', 3), ('player-4', 4)]
    >>> { key:value for (key, value) in list_tuples }
    {'player-0': 0, 'player-1': 1, 'player-2': 2, 'player-3': 3, 'player-4': 4}

    #Example-3: Set comprehension 
    >>> my_set={num for num in [1,2,3,4]}
    >>> print(my_set)
    {1, 2, 3, 4}
    >>> 

    #Example-4: Generator expression 
    >>> [ i ** 2 for i in range(10) if i%2 == 0]
    [0, 4, 16, 36, 64]
    >>> ( i ** 2 for i in range(10) if i%2 == 0)
    <generator object <genexpr> at 0x100daeac0>
    >>> gen_exp=( i ** 2 for i in range(10) if i%2 == 0 )
    >>> [ print(num) for num in gen_exp ]
    0
    4
    16
    36
    64
    >>>

    #timeit
    ```    
  </details>
