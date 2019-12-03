# java9features

## Materials:
- GENERAL:
  - https://www.youtube.com/results?search_query=java+module+system
  - https://dzone.com/articles/java-9-modules-introduction-part-1
  - https://app.pluralsight.com/library/courses/java-9-modularity-first-look/table-of-contents
- CMD:
  - https://jrebel.com/rebellabs/java-9-modules-cheat-sheet/
  - https://openjdk.java.net/projects/jigsaw/quick-start
- GRADLE: 
  - https://github.com/java9-modularity/gradle-modules-plugin
  - https://guides.gradle.org/building-java-9-modules/
  
## Goals:
- [ ] A
- [ ] B

```
package use;

import prov.ModuleProvider;

public class ModuleUser {
  public static void main(String[] args){
    ModuleProvider.helloPrinter("Mindaugas");
  }
}
```
```
package prov;

public class ModuleProvider {
  public static void helloPrinter(String s){
    System.out.println("Hello" + s);
  }
}
```

```
javac -d out --module-path cf.mindaugas.hello --module-source-path . --module cf.mindaugas.app,cf.mindaugas.hello

javac -d out --module-source-path . --module cf.mindaugas.hello
javac -d out --module-path ./cf.mindaugas.hello/ --module-source-path . --module cf.mindaugas.app


java --module-path ..\out -m cf.mindaugas.app/cf.mindaugas.app.App

javac -d ../out --module-path ../out/com.banana.hello --module-source-path . --module cf.mindaugas.app

```
