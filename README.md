# ja-netfilter 2022.2.0

### A Java Instrumentation Framework

## Usage

* download from the [releases page](https://gitee.com/ja-netfilter/ja-netfilter/releases)
* add `-javaagent:/absolute/path/to/ja-netfilter.jar` argument (**Change to your actual path**)
    * add as an argument of the `java` command. eg: `java -javaagent:/absolute/path/to/ja-netfilter.jar -jar executable_jar_file.jar`
    * some apps support the `JVM Options file`, you can add as a line of the `JVM Options file`.
    * **WARNING: DO NOT put some unnecessary whitespace characters!**
* or execute `java -jar /path/to/ja-netfilter.jar` to use `attach mode`.
* for **Java 17** you have to add at least these `JVM Options`:

  ```
  --add-opens=java.base/jdk.internal.org.objectweb.asm=ALL-UNNAMED
  --add-opens=java.base/jdk.internal.org.objectweb.asm.tree=ALL-UNNAMED
  ```

* edit your plugin config files: `${lower plugin name}.conf` file in the `config` dir where `ja-netfilter.jar` is located.
* the `config`, `logs` and `plugins` directories can be specified through **the javaagent args**.
  * eg: `-javaagent:/path/to/ja-netfilter.jar=appName`, your config, logs and plugins directories will be `config-appname`, `logs-appname` and `plugins-appname`.
  * if no javaagent args, they default to `config`, `logs` and `plugins`.
  * this mechanism will avoid extraneous and bloated `config`, `logs` and `plugins`.

* run your java application and enjoy~
## update

   
