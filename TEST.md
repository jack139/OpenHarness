# Local Test

# docker

```bash
docker build -t openharness -f ./Dockerfile .
```


# first config

```bash
# Initialize config (first time only)
docker run -it -v ./runtime/.openharness:/root/.openharness --rm openharness setup

# Edit config on host to add API keys
vim ./runtime/.openharness/settings.json
```


# run

```bash
# Or run a single command
docker run -v ./runtime/.openharness:/root/.openharness --rm openharness -p "hello"

# for test
docker run -it -v ./runtime/.openharness:/root/.openharness --rm --entrypoint bash openharness
```
