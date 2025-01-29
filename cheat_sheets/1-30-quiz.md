## Relevant notes from class

24. echo prints to stdout - standard out
25. by default it's the screen - TTY - stands for teletype
26. `>>` redirects stdout to a file - appends
27. cat outputs content of a file
28. `|` is called a pipe - takes the output of a previous command and puts it into the right command
29. just running grep opens a new interface for you to type in so that it can search through it
30. `^` means control
31. grep outputs the whole line, if it contains the specified phrase
32. grep does two things - it loads a file and searches - this means it doesn't conform with unix philosophy
33. input redirection with < - pass contents of a file to the input of a program - so `< readme` is the same as `cat readme |`
34. `>` output redirection but deletes the contents of the file first


11. ^ - means beginning of line
12. $ - means end of line
13. wc -l
    1. counts the total number of lines in stdin
    2. wc is word count, -l is a line modifier
14. if there's no output to a command on a quiz LEAVE THE PROBLEM BLANK
    1. he will take points off if you write 'there is no output'
15. grep -E tag
    1. allows extended regular expressions
    2. ie alternation operators
    3. when do you need the -E?
        1. check the grep manpage with man grep
        2. for now you can kinda ignore the -E
        3. it's about the minimal required syntax to make regex work- | isn't in it
16. inside of quotation marks, | is an alternation operator
17. for the quiz we have to know ^ $ . * |
18. here document, heredoc - 
19. `<<EOF` - input redirection via a heredoc - when you run this it will take everything you type until you type EOF and redirect that input into the thing to the left
    1. EOF is traditional but you can use any combination of characters you want
    2. has to be an exact match, not regex
20. ! isn't an exclamation point, it's a bang


10. making your shell prompt shorter - export ps1='$ '
11. idempotency - if a function has no effect and you can call it more than one time without changing the environment, it's idempotent
12. shell variable features
    1. no spaces around equals sign
    2. a string with spaces has to be in quotation marks
13. if you want to do a variable substitution you need a dollar sign in front of your variable
14. in shell, variable gets interpreted before passing the outcome to the terminal
15. in python, single and double quotes have the same meaning- not in terminal
16. in single quotes, variable expansion does not happen
17. in double quotes, it does!
18. $() is command subsitution- $ always means substitution, () means whatever is inside is run as if it were a function
19. so var=$(echo echo echo) runs echo echo echo, and puts the output in a file named var
20. concatenation is just smushing stuff together
21. putting curly braces around the variable is cool too
22. if you use a variable that doesn't exist you don't get an error message, it just subsitutes in an empty string
23. heredocs - we covered these last class
24. any time you do substitution in a shell instead of in double quotes, spacing gets ignored and it just all gets printed in one line
25. if you put single quotes around the EOF characters in the heredoc it ignores variable substitution
26. you can't substitute some variables and not others
27. new way of defining a varible
    1. export {variable definition}
    2. this makes the variable an environment variable- will get passed to all children processes
    3. any time you run a shell script, all the variables you exported exist inside of the child process and will get substituted correctly
    4. you can also make one by defining a variable in the same line as when you run a child process

## Notes from reviewing quizzes


