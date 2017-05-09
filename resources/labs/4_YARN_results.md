
# Slowest
```
Mapper containers=8
Reducer containers=1
Container memory=1024MB
mapper JVM heap=819MB
reducer JVM heap=819MB

Teragen :

real    1m25.493s
user    0m5.901s
sys     0m0.744s

Terasort :

real    2m58.733s
user    0m8.503s
sys     0m0.780s
```

# Fastest
```
Mapper containers=8
Reducer containers=2
Container memory=512MB
mapper JVM heap=409MB
reducer JVM heap=409MB

Teragen :

real    1m29.851s
user    0m5.520s
sys     0m0.723s

Terasort :

real    2m22.101s
user    0m8.173s
sys     0m0.783s
```



