
Note: This should be forked off of the codebase created by base.md

```ucm:hide
.> compile.native.fetch
.> compile.native.genlibs
.> load unison-src/builtin-tests/testlib.u
.> add
```

If you want to define more complex tests somewhere other than `tests.u`, just `load my-tests.u` then `add`,
then reference those tests (which should be of type `'{IO,Exception,Tests} ()`, written using calls
to `Tests.check` and `Tests.checkEqual`).

```ucm:hide
.> alias.type #ggh649864d ThreadKilledFailure
.> load unison-src/builtin-tests/concurrency-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/tcp-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/tls-chain-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/tls-tests.u
.> add
.> load unison-src/builtin-tests/bytes-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/list-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/text-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/bytes-tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/io-tests.u
.> add
```

TODO remove md5 alias when base is released
```ucm:hide
.> alias.term ##crypto.HashAlgorithm.Md5 base.crypto.HashAlgorithm.Md5
```

```ucm:hide
.> load unison-src/builtin-tests/tests.u
.> add
```

```ucm:hide
.> load unison-src/builtin-tests/tests-jit-only.u
.> add
```

```ucm
.> run.native tests
```

```ucm
.> run.native tests.jit.only
```
