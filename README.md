
# 🦜🔗✏️LangChain Ghost Blogger
EcrivAI is a fully automated AI blog writer that uses LangChain and GPT type LLMs for topic selection and content generation. Forked from original maintainer in order to take advantage of stronger LLMs which have been released.

## Usage
### Prerequisites
1. 🐍 You will need a working install of [`conda`](https://www.anaconda.com/download#downloads).
2. 🔑 You will need an API key from OpenAI, Google, or Claude. You can create one for free here, but usage incurs costs:
    - [OpenIA](https://platform.openai.com/account/api-keys) - to use models like GPT4
    - [Google](https://ai.google.dev/) - to use models like Gemini
    - [Claude](https://www.anthropic.com/api) - Claude models

### Dev Environment Setup
1. Set up your API keys in a file called `.env` (see `.env.example` for an example)
2. Set up and activate conda environment
    ```bash
    conda env create -f conda.yml
    conda activate ecrivai
    ```

> If you are having trouble setting your environment variables with the `.env` file or you want to manually add them instead of using a `.env` file, you can set your environment variable in your `ecrivai` conda environment like this:
>```shell
> # set api key env var
> conda env config vars set OPENAI_API_KEY="your-api-key-here"
> conda env config vars set GOOGLE_API_KEY="your-api-key-here"
> # re-activate env
> conda activate base
> conda activate ecrivai
>```

### CLI

> Note: Remember to activate your `ecrivai` conda environment before doing this (see above)

You can quickly generate a new original blog by running:

```
python ecrivai/add_blog.py
```

This will add a blog to a Markdown file in a directory called `content/`. You can also specify your own output directory by running this instead:
```
python ecrivai/add_blog.py --out-dir path/to/dir
```
