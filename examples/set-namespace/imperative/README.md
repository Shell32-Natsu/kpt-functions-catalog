# set-namespace: Imperative Example

### Overview

This examples shows how to set namespace in the `.metadata.namespace` field on
all resources by running [`set-namespace`] function imperatively. Resources that
are known to be cluster-scoped will be skipped.

### Function invocation

Get the config example and try it out by running the following commands:

```sh
$ kpt pkg get https://github.com/GoogleContainerTools/kpt-functions-catalog.git/examples/set-namespace/imperative
$ kpt fn eval imperative --image=gcr.io/kpt-fn/set-namespace:unstable -- namespace=example-ns
```

The desired namespace is provided after `--` and it will be converted to
`ConfigMap` by kpt and used as the function configuration.

### Expected result

Check all resources have `metadata.namespace` set to `example-ns`:

[`set-namespace`]: https://catalog.kpt.dev/set-namespace/v0.1/
