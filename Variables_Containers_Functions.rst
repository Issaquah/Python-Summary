
.. code:: ipython3

    #variables can be declared dynamically and don't need  no need to declare their data type
    a=2
    b=3.3
    c="python"
    print(a)
    print(b)
    print(c)


.. parsed-literal::

    2
    3.3
    python
    

.. code:: ipython3

    #Containers
    #LIST
    # 1)slicing a list
    lst = [1, 2, 3.3, "Car", "Yatch", 1.0]
    print(lst)
    lst[1:3]
    lst[0:]
    print(lst)
    lst[0:-1]
    print(lst)
    lst[:]
    
    


.. parsed-literal::

    [1, 2, 3.3, 'Car', 'Yatch', 1.0]
    [1, 2, 3.3, 'Car', 'Yatch', 1.0]
    [1, 2, 3.3, 'Car', 'Yatch', 1.0]
    1 1
    2 2
    3 3.3
    4 Car
    5 Yatch
    6 1.0
    

.. code:: ipython3

    # LIST
    # 2)looping through list
    
    count=0
    lst = [1, 2, 3.3, "Car", "Yatch", 1.0]
    for i in lst:
        count += 1
        print(count,i)


.. parsed-literal::

    1 1
    2 2
    3 3.3
    4 Car
    5 Yatch
    6 1.0
    

.. code:: ipython3

    # LIST
    # 3)Indexing
    
    lst = [1, 2, 3.3, "Car", "Yatch", 1.0]
    
    print(lst[0])
    print(lst[4])
    print(lst[5:])
    


.. parsed-literal::

    1
    Yatch
    [1.0]
    

.. code:: ipython3

    # LIST
    # 4)MODIFYING A LIST : append/remove/extend another list
    
    lst = [1, 2, 3.3, "Car", "Yatch", 1.0]
    
    lst.append(2.7777)
    print(lst)
    
    lst1 = [2, 3, 5, 111, "Todd", "Yuval"]
    
    lst.append(lst1)
    print(lst)
    
    lst.pop(3)
    print(lst)
    


.. parsed-literal::

    [1, 2, 3.3, 'Yatch', 1.0, 2.7777, [2, 3, 5, 111, 'Todd', 'Yuval']]
    


.. code:: ipython3

    # DICTIONARY
    # OPERATIONS : 1)CREATE/2)INDEXING AND RETURN VALUES/ 3)/LOOPING/ 4)MODIFY:append element;remove element;extend dictionary
    
    # 1)CREATING 
    # 2)INDEXING AND RETURN VALUES
    our_dict = {1:2,2:3,3:"Car",4:9.999,5:"Arum",6:"Marquard",7:243}
    
    print(our_dict[3])
    print(our_dict[2])
    print(our_dict.get(4))
    print(our_dict.get(1))


.. parsed-literal::

    Car
    3
    9.999
    2
    

.. code:: ipython3

    # DICTIONARY
    # 3)LOOPING THROUGH LIST
    # 3.1)loop and get keys
    # 3.2)loop and get values
    our_dict = {1:2,2:3,3:"Car",4:9.999,5:"Arum",6:"Marquard",7:243}
    for i in our_dict:
        print(i)
    print("")    
    for j in our_dict:
        print(our_dict[j])
    


.. parsed-literal::

    1
    2
    3
    4
    5
    6
    7
    
    2
    3
    Car
    9.999
    Arum
    Marquard
    243
    

.. code:: ipython3

    # DICTIONARY
    # 4)MODIFY:append element;remove element;extend dictionary
    
    our_dict = {1:2,2:3,3:"Car",4:9.999,5:"Arum",6:"Marquard",7:243}
    # append elements
    our_dict[8]="TeV"
    our_dict[9]="eee"
    
    # remove elements
    our_dict.pop(6)
    our_dict.pop(1)
    
    # extend another dictionary
    our_dict1 = {1:"cccc", 2:"ttttt", 3:"ooop"}
    our_dict[10]=our_dict1
    
    print(our_dict)
    
    


.. parsed-literal::

    {2: 3, 3: 'Car', 4: 9.999, 5: 'Arum', 7: 243, 8: 'TeV', 9: 'eee', 10: {1: 'cccc', 2: 'ttttt', 3: 'ooop'}}
    


.. code:: ipython3

    # TUPLES
    # OPERATIONS : 1)CREATE/ 2)INDEXING /3)LOOPING /4)SLICING 
    
    # 1)CREATE TUPLE
    # 2)INDEXING
    
    tpl = (1, 2, 34, "Maxx", 3.8098, "zhen", "Maxx")
    print(tpl)
    print("")
    print(tpl[1])
    print(tpl[4])
    print(tpl[0])
    print(tpl[3])
    


.. parsed-literal::

    (1, 2, 34, 'Maxx', 3.8098, 'zhen', 'Maxx')
    
    2
    3.8098
    1
    Maxx
    

.. code:: ipython3

    # TUPLES
    # 3)LOOPING 
    # 4)SLICING
    
    tpl = (1, 2, 34, "Maxx", 3.8098, "zhen", "Maxx")
    
    for i in tpl:
        print(i)
    
    print("")
    
    print(tpl[:])
    print(tpl[0:3])
    print(tpl[:2])
    print(tpl[1:])


