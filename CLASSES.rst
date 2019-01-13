
.. code:: ipython3

    # CLASSES : BLUEPRINT FOR CREATING OBJECTS 

.. code:: ipython3

    class MyClass:
        
    #def __init__(self) method is a constructor provided by python 
    #whenever object created PVM invokes __init__() and passes that object as first parameter to the functions defined
    #so self parameter in any other methods wil be the object actually which was passed and taht object replaces self.var as obj.var
    
        def __init__(self,name):
            self.name = name
    
        def greeting(self):                           #simple user def function that prints out text
            print("Hey,",self.name)
    
        def greet_user(self):                        #function takes input from user and prints text along with input
            name = input("What's your name:")
            print("Hello,", name)
    
        def addition(self):                          
            number1 = int(input("Enter the number:"))         #input 1st number
            number2 = int(input("Enter the number:"))         #input 2nd number
            add = number1 + number2                           #add botha nd store in a 3rd variable
            print("Sum is:",add)                              #print the final result
    
        def spectate(self):  
            our_list = []                                     #initialize an empty list
            size_of_list = int(input("Enter size of list:"))  #ask user to specify length of list.this will conatin no of eements as length
            for i in range(size_of_list):                     #use range function to loop through list
                element = input('Enter something: ')          #ask user to input range number of times
                our_list.append(element)                      #append the entered input to list
            print(our_list)                                   #print out the fnal output
    
    m = MyClass("Chuck")                                      #create an instance of class
    
    m.greet_user()                                            #access method by using . 'dot' operator after instance 
    m.greeting()
    print("")
    m.addition()
    print("")
    m.spectate()
    
    
