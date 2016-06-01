# logio server

## Installation
### Step 1 Installation

```
docker pull maltyxx/logio_server
```

### Step 2 Run

```
docker run -ti -p 28777 -p 28778:28778 --name logio_server maltyxx/logio_server
```

### Step 3 Compose

```yaml
logio_harvester:
    image: maltyxx/logio_harvester
    ports:
        - "28777"
        - "28778:28778"
    environment:
        - TZ=Europe/Paris
    restart: always
```
