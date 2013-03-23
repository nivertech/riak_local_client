riak_local_client
=================

###Riak Erlang local client

The Riak local client Erlang modules extracted from:
- https://github.com/basho/riak_kv/tree/1.3.0

###Why do you need this?

When working with riak local client from separate Erlang VM, you need to set path, so BEAM will be able to find `riak_kv/ebin`.
While this easy to do with `ERL_LIBS` environment variable, it still doesn't solve th problem for other tools like running eunit or common tests.

``` bash
ERL_LIBS=MYAPP/deps:PATH_TO_RIAK/riak/deps:/$ERL_LIBS
export ERL_LIBS
```

###How to build

Install rebar, then:

```
rebar compile
```

