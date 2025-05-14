# Awk - Top 10 awk usages

awk is a scripting language, and it is helpful when working in the command line. It's also a widely used command for text processing.

## Following are the top 10 awk usages

1. Print specific columns
   
   - Syntax : awk '{print $line_no} file_name
   - Example: 
     - awk '{print $1}' file_name.txt -> This command prints the first column of the file_name.txt
     - awk '{print $1, $3}' file_name.txt -> Prints multiple columns separeted by comma
     - awk '{print $0}' file_name.txt -> Prints the complete file, just like cat command

2. Pattern matching

   - Syntax : awk '/pattern/ {print $0}' file_name
   - Example:
     - awk '/error/ {print $0}' file_name.txt -> This will print all the lines with 'error' in it.
     - awk '/^A/' file_name -> Prints all the lines that start with 'A'
     - awk '/0$/' file_name -> Prints all the lines that end with '0'(zero)

3. Field separator
   
    - Syntax : awk -F: '{print $1}' file_name -> By default awk separates columns by white-space, but using -F: it can be set to ':'.
    - Variation:
      - awk -F: '{print $1}' file_name.csv
      - awk -F, '{print $1}' file_name -> This will separate columns by ','.

4. Condition based print
   
   - awk '$3 > 50 {print $1, $3}' file_name -> Prints lines where value of 3rd column is greater than 50. 

5. Sum a column
   - awk '{sum += $2} END {print sum}' file_name -> Sums the value 

6. Line numbering
   - Syntax : awk '{print NR, $column_no}' file_name
   - Example:
     - awk '{print NR, $0}' file_name -> Prints the line number before each line and then prints it.
  
7. Counts lines matching a pattern
   - awk '/failed/ {count++} END {print count}' file_name -> 

8. Replace text
   - Syntax : awk '{gsub("target", "replacement"); print}' file_name -> gsub = General substitution
   - awk '{gsub("foo", "bar"); print}' file_name

9.  Print last line
    - awk 'END {print}' file_name

10. Multiple conditions
    - Syntax : awk 'condition 1 && condition 2 {print column_number}' file_name 
    - awk '$2 >= 50 && $2 <= 100 {print $1, $2}' file_name


## Reference
**freecodecamp** - https://www.freecodecamp.org/news/the-linux-awk-command-linux-and-unix-usage-syntax-examples/