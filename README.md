# Defining-and-Instantialing-a-Class
Wrap the words_dict() and print_top_words() functions in a class called WordProcess

Place the insertion point on line 10 and press Enter twice.

There should be two blank lines between your insertion point and the end of the COMMON_WORDS definition.

Type class WordProcess:

Highlight the code from lines 14 through 60 and press Tab.

Your two functions are now within the scope of the overall WordProcess class. In other words, they are now methods of the WordProcess class.

Position the insertion point at the end of line 12, and press Enter.

Type the following docstring with a blank line after it:

Add a constructor to your new class.

Position the insertion point in line 14. Press Enter and Tab.

Type the following code, including the empty line at the end.

This constructor takes self, as all constructors do, and it also takes file as a parameter. This will be the file path that the user provides, and in this constructor, you're assigning an instance attribute to this parameter.

On line 19, in the words_dict() method, add self as a parameter.

You'll be using the reference to the class instance in order to invoke the file path that the user provides.

Select the list expression in lines 21 and 22 as shown.

Replace the selected code by typing self.file

Construct an instance of the class with your user's file path input.

Position the insertion point at the end of line 70 and press Enter twice.

Type the following:

This constructs an instance of WordProcess with the user's input as the file parameter. The instance is assigned to the variable class_init.

Change function calls to class method references and perform additional cleanup.

In line 87, change the print_top_words() function call to the following:

In this line, you're calling the print_top_words() method by first referencing the WordProcess class. This prevents issues arising with scope. When you call this method, you're passing in two parameters: the class instance you constructed previously (which contains the user's file path) and the common_word answer to the question of suppressing common words. This all ends in the print_top_words() method executing its code and printing the results to the console.

Scroll up to line 46, where the print_top_words() method is defined.

Add self as the first parameter, keeping choice as the second.

Now, choice will take on the common_word answer, and self will, as usual, refer to the class instance.

In line 49, change the function call to a method call.

The word_count variable will now hold the dictionary returned by the words_dict() method, while using the class instance.

Add a class method that creates a key to be used in sorting results.

Position the insertion point in line 18, and press Enter and Tab.

Type the following code, including the empty line at the end.

This is a class method and not associated with any instance. It takes item as a parameter and returns index -1 of item. The -1 index tells Python to start from the end of the list rather than the beginning.

Scroll down to the print_top_words() method. On line 54, locate the items variable definition.

Add a comment, revise the statement, and add blank lines before and after it as shown.

The sorted() function also takes two additional arguments, a key and a reverse value. The key references the sort_by_value() class method you just created and tells Python to sort each tuple in the list by its last item. Recall that each tuple holds two values: the dictionary key and its associated value. The value comes second, and is technically last ([-1]), so Python is sorting by value. Since the value is the frequency that a word appears, Python is sorting by frequency. Lastly, the reverse argument simply tells Python to output the results in descending order (most frequent word first).

On line 25, add .split() to the end of the read_input definition so that your string input can be split into a list.

Test out your program to confirm that your class code works.

Run the program.

At the first prompt, type ThiS iS a test! A test, a

Answer "y" or "n" to suppressing common words, whichever you prefer.

Verify that the results are successfully printed to the console.

Run the program again, this time verifying the opposite choice for suppressing words.
