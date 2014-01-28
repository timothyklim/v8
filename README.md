# install

```
export GYPFLAGS="-D OS=solaris"
gmake dependencies
gmake x64.release -j 4 library=shared strictaliasing=off # or ia32
ginstall -m 755 `pwd`/out/x64.release/lib.target/libv8.so /opt/local/lib/libv8.so
for f in `pwd`/include/*.h; do ginstall -m 644 ${f} /opt/local/include/; done
```
