# Update a File through a Python Algorithm

### Project Description

An allow list of IP addresses is used at my organization to control access to prohibited content.  The `allow_list.txt` file contains information on these IP addresses.  A separate delete list identifies the IP addresses that should no longer have access to this content.  I developed an algorithm to automatically update the `allow_list.txt` file and remove IP addresses that should no longer have access.

### Open the file that contains the allow list

I started the process by opening the `allow_list.txt` file.  I first assigned this file name as a string to the `import_file` variable.

![image alt](https://github.com/mruiz4241/mruiz4241/blob/99598430c66b412f36268309eec0de39b91e8814/ScreenshotPython1.png)

Then, I used a `with` statement to open the file:

![image alt](https://github.com/mruiz4241/mruiz4241/blob/ad113b74582d9d5003436856f2f683e2024adad5/ScreenshotPython2.png)

In my algorithm, the `with` statement is combined with the `.open()` function in read mode to open the allow list file and read it.  The reason for opening the file is so that I can access the IP addresses recorded in the allow list file.  The `with` keyword assists in resource management by shutting the file after exiting the `with` statement.  In the code using `open(import_file, "r") as file:`, the `.open()` function contains two parameters. The first identifies the file to import, and the second specifies what I intend to do with it.  In this situation, `"r"` means I want to read it.  The code also employs the `as` keyword to create a variable named `file`, which holds the result of the `.open()` method while I work within the with statement.

### Read the file contents

In order to read the file contents, I used the `.read()` method to convert it into the string.

![image alt](https://github.com/mruiz4241/mruiz4241/blob/19dbd6debc7cf076c14378942521f2814ae537c5/ScreenshotPython3.png)

When using an `.open()` function with the `"r"` option for "read," I can call the `.read()` method within the body of the with statement.  The `.read()` method transforms the file to a string, allowing me to read it.  I used the `.read()` function on the file variable specified in the with expression.  I then allocated the string output of this procedure to the variable `ip_addresses`. 

In essence, this code reads the contents of the `allow_list.txt` file and converts them to string format, which I can then use to organize and extract data in my Python program.

### Convert the string into a list

To delete specific IP addresses from the allow list, I required them in list format.  I then used the `.split()` method to transform the `ip_addresses` string into a list:

![image alt](https://github.com/mruiz4241/mruiz4241/blob/e8a359c713588d387ace6d17670be688a8053cae/ScreenshotPython4.png)

The `.split()` function is invoked by attaching it to a string variable.  It operates by turning the contents of a string into a list.  Splitting `ip_addresses` into a list makes it easier to remove IP addresses from the allow list.  By default, the `.split()` function divides text by whitespace into list items.  In this approach, the `.split()` function turns the data contained in the variable `ip_addresses`, which is a string of IP addresses separated by whitespace, into a list of IP addresses.  To save this information, I transferred it to the variable `ip_addresses`.

### Iterate through the remove list

Iterating through the IP addresses contained in the `remove_list` is an important part of my technique.  To accomplish this, I used a `for` loop:

![image alt](https://github.com/mruiz4241/mruiz4241/blob/48908b40788d9e586e680acd5cf4ae8a4c18e9b6/ScreenshotPython5.png)

Python's `for` loop repeats code for a given sequence.  The `for` loop in this Python program serves the goal of applying specified code instructions to all elements in a series.  The `for` keyword begins the for loop.  It is followed by the loop variable `element` and the keyword `in`.  The term in means to cycle through the sequence `ip_addresses` and assign each value to the loop variable `element`.

### Remove IP addresses that are on the remove list

My technique involves deleting any IP address from the allow list `ip_addresses` that is also in the `remove_list`.   Because there were no duplicates in `ip_addresses`, I could use the following code to accomplish this:

![image alt](https://github.com/mruiz4241/mruiz4241/blob/c13b7a3ff5e134689dcba0de2bffe894300c52db/ScreenshotPython6.png)

