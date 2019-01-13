
.. code:: ipython3

    # FILES
    # OPERATIONS : read() / write() / append() / open()

.. code:: ipython3

    # FILES
    # OPERATIONS : 1)craete ,2)open() , 3)write()
    
    file_name = input("Enter the file name:")                  #ask user to specify name for file
    
    open_file = open(file_name, "w+")                          #open file in write mode 
    user_input = input("Write something to %s:" % file_name)   #ask to add with specifying name of file 
    read_data = open_file.read()                               #read data from file
    print(read_data)                                           #print input written in file
    open_file.close()                                          #closes file operation


.. parsed-literal::

    Enter the file name:pass
    Write something to pass:this is python. this is awesome
    
    

.. code:: ipython3

    # FILES
    # OPERATIONS : append data
    
    file_name = input("Enter the file name:")
    
    f = open(file_name, "a")
    user_input = input("What would you like to add to %s:" % file_name)
    f.write(user_input)    
    with open(file_name) as f:                  #use file to refer to file object
            for line in f:                      #use loop to scan through file
                u = line.split()                #split lines as in elements in list
                print(u)
    f.close()



.. code:: ipython3

    # FILES
    # OPERATIONS : Check if File exists 
    
    # os module contains a submodule - 'path'. path module contains isFile method that returns True if file exists and
    # false if it does not exist. Sys module can be used to exit out of program if file does not exist
    
    import os, sys
    
    file_name = input("Enter the file name:")
    
    if os.path.exists(file_name):                   #path submodule checks if file exists
        our_file = open(file_name, 'r')             #if present then open in read mode
        read_data = our_file.read()
        print(read_data)                            #print data that is in file
        our_file.close()  
    else:
        sys.exit()                               #if file not present then execution jumps to else bloc
    

