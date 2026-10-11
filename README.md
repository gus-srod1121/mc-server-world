# Docker Compose
docker-compose.yml
```yml
container_name: mc-server
pull_policy: daily

tty: true
stdin_open: true

ports:
  - 25565:25565       # java
  - 19132:19132/udp   # bedrock
  - 24454:24454/udp   # voicechat

environment:
  EULA: TRUE

  TYPE: FABRIC
  VERSION: 26.2

  MEMORY: 2G

volumes:
  - ./data:/data

# command: --safeMode

restart: unless-stopped
```
