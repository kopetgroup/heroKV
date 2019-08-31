# heroKV

simple key value store built on top of RocksDB

git: 
```
https://github.com/kopetgroup/heroKV.git
```
### run
```
docker run --rm -ti --name herokv -p 8080:8080 afnia/herokv
```

### build & run
```
docker build -t herokv .
```

### test

- set
```
http://localhost:8080/set/key/valueX
http://localhost:8080/set/key2/valueX
```
- set [json data]
```
curl --request POST \
  --url http://localhost:8080/set/kopet \
  --header 'content-type: application/json' \
  --data '{
	"nowplaying": {
        "title": "Joker (2019)",
        "year": 2019
    }
}'
```

- get
```
http://localhost:8080/get/key
```

- keys
```
http://localhost:8080/keys/ke
```

