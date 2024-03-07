# AutoGen示例说明
- AI Agnet仅限GPT4支持，请完成一次请求Token不可预估，请留意费用消耗。
- 免费会员GPT4配额，很可能不足以支撑完成DEMO演示，建议付费会员测试体验。
- 部分示例代码参考AutoGen官方文档，重点验证白菜GPT对AutoGPT的支撑能力，代码说明，请参考官方文档。
- 所有示例代码均在colab上调试通过，仅需替换白菜GPT的API_KEY即可

# 更新日志

## 20240307 AutoGen示例
### 1、agentchat_stream
- 交互LLM代理处理数据流
> AutoGen提供由LLM、工具或人类驱动的可对话代理，可通过自动聊天进行任务执行。该框架通过多代理对话允许工具使用和人类参与。请在此处找到关于此功能的文档。在本示例中，我们演示如何使用定制代理持续从网络获取新闻并请求投资建议。
- AutoGen官方文档
> https://github.com/microsoft/autogen/blob/main/notebook/agentchat_stream.ipynb

- 白菜GPT示例代码
> https://gist.github.com/baicaigpt/66510b611cb337b86aa3472786ae5c11

### 2、agentchat_function_call
- 这段代码的主要功能是利用谷歌搜索 API 搜索新闻，并通过自动生成的代理进行对话式交互。
>该代码段是一个简单的 Python 脚本，用于创建一个自动获取谷歌新闻并撰写新闻稿的功能。以下是代码中各部分的功能说明：

search_google_news(keyword): 这个函数使用 SerpApi 模块来搜索谷歌新闻。它接受一个关键词作为参数，并返回相关新闻的链接列表。

autogen: 这是一个模块，用于创建对话式代理。它创建了两个代理对象：assistant 和 user_proxy。

llm_config: 这是配置参数，用于设置语言模型的行为。其中包含了模型、超参数等配置信息。

system_message: 这是一个系统提示消息，用于向用户介绍其在对话中的角色和任务。

user_proxy.initiate_chat: 这个方法启动了代理之间的对话，并向 assistant 发送了一条消息，请求搜索关于“哈马斯”的谷歌新闻并撰写一篇新闻。

- 白菜GPT示例代码
> https://gist.github.com/baicaigpt/1770d02b855c773b9a71ed44562ce629