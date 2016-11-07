## JagTag
JagTag is a simple - yet powerful and customizable - interpretted text parsing language!
Some methods are included in the built-in libraries, and additional methods can be defined that utilize the parser environment veriables, as well as the method's input.

## Simple Example
```java
import jagtag.*;
public class Example
{
  public static void main(String[] args)
  {
    Parser parser = JagTag.newDefaultBuilder()
                .addMethod( new Method("exclaim", (env,in) -> in[0]+"!!!") )
                .build();
    String result = parser.parse("{exclaim:{if:this|=|that|then:Foo Bar|else:Hello World}}");
    System.out.println(result);
  }
}
```
Result: `Hello World!!!`

## Current Projects
Here are some other projects that utilize JagTag:
* [**Spectra (Discord Bot)**](https://github.com/jagrosh/Spectra) - Spectra uses JagTag in its customizable "tags" (user-created commands), and in welcome and leave messages for servers. (https://github.com/jagrosh/Spectra/blob/master/src/spectra/jagtag/libraries/Discord.java)
