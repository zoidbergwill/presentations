# Examples

## Perf

```
perf record -F 99 -a -g -- sleep 60
perf report --sort comm,dso
```

## Flamegraphs

```
perf record -F 99 -a -g -- sleep 60
perf script > out.perf
./stackcollapse-perf.pl out.perf > out.folded
./flamegraph.pl out.folded > perf.svg
```

## eBPF + Python

## Scope

