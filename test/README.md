# Commands used

inside this folder

## Build
```bash
s2i build -E environment . seldonio/seldon-core-s2i-python3:1.8.0-dev local-debug:0.1
docker run -p 9000:9000 local-debug:0.1
```


## Test
```bash
curl -X POST localhost:9000/api/v0.1/predictions  -H "Content-Type: application/json" -d '{"jsonData":{"board_state":[[-1,1,-1,-1,-1],[1,2,-1,-1,-1],[-1,2,1,-1,-1],[-1,-1,-1,1,-1],[-1,-1,-1,-1,-1]],"ship_types":[{"type":"Destroyer","cells":[[1,1],[2,1]]}]}}'
```
