# llamash
RESTful API Bridge for [Ollama](https://ollama.com).

### Build and Run
```shell
$ go build .
$ ./llamash
```

### Setup
Before starting the bridge server, you need a running Ollama server which the address is ```http://127.0.0.1:11434``` in default.
```shell
$ podman run --network host ollama serve
$ ./llamash -p 11444 -i 'http://127.0.0.1:11434'
```

### Enjoy it!
```shell
$ curl 'http://127.0.0.1:11444/generate?model=codellama&prompt=sayhi'
```

GET Form:
- ```generate``` Generate content.
    - ```model``` The LLaMA model you gonna use.
    - ```prompt``` The content will send to the model.
    
Responds in pure text.
