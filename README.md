# jmh-benchmarks

### Instructions to run
1. Go to project root and run
` mvn clean install`
2. Then run 
`java -jar target/benchmarks.jar`

Sample run results on my Macbook Pro Mid 2014:

```
# Run complete. Total time: 00:16:45

REMEMBER: The numbers below are just data. To gain reusable insights, you need to follow up on
why the numbers are the way they are. Use profilers (see -prof, -lprof), design factorial
experiments, perform baseline and negative tests that provide experimental control, make sure
the benchmarking environment is safe on JVM/OS/HW level, ask for reviews from the domain experts.
Do not assume the numbers tell you what you want them to tell.

Benchmark                     Mode  Cnt   Score    Error  Units
MyBenchmark.testMethod        avgt   25  ≈ 10⁻⁸            s/op
MyBenchmark.testMethodStatic  avgt   25  ≈ 10⁻⁸            s/op
```

**Inference**

Both executing non static and static does not have any performance improvements even at the scale of 10 ^ -8. So adding static is just a matter of convention than for performance.