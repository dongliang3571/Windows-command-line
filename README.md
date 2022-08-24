# Windows-command-line

### Comments

Two ways to write comments
```cmd
REM this is a comment
:: another comment
```

### `@` sign

The `@` symbol tells the command processor to be less verbose; to only show the output of the command without showing it being executed or any prompts associated with the execution. When used it is prepended to the beginning of the command, it is not necessary to leave a space between the "@" and the command.

For example:

 If we did `@echo off`, It would've shown echo off on the command line, however with @ you can make it so it doesn't show it.


### Funtions

```cmd
:function_name 
Do_something 
EXIT /B 0 :: EXIT /B %ERRORLEVEL% is a way to exit function, another way is goto:eof
```

for example:

```cmd
:Display 
SET /A index=2 
echo The value of index is %index% 
EXIT /B 0

:: calling a function
call :Display
```

another example:

```cmd

:myDosFunc    :: here starts my function identified by it`s label
echo. :: here the myDosFunc function is executing a group of commands
echo. :: it could do a lot of things
GOTO:EOF :: Finished and exit
```


