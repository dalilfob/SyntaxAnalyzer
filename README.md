#Syntax Analyzer

Toy Language Syntax Analyzer (CUP/YACC) 

## Quick Start
- Clone this
- ``sh setup.sh``
- ``sh run.sh``

## Compile Instructions
### Clone this repository

```
git clone https://github.com/blazindragon/SyntaxAnalyzer.git
```

### Compile via Bash Script (Reccomended)

Works in Bash (UNIX) and Powershell with 'sh' in path (WINDOWS)

```
sh setup.sh 
```

### Compile Manually

```
java -jar lib/JFlex.jar toy.flex > dump.no
java java_cup.Main -nowarn -nosummary -expect 50 toy.cup &> dump.no
javac Driver.java
```
The redirects to ``dump.no`` are used to filter the warning messages and garbage output from stdout (byproduct of altering the CUP files to print shifting). Feel free to remove them. 


## Run Tests

### Via Script

```
sh run.sh
```

### Manually

```
java Driver tests/test1.toy > results/test1.out
java Driver tests/test2.toy > results/test2.out
java Driver tests/test3.toy > results/test3.out
java Driver tests/test4.toy > results/test4.out
```

## Resources

[JFlex Manual](http://jflex.de/manual.html)

[Cup User Manual](http://www2.cs.tum.edu/projects/cup/manual.html#basic-symbols)

[Cup Tools Slides](http://cs.haifa.ac.il/courses/compilers/BILAL/Tutorials/JLex_CUP_tools.pdf](Cup Tools Slides)
