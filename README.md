# Simple java library to sum to numbers

Simple test to create a Java Library and upload it to Maven Central.

It adds two integer numbers

```java
package simplesum;

public class Simplesum {
    public static int add(int a, int b){
        return a+b;
    }
}
```

## Requirements

* **Java version**: 11
* **Maven version**: 3.8.3

## Steps

To create the Java package run this command (`-X` option is optional to show the Debug output):

```sh
mvn package -X
```

Then install it to your Maven local repository (by default it's located in `~/.m2/repository`

```sh
mvn install:install-file -Dfile=target/simplesum-1.0.jar -DpomFile=pom.xml -Dpackaging=jar -DcreateChecksum=true

```

## Sample Java code

Below is a simple java code (`8+9`) and the pom.xml fragment that calls the library:

```java
import simplesum.Simplesum;

public class Main {
    public static void main(String[] args) {
        System.out.println(Simplesum.add(8, 9));
    }
}
```

pom.xml fragment:

```xml
.
.
.
<dependencies>
    <dependency>
        <groupId>io.github.julian-alarcon</groupId>
        <artifactId>simplesum</artifactId>
        <version>1.0</version>
    </dependency>
</dependencies>
.
.
.
```

## References

* [https://www.programcreek.com/2011/07/build-a-java-library-for-yourself/](https://www.programcreek.com/2011/07/build-a-java-library-for-yourself/)
* [https://stackoverflow.com/questions/54452664/how-to-create-a-maven-library-non-executable-jar/54454920](https://stackoverflow.com/questions/54452664/how-to-create-a-maven-library-non-executable-jar/54454920)
* [https://github.com/suru33/sqlite-dialect](https://github.com/suru33/sqlite-dialect)
* [https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)
* [https://winterbe.com/posts/2018/08/29/migrate-maven-projects-to-java-11-jigsaw/](https://winterbe.com/posts/2018/08/29/migrate-maven-projects-to-java-11-jigsaw/)
* [https://docs.oracle.com/javase/tutorial/java/package/createpkgs.html](https://docs.oracle.com/javase/tutorial/java/package/createpkgs.html)
