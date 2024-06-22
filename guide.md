Install the packages:

```bash
pipenv install tqdm notebook==7.1.2 openai elasticsearch
```

If you use OpenAI, we need the key:

* Sign up at https://platform.openai.com/ if you don't have an account
* Go to https://platform.openai.com/api-keys
* Create a new key, copy it 

Let's put the key to an env variable:


```bash
export OPENAI_API_KEY="TOKEN"
```

But a better way for managing keys is using direnv:

```bash
sudo apt update
sudo apt install direnv 
direnv hook bash >> ~/.bashrc
```

Create / edit `.envrc` in your project directory:

```bash
export OPENAI_API_KEY='sk-proj-key'
```

Make sure `.envrc` is in your `.gitignore` - never commit it!

```bash
echo ".envrc" >> .gitignore
```

Allow direnv to run:

```bash
direnv allow
```