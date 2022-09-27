Python Debugger 

Use breakpoint() in code to put breakpoint.
Run code and pdb will automatically start debugging.

Commands:
-h(elp) - show commands list
-q(uit) - stop debugging
-n(ext) - jump to next breakpoint
-w(here) - prints current frame
-u(p) [count] - frame up
-d(own) [count]- frame down
-b(reak) - set breakpoint
-tbreak - set temp breakpoint
-cl(ear) [number] - clear breakpoints 
-disable [number] - disable breakpoint in specific line
-enable [number] - enable breakpoint in specific line
-ignore [number] - ignore next given number of breakpoints
-condition [number] - set condition which must eveluate to true before breakpoint
-commands [number]  - specify list of commands for breakpoint. type end in the end of command list
-s(tep) - execute current line and stop at first possible occasion
-unt(il) [lineno] - continue execution until line number is greater or equal to given one.
-r(eturn) - execute until current function returns
-c(ontinue) - continue execution to next breakpoint
-l(ist) - list source code around breakpoint.
-ll - long list
-a(rgs) - print arguments of current function
-p [expression] - evaluate expression and print value
-pp [expression] - like p but pretty-printed
-whatis [expression] - print type of expression
