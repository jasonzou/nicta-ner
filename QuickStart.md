- Command line shell interface to process the input text
```
  > java -Xmx200m -jar NamedEntityAnalyser.jar
  Type in texts, -q for quit.
  > <Input text>
```

- Find named entities from the text document:

```
  > java -Xmx200m -jar NamedEntityAnalyser.jar <text fileName>  
```

- Using jar in the java code:

  * import ner pakcage
```
  import nicta.ner.NamedEntityAnalyzer;
  import nicta.ner.NERResultSet;
```

  * Create analyzer
```
  NamedEntityAnalyzer namedEntityAnalyzer = new NamedEntityAnalyzer();
```

  * string analysis
```
  NERResultSet nerResultSet = namedEntityAnalyzer.process("String input here.");
```

  * file analysis
```
  NERResultSet nerResultSet = namedEntityAnalyzer.process(NamedEntityAnalyzer.ReadFileAsString("File name"));
```

  * output to string
```
  String result = nerResultSet.toString();
```

  * output to HashMap
```
  HashMap<String, String> resultMap = nerResultSet.getMappedResult();
```