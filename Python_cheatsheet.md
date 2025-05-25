# Python Cheatsheet


## Data types
str - store characters
int, float, complex - store numeric values
list, tuple, range - store multiple values in continuous fashion
dict - store key - value pair
bool - store True or False(Boolean values)


## if - elif - else
if (condition):
    statement/s;
elif (condition):
    statement/s;
else:
    statement/s;

elif and else are optional
But if elif is given, must write else
When condition of if is false, condition of next elif is checked. This goes on till statement of any elif is correct. Else the statement in else is executed.


## Iteration

### while:
while (condition):
    statement/s;

till the condition is correct the statement/s will be executed

### for
for iterator in range(lower, upper):
    statement/s;

range generates values starting from lower till upper (but not include upper) and passes one value at a time to iterator
till the last value the loop runs

for iterator in iterate_type:
    statement;
here the iterate_type can be list,tuple, dictionary, set, string.


### string operations

variable_name = str() 
variable_name = ''
create empty string

### list operations

variable_name = []
variable_name = list()

create empty list
variable_name.append(value) : add 'value' at the end of the list.
variable_name.insert(index, value) : add value at the index
variable_name.extend(new_list) : extends the list by new_list i.e. adds the values of new_list as elements.
lst.count(value) : counts the occurance of value in the list
lst.index(value) : return the index of the first occurance of value
lst.pop(index) : if index is given then the value at that index is removed and returned, else the value at last index is removed and returned 

### Dictionary

dict = {} : empty dictionary

dict[key] = value : update the value of key
if key in dict:
    dict[key] += 1
else:
    dict[key] = 1 
: This counts the occurance of key and store in dictionary

dict.pop(key) : remove the key, value pair of the given key

dict.clear() : removes all the elements

dict.items() : makes a list of tuples of key,value pair

for key, value in dict.items():
    print(f'{key}, {value});