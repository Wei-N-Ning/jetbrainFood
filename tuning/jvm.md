
source:

Tuning CLion

https://www.jetbrains.com/help/clion/tuning-the-ide.html

CLion runs on the Java Virtual Machine (JVM), which has various options that control its performance. The default options used to run CLion are specified in the following file:

(linux)
```
<IDE_HOME>/bin/clion64.vmoptions (for the default 64-bit JVM)
<IDE_HOME>/bin/clion.vmoptions (for optional 32-bit JVM)<Paste>
```

To configure JVM options:
```
On the Help menu, click Edit Custom VM Options.
```
CLion creates a copy of the file with JVM options in the configuration directory and opens it in a new editor tab. Any values that you change in this file will override the values from the original default file.

NOTE: it creates a config file copy at ~/.CLion$$$/config

`-Xmx, Xms`	

Limits the maximum memory heap size that the JVM can allocate for running CLion. Default value depends on the platform. If you are experiencing slowdowns, you may want to increase this value, for example, to set the value to 2048 megabytes, change this option to `-Xmx2048m`.

NOTE: this can be helpful for me at wt (heavily templated code)

Do not change platform properties in the default file, because it is replaced when CLion is updated. Moreover, in case of macOS, editing this file violates the application signature.


