# This repository is intended for shell script examples

**Execute command passing parameter resulting from another command**
```bash
curl -s -X GET https://dummyjson.com/products/1 | jq '.thumbnail' | xargs curl  -O
```
