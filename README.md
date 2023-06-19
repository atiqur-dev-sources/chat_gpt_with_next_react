# chat_gpt_with_next_react

Documentations:
https://www.codingthesmartway.com/how-to-use-chatgpt-with-react/

```
npm install chatgpt chatgpt-prompts
🏗️ Project Setup
Please feel free to read this blogpost I made if you are unfamiliar in setting up a NodeJS project that is ESM compatible. Otherwise, you can follow the commands below to set up your project.

git clone --depth 1 https://github.com/pacholoamit/chatgpt-prompts.git
cp -r chatgpt-prompts/examples/basic my-chatgpt-app
cd my-chatgpt-app
npm install
npm start  # Make sure to change the OPEN_AI_API_KEY in src/index.ts
🚀 Quickstart
By default the chatgpt-prompts persists the instance of the prompt you are using. All of the 140+ prompts found at awesome-chatgpt-prompts are compiled in this library.

import { createChatGPTPrompt } from "chatgpt-prompts";

const run = async () => {
  /**
   * @description ChatGPT Prompt, accepts the same parameters as the
   * ChatGPTAPI constructor, but returns a promise that resolves to a
   * ChatMessage.
   *
   * @see {@link https://github.com/transitive-bullshit/chatgpt-api/blob/main/docs/classes/ChatGPTAPI.md#constructor}
   *
   */
  const prompts = createChatGPTPrompt({
    apiKey: "OPEN_AI_API_KEY",
  });

  // Use the Accountant prompt of ChatGPT
  let res = await prompt.accountant("Why am I still broke as a software engineer?");
  console.log(res.text);

  res = await prompt.accountant("How do I not become broke as a software engineer?");
  console.log(res.text);

  res = await prompt.accountant("Am I a software engineer?");
  console.log(res.text);
};

run().catch((err) => console.log("Something went wrong"));
```
