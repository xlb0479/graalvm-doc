# 本地镜像构建输出

- [构建阶段](#构建阶段)
- [资源使用统计](#资源使用统计)
- [机器可读的构建输出](#机器可读的构建输出)

下面是构建`HelloWorld`类的本地镜像时的输出示例：

```text
================================================================================
GraalVM Native Image: Generating 'helloworld' (executable)...
================================================================================
[1/8] Initializing...                                            (2.8s @ 0.15GB)
 Java version: 20+34, vendor version: GraalVM CE 20-dev+34.1
 Graal compiler: optimization level: 2, target machine: x86-64-v3
 C compiler: gcc (linux, x86_64, 12.2.0)
 Garbage collector: Serial GC (max heap size: 80% of RAM)
--------------------------------------------------------------------------------
 Build resources:
 - 13.24GB of memory (42.7% of 31.00GB system memory, determined at start)
 - 16 thread(s) (100.0% of 16 available processor(s), determined at start)
[2/8] Performing analysis...  [****]                             (4.5s @ 0.54GB)
    3,163 reachable types   (72.5% of    4,364 total)
    3,801 reachable fields  (50.3% of    7,553 total)
   15,183 reachable methods (45.5% of   33,405 total)
      957 types,    81 fields, and   480 methods registered for reflection
       57 types,    55 fields, and    52 methods registered for JNI access
        4 native libraries: dl, pthread, rt, z
[3/8] Building universe...                                       (0.8s @ 0.99GB)
[4/8] Parsing methods...      [*]                                (0.6s @ 0.75GB)
[5/8] Inlining methods...     [***]                              (0.3s @ 0.32GB)
[6/8] Compiling methods...    [**]                               (3.7s @ 0.60GB)
[7/8] Layouting methods...    [*]                                (0.8s @ 0.83GB)
[8/8] Creating image...       [**]                               (3.1s @ 0.58GB)
   5.32MB (24.22%) for code area:     8,702 compilation units
   7.03MB (32.02%) for image heap:   93,301 objects and 5 resources
   8.96MB (40.83%) for debug info generated in 1.0s
 659.13kB ( 2.93%) for other data
  21.96MB in total
--------------------------------------------------------------------------------
Top 10 origins of code area:            Top 10 object types in image heap:
   4.03MB java.base                        1.14MB byte[] for code metadata
 927.05kB svm.jar (Native Image)         927.31kB java.lang.String
 111.71kB java.logging                   839.68kB byte[] for general heap data
  63.38kB org.graalvm.nativeimage.base   736.91kB java.lang.Class
  47.59kB jdk.proxy1                     713.13kB byte[] for java.lang.String
  35.85kB jdk.proxy3                     272.85kB c.o.s.c.h.DynamicHubCompanion
  27.06kB jdk.internal.vm.ci             250.83kB java.util.HashMap$Node
  23.44kB org.graalvm.sdk                196.52kB java.lang.Object[]
  11.42kB jdk.proxy2                     182.77kB java.lang.String[]
   8.07kB jdk.internal.vm.compiler       154.26kB byte[] for embedded resources
   1.39kB for 2 more packages              1.38MB for 884 more object types
--------------------------------------------------------------------------------
Recommendations:
 HEAP: Set max heap for improved and more predictable memory usage.
 CPU:  Enable more CPU features with '-march=native' for improved performance.
--------------------------------------------------------------------------------
    0.8s (4.6% of total time) in 35 GCs | Peak RSS: 1.93GB | CPU load: 9.61
--------------------------------------------------------------------------------
Produced artifacts:
 /home/janedoe/helloworld/helloworld (executable)
 /home/janedoe/helloworld/helloworld.debug (debug_info)
 /home/janedoe/helloworld/sources (debug_info)
================================================================================
Finished generating 'helloworld' in 17.0s.
```

## 构建阶段

### 初始化



## 资源使用统计

## 机器可读的构建输出