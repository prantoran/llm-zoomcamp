## Install Ollama

https://github.com/ollama/ollama

curl -fsSL https://ollama.com/install.sh | sh


```bash
ollama start
```

```bash
ollama run phi3
```


## Running Ollama and Phi 3 in Docker-Compose

```bash
docker run -it \
    --name elasticsearch \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3
```

```bash
docker run -it \
    -v ollama:/root/.ollama \
    -p 11434:11434 \
    --name ollama \
    ollama/ollama
```

```bash
docker exec -it ollama bash
```

```bash
ollama pull phi3
```

```bash
streamlit run qa_faq.py
```