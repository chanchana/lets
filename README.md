# lets
Simply customize your own commands shortcut

## Usage
You need to create `.letsipe` file in your target directory.
The syntax is
```
SHORTCUT_NAME {
    COMMAND
    COMMAND
    ...
}

default {
    COMMAND
    COMMAND
    ...
}
```
After that you can run your set of your command by
```
$ lets SHORTCUT_NAME
```
If there is no shortcut name provided, it will run the commands in the default bracket.

## Example

```
.letsipe

run {
    cd test
    gcc -o cfile cfile.c
    ./cfile
}

say {
    echo "hi"
}

default {
    echo "letsipe example"
}
```

```
$ lets run # will compile and run c file
$ lets say # will print hi
$ lets # will print letsipe example 
```
