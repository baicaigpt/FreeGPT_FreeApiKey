# 开发须知
>
>一定要替换为白菜的api base和api key，差一个都是不对的。
>
```js
1、使用白菜转发API_KEY: baicai_xxxxxxxx 替换官方 API_Key: sk-xxxxxxxx
2、使用白菜转发API_BASE: api.baicaigpt.com 替换官方域名：api.openai.com
```

>兼容OpenAI官方库，大部分ChatGPT[三方客户端或插件](https://github.com/baicaigpt/FreeGPT_FreeApiKey/tree/main/01%E5%BA%94%E7%94%A8%E7%A4%BA%E4%BE%8B/02%E7%BB%88%E7%AB%AF%E7%94%A8%E6%88%B7)可用。

## 1、curl请求
```js
curl https://api.baicaigpt.com/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer 你的白菜API_KEY" \
  -d '{
    "model": "gpt-3.5-turbo",
    "messages": [{"role": "user", "content": "Hello!"}]
  }'
```
正常运行，返回如下

![image](https://github.com/baicaigpt/FreeGPT_FreeApiKey/assets/160614217/dc7a73dd-fae0-4654-8911-827ae1fabfe2)
