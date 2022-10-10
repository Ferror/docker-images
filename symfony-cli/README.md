# Usage

```Dockerfile
FROM ferror/symfony-cli:latest AS symfony-cli

COPY --from=symfony-cli /usr/bin/symfony /usr/bin/symfony
```
