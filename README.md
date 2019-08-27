```
--------------------------------------------------------------------------------
 "dt" is a simple productivity tool that organizes your work into LIFO stacks.
--------------------------------------------------------------------------------

$ ./dt help
usage: ./dt [subcmd]
  subcmd:   behavior:
  all       display entire contents of all stacks
  cat       display entire contents of current stack
  edit      open all stacks in text editor for bulk modification
  head      display top of current stack
  help      display this message
  ls        list all stacks
  pop       remove top of current stack
  push      add item at top of current stack
  rm        delete given stack
  switch    switch to given stack, creating it if necessary

--------------------------------------------------------------------------------
        When you run "dt" for the first time, you'll see an empty stack.
--------------------------------------------------------------------------------

$ ./dt ls
* main

$ ./dt cat
*

--------------------------------------------------------------------------------
            As you come up with things to do, add them to the stack.
--------------------------------------------------------------------------------

$ ./dt push Upload dt to Github

$ ./dt push Write a readme for dt

$ ./dt push Record a screencast for dt

--------------------------------------------------------------------------------
         "dt cat" will show you all the items, with the latest on top.
--------------------------------------------------------------------------------

$ ./dt cat
* Record a screencast for dt
Write a readme for dt
Upload dt to Github

--------------------------------------------------------------------------------
                 "dt" by itself will show you the latest item.
--------------------------------------------------------------------------------

$ ./dt
* Record a screencast for dt

--------------------------------------------------------------------------------
       If you get interrupted, you can make a new stack with "dt switch".
--------------------------------------------------------------------------------

$ ./dt switch interrupted-by-boss
* interrupted-by-boss
main

$ ./dt push Work on important project

$ ./dt push ZOMG go to important meeting

--------------------------------------------------------------------------------
                         "dt ls" will list your stacks.
--------------------------------------------------------------------------------
$ ./dt ls
* interrupted-by-boss
main

--------------------------------------------------------------------------------
            "dt all" will show you the contents of all your stacks.
--------------------------------------------------------------------------------

$ ./dt all

-- interrupted-by-boss --
* ZOMG go to important meeting
Work on important project

-- main --
* Record a screencast for dt
Write a readme for dt
Upload dt to Github

--------------------------------------------------------------------------------
   As you complete each work item, use "dt pop" to remove it from the stack.
             If you see "*" by itself, it means the stack is empty.
--------------------------------------------------------------------------------

$ ./dt pop

$ ./dt
* Work on important project

$ ./dt pop

$ ./dt
*

--------------------------------------------------------------------------------
        When you're done with a stack, you can use "dt rm" to delete it.
--------------------------------------------------------------------------------

$ ./dt rm interrupted-by-boss

--------------------------------------------------------------------------------
  Phew!  Now you're done with that, and you can get on with whatever you were
                     doing before you were interrupted. :-)
--------------------------------------------------------------------------------

$ ./dt all

-- main --
* Record a screencast for dt
Write a readme for dt
Upload dt to Github

$ ./dt pop
```
