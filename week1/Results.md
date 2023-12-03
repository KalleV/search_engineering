# Results

## Baseline

```sh
python query.py --query_file $QUERY_FILE --max_queries 10000
```

```sh
INFO:Finished running 10000 queries in 0.9850499600501886 minutes
```

## Change the name matching field to no longer be a fuzzy match

```json
"match": {
    "name": {
        // ...
        "fuzziness": "0",
        // ...
    }
}
```

```sh
INFO:Finished running 10000 queries in 0.8921986607660074 minutes
```

## Drop the function scores

```sh
INFO:Finished running 10000 queries in 0.8213414676836692 minutes
```

## Drop every other matching function except the multi_match

```sh
INFO:Finished running 10000 queries in 1.2199404365829347 minutes
```

## Last, but not least, change the multi_match to only search the name and shortDescription field.

```sh
INFO:Finished running 10000 queries in 1.2182371075983005 minutes
```