.. parsed-literal::

    1
    2
    34
    Maxx
    3.8098
    zhen
    Maxx
    
    (1, 2, 34, 'Maxx', 3.8098, 'zhen', 'Maxx')
    (1, 2, 34)
    (1, 2)
    (2, 34, 'Maxx', 3.8098, 'zhen', 'Maxx')
    

.. code:: ipython3

    # TUPLES
    # 5)FINDING THE OCCURANCE OF ELEMENTS IN TUPLE
    
    tpl = (1,2,34,"Maxx",3.8098,"zhen","Maxx")
    
    print("Maxx:",tpl.count("Maxx"))

.. code:: ipython3

    # SETS
    # OPEARTIONS: 1)CREATE/ 2)EXTEND ELEMENT TO SET /3)MODIFY SET /4)LOOPING
    
    # 1)CREATE
    # 4)LOOPING THROUGH SET
    
    sets = {1,2,3,4,5,"Maxx","zhen","doug"}
    
    for i in sets:
        print(i)

.. code:: ipython3

    # SETS
    # 2)EXTEND ELEMENT TO SET
    
    sets = {1,2,3,4,5,"Maxx","zhen","doug"}
    
    sets.add("sas")
    sets.add("Truman")
    sets.add(2.333)
    sets.add(8.9990)
    
    print(sets)


.. parsed-literal::

    {1, 2, 3, 4, 5, 'Maxx', 'sas', 'Truman', 2.333, 8.999, 'zhen', 'doug'}
    

.. code:: ipython3

    # SETS
    # 3)MODIFY SET : remove() / pop() / discard()
    
    sets = {1,2,3,4,5,"Maxx","zhen","doug"}
    
    sets.remove(1)
    print(sets)
    sets.discard("zhen")
    print(sets)
    sets.pop()
    print(sets)
    


.. parsed-literal::

    {2, 3, 4, 5, 'Maxx', 'zhen', 'doug'}
    {2, 3, 4, 5, 'Maxx', 'doug'}
    {3, 4, 5, 'Maxx', 'doug'}
    


.. code:: ipython3

    # FUNCTIONS : BLOCK OF CODE - WRITE ONCE CALL MANY TIMES YOU WANT
    # OPERATIONS : 1)DEFINE FUNCTION THAT PRINTS A STATEMENT
    
    def say_hello_world():          
        print("hello, world")
    
    say_hello_world()
    

.. code:: ipython3

    # FUNCTIONS : BLOCK OF CODE - WRITE ONCE CALL MANY TIMES YOU WANT
    # OPERATIONS : WHAT USER DEFINED FUNCTIONS LOOKS LIKE 
                   
    def addition():
        number1 = int(input("Enter the number:"))
        number2 = int(input("Enter the number:"))
        add = number1 + number2
        print("Addition=",add)
        
    def say_hello_to_user():
        name_of_user = input("Enter your name:")        
        print("Hello, ", name_of_user)     
    
    say_hello_to_user()
    addition()
    


.. parsed-literal::

    Enter your name:Chaitanya
    Hello,  Chaitanya
    Enter the number:3
    Enter the number:6
    Addition= 9
    

.. code:: ipython3

    # FUNCTIONS : BLOCK OF CODE - WRITE ONCE CALL MANY TIMES YOU WANT
    # OPERATIONS : 1)PARAMETERIZED FUNCTION
    #              2)RETURNING MULTIPLE VALUES 
    
    def calc(number1, number2):
        sum = number1 + number2                 
        diff = number1 - number2
        product = number1 * number2
        div = number1 / number2
    
        return sum, diff, product, div
    
    print(calc(10,20))
    


.. parsed-literal::

    (30, -10, 200, 0.5)
    

.. code:: ipython3

    # FUNCTIONS : BLOCK OF CODE - WRITE ONCE CALL MANY TIMES YOU WANT
    # OPERATIONS : WHAT INNER FUNCTION LOOKS LIKE
    
    def message(username):
        def greet_user():
            return "Hello, "
        greet = greet_user() + username
        return greet
    
    message("Aaron")
    

.. code:: ipython3

    # FUNCTIONS : BLOCK OF CODE - WRITE ONCE CALL MANY TIMES YOU WANT
    # OPERATIONS : WORKING WITH DATA-STRUCTURES IN FUNCTIONS
    
    def display(lst):                     
        for i in lst:                      
            print(i)                       
    
    display([1,2,3,4,5])
    

.. code:: ipython3

    # RECURSIVE FUNCTIONS - FUNCTION THAT CALLS ITSELF
    # OPERATIONS : CALCULATE FACTORIAL OF A NUMBER
    
    def factorial(n):                       
        if n == 0:                       
            return 1
        else:
            result = n * factorial(n - 1)   
        return result                       
    
    factorial(4)

.. code:: ipython3

    # RECURSIVE FUNCTIONS - FUNCTION THAT CALLS ITSELF
    # OPERATIONS : CALCULATE FACTORIAL OF A NUMBER USING ITERATION
    
    def iterative_recursion():
        num = int(input("Enter a value:"))
        result = 1
        for i in range(2, num+1):
            result = result * i
        return result
