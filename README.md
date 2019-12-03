# java9features


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
