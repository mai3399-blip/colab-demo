# Creative ideas in Google Colab

A beginner-friendly notebook that asks for an everyday object and uses the
OpenAI Responses API with `gpt-6-luna` to suggest **three numbered unusual, practical ideas** per object.
Each idea is explained in 2-3 short sentences. Enter objects one at a time in a
loop, and type `quit` to stop.

## Run it

1. Open [Google Colab](https://colab.research.google.com/).
2. Choose **File > Upload notebook** and select `creative_ideas.ipynb`.
3. Run the cells from top to bottom with their play buttons. The first code cell installs or updates the OpenAI SDK; no local Python installation or GPU is needed.
4. Enter your OpenAI API key at the hidden `getpass` prompt.
5. Enter an everyday object, for example `paper clip`. Read the three numbered ideas.
6. Keep entering more objects at the prompt. The same key is used throughout the loop.
7. Type `quit` to stop (any capitalization works). Blank input asks you to try again without calling the API. To start a new session, rerun the final code cell and enter your key again.

You need internet access, an [OpenAI API key](https://platform.openai.com/api-keys),
model access, and available API credit. API usage may incur charges.
If a request fails, check these requirements and retry. Error details are
intentionally hidden to avoid exposing credentials.

## Keep your key private

- Enter the key only at the runtime prompt. Never paste it into code, Markdown, outputs, the README, or Git.
- The key stays in runtime memory and is passed directly to the SDK; it is not saved to a file or environment variable.
- The notebook prints only the generated ideas or a generic status message, never the key or raw exceptions.
- Disconnect and delete the Colab runtime when finished to clear memory.
- Clear all cell outputs and inspect the notebook before sharing or committing it.

The object text is sent to OpenAI. The request uses `store=False` to disable
response storage; this does not change other applicable API data policies.

## Files

- `creative_ideas.ipynb`: commented, step-by-step Colab notebook with no saved outputs.
- `hello_colab.ipynb`: existing class demo, left unchanged.

## References

- [OpenAI text generation and Responses API](https://developers.openai.com/api/docs/guides/text?lang=python)
- [GPT-6 Luna](https://developers.openai.com/api/docs/models/gpt-6-luna)
