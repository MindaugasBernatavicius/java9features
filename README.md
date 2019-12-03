# java9features

## Materials:
- https://www.youtube.com/results?search_query=java+module+system
- https://dzone.com/articles/java-9-modules-introduction-part-1
- https://jrebel.com/rebellabs/java-9-modules-cheat-sheet/

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
