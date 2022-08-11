# OpenCanary

Docker builds every week based on [official OpenCanary repository](https://github.com/thinkst/opencanary)  
Build repo - https://github.com/acheremisov/opencanary.  
Builds for ARM64 and x86

**Docker Compose**

```
services:
  opencanary:
    image: acheremisov/opencanary:latest
    container_name: opencanary
    restart: unless-stopped
    name: opencanary
    ports:
    # Include other ports, depends on your config file
      - 21:21
      - 80:80
    volumes:
      - "${PWD}/data/.opencanary.conf":"/root/.opencanary.conf"
```

[Configuration file and environment variables](https://opencanary.readthedocs.io/en/latest/starting/configuration.html)
