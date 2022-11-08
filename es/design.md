
## full-text search
todo

## embedding

### itemId-vector
itemId-vector-index
```json
{
  "mappings": {
    "properties": {
      "itemId-vector": {
        "type": "dense_vector",
        "dims": 10,
        "index": true,
        "similarity": "l2_norm"
      },
      "itemId": {
        "type": "keyword"
      }
    }
  }
}
```

data   
eg:
```json
{ "index": { "_id": "1" } }
{ "itemId-vector": [0.0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9], "itemId": "item_999999" }

```

query  
eg:  
```json
{
  "knn": {
    "field": "itemId-vector",
    "query_vector": [0.0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9],
    "k": 10,
    "num_candidates": 20
  },
  "fields": [ "itemId"]
}
```