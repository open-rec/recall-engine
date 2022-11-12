
## full-text search
todo

## embedding

### itemId-vector
{scene}_itemId-vector-index
```json
{
  "mappings": {
    "properties": {
      "vector": {
        "type": "dense_vector",
        "dims": 10,
        "index": true,
        "similarity": "l2_norm"
      },
      "id": {
        "type": "keyword"
      }
    }
  }
}
```