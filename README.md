#Syntax Analyzer

Toy Language Syntax Analyzer (CUP/YACC) 

# Compile & Run Instructions
1. Clone this repository
```
git clone https://github.com/blazindragon/SyntaxAnalyzer.git
```
2. Create Lexer.java via JFlex and JFlex Specification
```
java -jar JFlex.jar toy.flex
```
3. Create parser.java via CUP and CUP specificatin
```
java java_cup.Main -expect 50 -nonterms toy.cup
```
4. Test 
```
javac ParserDriver.java
java ParserDriver test1.toy
```

# Modified CUP Compile

In order to show shift actions, requires the use of the modified cup files:

```
java java_cup.Main -expect 50 -nonterms toy.cup
```

#CUP Compile

```
java -jar java-cup-11a.jar -expect 50 -nonterms toy.cup
```

## Resources

[JFlex Manual](http://jflex.de/manual.html)

[Cup User Manual](http://www2.cs.tum.edu/projects/cup/manual.html#basic-symbols)

[Cup Tools Slides](http://cs.haifa.ac.il/courses/compilers/BILAL/Tutorials/JLex_CUP_tools.pdf](Cup Tools Slides)
