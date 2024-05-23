## Deployment
### Docker (Recommended)

```shell
docker pull LightningK/LightningAI-chat

docker run -d -p 3000:3000 \
   -e OPENAI_API_KEY=sk-xxxx \
   -e CODE=your-password \
   LightningK/LightningAI-chat
```

You can start service behind a proxy:

```shell
docker run -d -p 3000:3000 \
   -e OPENAI_API_KEY=sk-xxxx \
   -e CODE=your-password \
   -e PROXY_URL=http://localhost:7890 \
   LightningK/LightningAI-chat
```

If your proxy needs password, use:

```shell
-e PROXY_URL="http://127.0.0.1:7890 user pass"
```

### Shell

```shell
bash <(curl -s https://raw.githubusercontent.com/LightningK/LightningAI-chat/main/scripts/setup.sh)
```
